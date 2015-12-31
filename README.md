# Tufte Hugo Theme

Hugo-Tufte is a minimalist blog-like theme for the
[static site generator Hugo](https://gohugo.io) that
attempts to be a faithful implementation of the
[Tufte-css](https://githubcom/edwardtufte/tufte-css) project.
It supports mathematical typesetting via [MathJax](https://www.mathjax.org).
By utilizing copious partial templates the theme is largely customizable.

## Site Parameters

The site specific parameters that this theme :wrecognizes are:

- `subtitle` string: This is displayed under the main title.
- `showPoweredBy` boolean: if true, display a shoutout to Hugo and this theme.
- `copyrightHolder` string: Inserts the value in the default copyright notice.
- `copyright` string: Custom copyright notice.

## Page Parameters

- `hideDate` boolean: if true, do not display a page date.  When `meta` is set to
  true, `hideDate` takes greater precedence.
- `hideReadTime` boolean: if true, do not display the page's reading time
  estimate.  When `meta` is set to true, `hideReadTime` takes greater precedence.
- `math` boolean: if true, try to render the page's LaTeX code using MatheJax. The
  theme follows the conventions in [Hugo's MathJax tutorial].
- `meta` boolean: if true, display page meta-data author, date, categories provided
  these page parameters exist and are not overridden.  Content in the `/post` directory,
  (i.e., pages of type "post") ignore this parameter.
- `toc` boolean: if true, display the table of contents for the page.

## Shortcodes

This theme provides the following shortcodes. 

- `blockquote`
  - Description: Wrap text in a blockquote and insert optional
  `cite` or `footer` metadata.
  - Example: 
  ```html
  {{% blockquote cite="www.shawnohare.com" footer="Shawn" %}}
    There is nothing more beautiful than an elegant mathematical proof. 
  {{% /blockquote %}}`
  ```
- `marginnote`
  - Description: Wrap text to produce a numberless margin note.
  - Usage: Accepts a required positional argument that is the margin note id.
  `{{% marginnote "<margin note id>"" %}}...{{% /marginnote %}}`
  - Example: `{{% marginnote "mn-example" %}}Some marginnote{{% /marginnote%}}`

- `section`
   - Description: This shortcode is provided as a work-around for wrapping
   complex blocks of markdown in section tags.
   - Usage: `{{< section "<begin || end>" >}}` map respectively to
   `<section>` and `</section>` tags.
   - Example: `{{< section "begin" >}}` inserts a `<section>` tag, while
   `{{<section "end" >}}` inserts the closing `</section>` tag.

- `sidenote`
  - Description: Wrap text to produce an automatically numbered sidenote.
  - Usage: identical to `marginnote`. 
  Accepts a required positional argument that is the side note id.
  `{{% sidenote "<side note id>"" %}}...{{% /sidenote %}}`
  - Example: `{{% sidenote "sn-example" %}}Some sidenote{{% /sidenote %}}`


## Templates
TODO
- [ ] Describe the role of each template file, as commenting within the files
      themselves seems to break the templates.
