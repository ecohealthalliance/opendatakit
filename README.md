
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Slide Deck for the Presentation on Open Data Kit for the Methods and Models Meetings (M3)

<!-- badges: start -->

<!-- badges: end -->

This repository contains the `Rmarkdown` script and related materials
used to produce the slide deck for the presentation on Open Data Kit for
the Methods and Models Meetings (M3) on the 26th of January 2021.

## The slide deck

The slide deck was created using [Yihui Xie’s `{xaringan}`
package](https://github.com/yihui/xaringan) and Garrick Aden-Buie’s
ninja-themed presentation Rmarkdown template from his
[`{xaringanthemer}`
package](https://github.com/gadenbuie/xaringanthemer).

The **Rmarkdown** document is named `opendatakit.Rmd`. The **Rmarkdown**
document relies on additional resources to produce the slide deck. These
are:

  - `xaringan-themer.css` - this is the CSS that comes included when
    using the [`{xaringanthemer}`
    package](https://github.com/gadenbuie/xaringanthemer)’s ninja-themed
    presentation template. This CSS file is dynamically re-generated
    using new style specifications used in the **Rmarkdown** document

  - `libs` folder - this directory contains javascript libraries used by
    [`{xaringanthemer}`
    package](https://github.com/gadenbuie/xaringanthemer) to generate
    the HTML slides

  - `images` folder - contains graphics used in the slides

These abovementioned four files are what is needed to reproduce the
slide deck.

## Publishing the slide deck online

To publish the slide deck online, the following workflow using [GitHub
Pages](https://pages.github.com) was used:

1.  Rendered the `opendatakit.Rmd` file into an HTML file with the
    filename `index.html`.

<!-- end list -->

``` r
rmarkdown::render(input = "opendatakit.Rmd", output_file = "index.html")
```

By using `index.html` as the output filename, the resulting URL will
need to just point to the enclosing directory.

2.  Created a `gh-pages` branch for the `opendatakit` repository.

3.  Enabled [GitHub Pages](https://pages.github.com) by selecting the
    `gh-pages` branch as the [GitHub Pages](https://pages.github.com)
    source.

After this, the slide deck is now published online at
<https://ecohealthalliance.github.io/opendatakit/>

## Creating a PDF version of the slide deck

The slide deck was converted into PDF using the `{pagedown}` package:

``` r
pagedown::chrome_print(input = "index.hml", output = "opendatakit.pdf")
```

This operation produces a PDF file of the presentation called
`opendatakit.pdf`. This operation requires that Google Chrome or
Chromium (for Linux) is installed on your computer.

## Additional resources

In addition to the four files or directories discussed above, a
directory named `forms` is also included in this repository. This
contains 2 demonstration/example XLSForms used in the presenration.
