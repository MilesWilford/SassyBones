SassyBones beta
Miles Wilford
==========

A Skeleton-Based SASS grid system that relies on extensions instead of mixins to produce clean, lightweight code.

Using extensions feels right to me because it makes the CSS feel very object-oriented.  Rather than
using a mixin to just drop some code inside of a bunch of defined classes repeatedly, we instead specify a base
object using the SASS placeholder (`%`) and extend those classes with the page's custom classes.

I made this because I really dislike grid systems and wanted to see if I could make a system I didn't hate using.
I don't think I was successful; grids still don't feel good to me.  This one is at least servicable, though.

Preqrequisites
-----------
This uses [SASS](http://sass-lang.com/).  That's it.

Install
----------------------
Just place `_sbgrid.scss` into the folder with your sass files.  Once it's in,

    @import "sbgrid";

That's all it takes.  The included `main.scss` file is for demonstration ONLY and should not be used.

Usage
--------------------
A bunch of placeholder files are specified in `_sbgrid.scss`.  To use any of these elements,
specify your own class or ID in the HTML, then in your main .scss file, `@extend %sb-placeholder;`

This uses the same 16-column 960px grid as Skeleton.css by default.  The following variables are specified:

    $grid-base:    960px !default;
    $column-count: 16 !default;
    $gutter:       10px !default;
    $row-break:    $gutter * 2 !default;


    $breakpoint-tablet-portrait:  959px !default;
    $breakpoint-mobile-landscape: 768px !default;
      $mobile-landscape-colwidth: 420px !default;
    $breakpoint-mobile-portrait:  480px !default;
      $mobile-portrait-colwidth:  300px !default;

You can change the value of any of these variables before your `@import` for a different-sized grid.

###Included placeholder classes
A sample page is provided at `sample.html`.  Here is a listing of all the elements you can use with `@extend`.

All placeholders start with `%sb-` except for the ones used in clearing.

* `%clearfix`
* `%clear`
* `%sb-container`
* `%sb-column`, `%sb-columns`
* `%sb-row`
* `%sb-1-col`, `%sb-1-cols`
* `%sb-#-col` where `#` is a number of columns between 2 and the specified `$column-count`
* `%sb-third`, `%sb-1-third`, `%sb-1-thirds`
* `%sb-2-third`, %sb-2-thirds
* `%sb-offset-#` where `#` is a number of columns between 1 and the speified `$column-count`
* `%sb-alpha`
* `%sb-omega`