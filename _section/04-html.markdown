---
title:  "HTML"
date: 2015-05-01
hashlink: html
---

HTML stands for Hypertext Markup Language. These were heavily used HTML structures and best practices.

### Basic HTML structure:

{% highlight html %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8"/>
  <title>Page Title</title>
  <link rel="author" href="humans.txt"/>
  <link rel="stylesheet" href="style.css?v1.0"/>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="keywords" content="tags, tags, tags">
</head>

<body>

  <!-- Content goes here -->

  <script type="text/javascript" src="script.js"></script>

</body>

</html>
{% endhighlight %}

* Regarding humans.txt, you can read more about it on <a href="http://humanstxt.org/">humans.txt</a> website.
* Links to Javascript file should sits at the end of body content. Performance issues.
* Use CSS cache busting technique for CSS and Js.

### Semantic Elements in HTML 5:

**Header** --- Defines the header of a page or section. It often contains a logo, the title of the Web site, and a navigational table of content. Example:

{% highlight html %}
<header>
  <h1><a href="/">infomalaya</a></h1>
  <p class="description">Curated News 1.0</p>
</header>
{% endhighlight %}

**Section** --- Defines a section in a document. Example:

{% highlight html %}
<section>
  <h1>Heading</h1>
  <p>Bunch of awesome content</p>
</section>
{% endhighlight %}

**Nav** --- Defines a section that contains only navigation links. Example:

{% highlight html %}
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
{% endhighlight %}

**Article** --- Defines self-contained content that could exist independently of the rest of the content. Example:

{% highlight html %}
<article>
  <h4>A really awesome article</h4>
  <p>Lots of awesome text.</p>
</article>
{% endhighlight %}

**Aside** --- Defines some content loosely related to the page content. If it is removed, the remaining content still makes sense. Example:

{% highlight html %}
<article>
  <p>The Disney movie <em>The Little Mermaid</em> was first released to theatres in 1989.</p>
  <aside>The movie earned $87 million during its initial release.</aside>
  <p>More info about the movie...</p>
</article>
{% endhighlight %}

**Footer** --- Defines the footer for a page or section. It often contains a copyright notice, some links to legal information, or addresses to give feedback. Example:

{% highlight html %}
<footer>
  <p>Some copyright info or perhaps some author info for an article?</p>
</footer>
{% endhighlight %}

### HTML5 semantic elements in action, example:

{% highlight html %}
<main><!-- Begin main document -->

  <header><!-- Begin header -->
    <h1></h1>
  </header><!-- End header -->

  <section class="content"><!-- Begin content section -->

    <article><!-- Begin article area -->
      <hgroup>
        <h2></h2>
      </hgroup>

      <p></p>
    </article><!-- End article area -->

    <nav class="pagination"><!-- Begin page navigation -->
      <p class="left"><a href="#">&laquo; Older</a></p> 
      <p class="right"><a href="#">Newer &#187;</a></p>
    </nav><!-- End page navigation -->

  </section><!-- End content section -->

  <section class="sidebar"><!-- Begin sidebar section -->

    <aside class="widget">
      <h3></h3>
    </aside>

  </section><!-- End sidebar section -->

  <footer><!-- Begin footer -->
    <p></p>
  </footer><!-- End footer -->

</main><!-- End main document -->
{% endhighlight %}

* View the <a href="https://developer.mozilla.org/en/docs/Web/Guide/HTML/HTML5/HTML5_element_list">complete HTML5 element list</a> from Mozilla Developer Network.

### HTML best practices:

* Always comment the code block. Example:
{% highlight html %}
<footer><!-- Begin footer -->
  <p>Hosted on <a href="#">GitHub Pages</a></p>
</footer><!-- End footer -->
{% endhighlight %}
* Use classes, not ID's, unless it's for DOM or hashlinks.
* Use <a href="http://css-tricks.com/semantic-class-names/">semantic</a> markup and class name. Refer Schema.org for more info.
* Use <a href="http://www.html-5-tutorial.com/all-html-tags.htm">all available</a> HTML tags and elements to avoid divitis Syndrome.
* Use <a href="http://alistapart.com/article/understandingprogressiveenhancement">progressive enhancement</a> whenever possible.

### HTML resources:

<ul>
  <li><a href="http://alistapart.com/article/a-brief-history-of-markup">A Brief History of Markup by Jeremy Keith</a></li>
  <li><a href="http://www.smashingmagazine.com/2009/04/22/progressive-enhancement-what-it-is-and-how-to-use-it/">Progressive Enhancement: What It Is, And How To Use It? By Sam Dwyer</a></li>
  <li><a href="http://mdo.github.io/code-guide/">Code Guide by Mark Otto</a></li>
  <li><a href="http://alistapart.com/article/accessibility-the-missing-ingredient">Accessibility: The Missing Ingredient by Andrew Hoffman</a></li>
  <li><a href="http://webdesign.tutsplus.com/articles/quick-tip-dont-forget-the-viewport-meta-tag--webdesign-5972">Don't Forget the Viewport Meta Tag by Ian Yates</a></li>
</ul>