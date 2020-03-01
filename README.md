# Minify [Jekyll](https://jekyllrb.com/) output

* Remove whitespace and comments for HTML and JavaScript (optionally other HTML things)
* Deliver extremely commented and formatted developer's code as easy-to-process one-liner for browsers
* Jekyll / [Liquid](https://shopify.dev/docs/liquid/reference/basics) only, integrated in Jekyll's normal processing, no easy-to-forget post-Jekyll steps or complex tool chain necessary

*No minification by replacing (long) "speaking" names with arbitrary identifiers **=> try to use short IDs already while coding, declaring them in - e.g. [JSDoc](https://jsdoc.app/) - comments (don't be too confident to understand "undeclared" long speaking names after some months)**.*


## Under the hood

This is a fork of the well done [jekyll-compress-html (JCH)][site] by Anatol Broder / penibelst - maybe the term "compress" might be slightly misleading since it does no ZIPing or the like, but minifies to the extent stated above.

The only functional change to JCH here is stripping off HTML *and* JavaScript comments in one pass (technically: adding `comments2`: original `comments: all` strips off `<!-- -->`, added `comments2: all` strips off `/* */`).

Another change is the provision of needed stuff here. The original JCH has a [site] for information and download and a [repository](https://github.com/penibelst/jekyll-compress-html) for development, the latter rather sophisticated and complex with very exemplary tests. This fork has only this repo for information, download and development (of course backed up by the linked original work). The master branch here (that what you see here) is reduced to a minimum to allow a more straightforward encounter with that great JCH util, for original's full development coverage see branch master-full-penibelst-staff.


## Usage

[Download](https://github.com/ErikCan/jekyll-compress-html/releases/latest) `compress.html` to your `_layouts` directory and define it as layout for your existing layout(s), e.g. as some "root" layout in a hierarchy or explicitely in every layout's front matter. Nothing else necessary, minification happens by / as normal Jekyll layout applying.




[site]: http://jch.penibelst.de/
