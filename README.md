# Jekyll sample content
I found myself creating *dummy* content over and over again to test Jekyll themes against. So to save time I put together a collection of posts, pages, and collections that cover all sorts of edge cases one might encounter.

This was predominately built to test [my Jekyll themes](https://mademistakes.com/work/jekyll-themes/) so there are a few layout specific tests in there. But otherwise it should be a solid starting point to test your project against.

## Usage

Simply copy the files into your project and assign `layout: ` as a [Front Matter default](https://jekyllrb.com/docs/configuration/#front-matter-defaults). Layouts haven't been assigned to make things more flexible as everyone names them differently.

**Examples:**

```yaml
defaults:
  
  # all posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: true
      related: true

  # all _pages
  - scope:
      path: ""
      type: pages
    values:
      layout: single

  # recipes collection
  - scope:
      path: ""
      type: recipes
    values:
      layout: single
  
  # pets collection
  - scope:
      path: ""
      type: pets
    values:
      layout: single

  # portfolio collection
  - scope:
      path: ""
      type: portfolio
    values:
      layout: single
```

## Sample Content

| Name | Description | Layout Dependent |
| ---- | ----------- | --------------- |
| **authors** | `authors.yml` data file for testing multi-author sites | Yes |
| **drafts** | sample draft posts | No |
| **includes** | various helpers for generating galleries, feature blocks, table of contents, etc. | Yes |
| **pages** | sample pages, 404 error page, and various Liquid-based archives | No |
| **collections** | collection documents for `_pets`, `_recipes`, `_portfolio` | No |
| **posts** | sample posts with a range of content and edge-cases | Yes |
| **images** | image assets found in sample posts and collections | No |

Some archives make use of the [`group-by-array`](https://github.com/mushishi78/jekyll-group-by-array) include helper.

---

## License

MIT License

Copyright (c) 2016 Michael Rose

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
