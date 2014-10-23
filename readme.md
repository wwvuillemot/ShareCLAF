Introduction
======

This project is composed of three (3) `git` repositories.  It is meant as a
proof of concept on how to share components such as CSS, JS, and even HTML
templates between different app frameworks using [Bower](http://bower.io).

  * **[ShareCLAF](http://github.com/wwvuillemot/ShareCLAF)** Contains the shared CLAF (common look and feel)
  * **[ShareRails](http://github.com/wwvuillemot/ShareRails)** Describes how to setup Bower with Rails
  * **[ShareAngularJS](http://github.com/wwvuillemot/ShareAngularJS)** Describes how to setup Bower with AngularJS

Motivation
======

This is mostly a bit of homework on to share CLAF (common look and feel) between
various web properties.  There are a lot of tools out there nowadays, and we are
starting to see various frameworks be deployed in a federated way for a single
brand.  In the hopes of applying the principle of DRY (Don't Repeat Yourself), I
thought it worth a cup of coffee (or two) to see how best to stitch different
frameworks together using a common look while reducing (eliminating?)
copy-and-paste.

Assumptions
=======

LESS
-----

For now I am assuming we will use [LESS](http://lesscss.org).  While there are
merits to [SASS](http://sass-lang.com), there is not enough material difference
between the two to worry about for purposes of this recipe.

Javascript
------

For now we are assuming plain-ole vanilla JavaScript.  Using CoffeeScript or
some other intermediary language, while possibly preferable to some, introduces
higher-order complexities to the overall motivations.

HTML
------

Similarly, we are assuming plain-ole vanilla HTML for templates.  We will need
to figure out how best to share these between frameworks, as each framework has
its own syntax for parsing HTML  template directives differently.

Configuration
========

`/bower.json`
------------

Create `bower.json` in the root of the project, and add something similar to the
below.  For now, we have kept it as simple as possible.

     {
       "name": "ShareCLAF",
       "version": "0.0.1",
       "main": "stylesheets/claf.less",
       "ignore": [
         "**/*~"
       ],
       "dependencies": {
       },
       "devDependencies": {
       }
     }

CSS
-----

Create a root directory `/stylesheets` where your `less` files will go.

JavaScript
------

Create a root directory `/javascripts` where your JavaScript files will go.
