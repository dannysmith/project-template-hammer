# Project Template (Hammer)

This is a base tempate for building static sites using [Hammer](http://hammerformac.com/). It's based partially on [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate). There is a similar template for those that use CodeKit [here](https://github.com/manyhatsdesign/project-template-codekit).

## Directories

* `/css` - contains a minified main.scss with all the other SCSS files imported.
* `/fonts` - an empty folder for font files.
* `/img` - contains all image files for the project
* `/includes` - contains partials as `.kit` files. They should start with an underscore.
* `/js` - contains the projects javascript files.
* `/js/vendor` - contains jQuery & Modenizr. Other plugins can go in here, but be aware of the number of HTTP requests. It might be better to build plugins into `plugins.js` using codekit imports.
* `/sprite` - contains images that should be compiled into a sprite using Compass. This can be removed if the project isn't using codekit.

## SCSS Source Files

* `_normalize.scss` - CSS Reset. Currently using [Version 2.0.1](https://github.com/necolas/normalize.css).
* `_base.scss` - Contains fixes for some common bugs and base styles.
* `_layout.scss` - Should contain layout-speciffic class declarations. See [SMACSS](http://smacss.com/) for more information on organising styles.
* `_helpers.scss` - Contains a stripped-down version of the helper classes from H5BP.
* `_print.scss` - Contains print-specific styles based on H5BP.

Each module (again, see [SMACSS](http://smacss.com/)) should have its own SCSS file. Hammer also imports Bourboun by default.

## Other Source Files

* `includes/_head.kit` - The top part of each page, based on H5BP.
* `includes/_foot.kit` - The bottom part of each page.
* `includes/_grid.kit` - A fluid grid overlay for use during development.
* `js/boxsizing-polyfill.htc` - A [polyfill](https://github.com/Schepp/box-sizing-polyfill) that allows IE to understand box-sizing.
* `main.js` - User Scripts should go in here.
* `plugins.js` - Based on H5BP, with a few additions.
* `codekit-config.json` - A CodeKit Config File
* `index.kit` - A template for the index page. Other pages should be dropped in the root and import `_head` and `_foot` like this.

## Typography

This template aims to keep superfluous code to a minimum. It only contains code that I find myself using in every project. As a consiquence, it keeps the typography and layout code to a minimum. The base font size is reduced to 10px using a percentage and thereafter `rem`s are used to declare font-sizes and heights, based on this value. This means that 1rem = 10px so the maths is a little easiter. Because rems aren't widely supported, A pixel value is always declared first.

Two baseline images are included for use with the grid overlay. One is at 20px and the other at 26px as these are the most common line-heights in my work.

## Grid

The bones for creating a fluid grid using nice round numbers are already present in the template, and an overlay is provided for use in development. You can turn the overlay off by setting `display: none;` on `#overlay` in `_grid.kit`, or by turning off the import for that file.

You should always build a grid that fits your design so this is only provided as an example. I'll be writing about building fluid grids soon, but theres some very sparce info [here](http://blog.dasmith.co.uk/post/24476543889/simple-responsive-grid). 

## HTML5 Boilerplate Version

This template currently uses Version 2.0.3 (9 Dec 2012) but may have been updated with some of the more recent changes. See the [H5BP changelog](https://github.com/h5bp/html5-boilerplate/blob/master/CHANGELOG.md).

## Contributing & Credit

If you'd like to contribute, go ahead and fork.

This template was built by [Danny Smith](http://dasmith.co.uk) ([@dannysmith](http://twitter.com/dannysmith)) and is based on [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate). It incorporates a number of other fixes and suggestions, some of which were written by others.

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/manyhatsdesign/project-template-hammer/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

