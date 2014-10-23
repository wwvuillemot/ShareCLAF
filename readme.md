Introduction
======

This project is composed of three (3) `git` repositories.  It is meant as a
proof of concept on how to share components such as CSS, JS, and even HTML
templates between different app frameworks using [Bower](http://bower.io).

  * **[ShareCLAF](http://github.com/wwvuillemot/ShareCLAF)** This repo
  * **[ShareRails](http://github.com/wwvuillemot/ShareCLAF)** Describes how to setup Bower with Rails
  * **[ShareAngularJS](http://github.com/wwvuillemot/ShareCLAF)** Describes how to setup Bower with AngularJS

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
