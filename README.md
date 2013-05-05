SassyBones beta
==========

A Skeleton-Based SASS grid system that relies on extensions instead of mixins to produce clean, lightweight code.

I've included the watched and compiled `css/` folder just so you can see the fact that main.css is empty.
Unless you are using a column, SassyBones won't add any CSS for that column.

Using extensions feels right to me because it makes the CSS feel very object-oriented.  Rather than
using a mixin to just drop some code inside of a bunch of defined classes repeatedly, we instead specify a base
object using the SASS placeholder (`%`) and extend those classes with the page's custom classes.
