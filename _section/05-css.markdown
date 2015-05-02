---
title:  "CSS"
date: 2015-05-01
hashlink: css
---

CSS stands for Cascading Style Sheets. These were frequently used CSS snippets and best practices.

### Frequently used CSS Snippets:

**CSS content documentation**, to make it easier to maintain. Example:

{% highlight css %}
/*
Project's name: MentariCSS
Version: 3.0 beta
Author: @mohdhuzairy
Last date modified: 11/02/2014
*/

/*
------------------------------------
Table of Contents:
------------------------------------
1. Reset Styles
2. MentariCSS Core Styles
3. User's Styles
4. Media Queries Styles
------------------------------------
*/

/* =1. Reset Styles */

/* =2. MentariCSS Core Styles */

/* =3. User's Styles */

/* =4. Media Queries Styles */

/* EOF */
{% endhighlight %}

**Body tag**, example:

{% highlight css %}
body
{
  font:1em/150% arial, sans-serif;
  color:#333;
  background:#fff;
}
{% endhighlight %}

**Media queries**, taken from Andrew Clarke's [320 and Up](http://stuffandnonsense.co.uk/projects/320andup/). Example:

{% highlight css %}
@media only screen and (min-width: 480px)
{
  /* Styles */
}

@media only screen and (min-width: 600px)
{
  /* Styles */
}

@media only screen and (min-width: 768px)
{
  /* Styles */
}

@media only screen and (min-width: 992px)
{
  /* Styles */
}

@media only screen and (min-width: 1382px)
{
  /* Styles */
}

@media only screen and (-webkit-min-device-pixel-ratio: 1.5), only screen and (min--moz-device-pixel-ratio: 1.5), only screen and (min-device-pixel-ratio: 1.5)
{
  /* Styles */
}
{% endhighlight %}

**CSS Pseudo Elements**. Example:

{% highlight css %}
/* Selects the first letter of the element */
p:first-letter
{
  font-size:3em;
  float:left;
}

/* Selects the first line of the element */
p:first-line
{
  font-style:italic;
  color:#333;
}

/* Selects the element that is the first child of its parent */
p:first-child
{
  background:#eee;
}

/* Selects the element that is the last child of its parent */
p:last-child
{
  background:#eee;
}

/* Specify the background color for element that is the second child of its parent, counting from the last */
p:nth-last-child(2)
{
  background:#eee;
}

/* Specify the background color for every even elements of its parent */
tr:nth-child(even) td
{
  background:#f6f6f6;
}

/* Specify the background color for every odd elements of its parent */
tr:nth-child(odd) td
{
  background:#eee;
}

/* Insert content before the element */
p:before
{
  content:"Read this: ";
}

/* Insert content after the element */
p:after
{
  content:"- Remember this";
}
{% endhighlight %}

### CSS Frameworks?

The best CSS framework is no CSS framework at all. However, not all people have the time to write all the styles by themselves. I recommend these CSS frameworks, for their functionality, wide coverage of styles, and well written documentation:

* [Bootstrap](http://getbootstrap.com/)
* [Foundation by Zurb](http://foundation.zurb.com/)
* [HTML5 Boilerplate](http://html5boilerplate.com)
* [Normalize.CSS by Nicolas Gallagher](http://necolas.github.io/normalize.css/)
* [CSS Reset by Eric Meyer](http://meyerweb.com/eric/tools/css/reset/)

### CSS Best Practices:

* Use all available CSS selectors.
* Make CSS code readable by you, and by anyone else who concerns. No CSS compressing.
* Comment the CSS code to make it easier to maintain in future.
* Use [CSS cache busting](http://twosixcode.com/notes/view/simple-cache-busting-for-css-and-js) technique.
* Audit your CSS code using [CSS Lint](http://csslint.net/).
* Don't repeat yourself when it comes to writing CSS. Make use of classes combination features.
* [Avoid CSS hacks](https://www.google.com/search?q=avoid+css+hacks). We don't need any hacks if we write CSS properly.
* It would be great if we can learn to use CSS pre-processor such as SASS to speed up development timeframe.

### CSS resources:

<ul>
  <li><a href="http://css-tricks.com/pseudo-element-roundup/">A Whole Bunch of Amazing Stuff Pseudo Elements Can Do by Chris Coyier</a></li>
  <li><a href="http://www.smashingmagazine.com/2013/10/21/challenging-css-best-practices-atomic-approach/">Challenging CSS Best Practices by Thierry Koblentz</a></li>
  <li><a href="http://islovely.co/#/posts/writing-high-performance-css">Writing High Performance CSS by Dom Habersack</a></li>
  <li><a href="http://benfrain.com/css-performance-revisited-selectors-bloat-expensive-styles/">CSS performance revisited: selectors, bloat and expensive styles by Ben Frain</a></li>
  <li><a href="http://www.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/">CSS Specificity: Things You Should Know by Vitaly Friedman</a></li>
  <li><a href="http://www.w3schools.com/cssref/css_selectors.asp">CSS Selectors Reference by W3Schools</a></li>
</ul>