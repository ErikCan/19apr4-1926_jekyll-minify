# Minify Jekyll output

* Remove whitespace and comments for HTML and JavaScript (optionally other HTML things)
* Deliver extremely commented and formatted developer's code as easy-to-process one-liner for browsers
* Use [Jekyll](https://jekyllrb.com/) ([Liquid](https://shopify.dev/docs/liquid/reference/basics)) only, no complex tool chain necessary

*No minification by replacing (long) "speaking" names with arbitrary identifiers **=> try to use short IDs already while coding, declaring them in - e.g. [JSDoc](https://jsdoc.app/) - comments (don't be too confident to understand "undeclared" long speaking names after some months)**.*


## Under the hood

This is a fork of the well done [jekyll-compress-html (JCH)][site] by Anatol Broder / penibelst - maybe the term "compress" might be slightly misleading since it does no ZIPing or the like, but minifies to the extent stated above.

The only functional change to JCH here is stripping off HTML *and* JavaScript comments in one pass (technically: adding `comments2`: original `comments: all` strips off `<!-- -->`, added `comments2: all` strips off `/* */`).



## Usage

[Download](https://github.com/ErikCan/jekyll-compress-html/releases/latest) `compress.html` to your `_layouts` directory and define it to be used by any "real" layout, e.g. as some "root" layout in a hierarchy or explicitely in every layout's front matter. Nothing else necessary, minification happens by / as normal Jekyll layout applying.




[site]: http://jch.penibelst.de/
