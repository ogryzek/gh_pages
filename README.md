#HTML, CSS, Bootstrap, Fontawesome, and Jekyll on Github Pages with Facebook API, Twitter API, and Brace forms  
## Introduction to HTML
[HTML Elements](http://meiert.com/en/indices/html-elements/) | [Semantics(WHATWG.org)](http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html) | [HTML Reference(W3.org)](http://www.w3.org/TR/html-markup/elements.html)   
  
HTML is a markup language used to format content for the web. It not only helps with the display and visualization of data, but it helps to *organize information*, making it accessible to human and web-crawler alike.  
  
The basic syntax of HTML consists of elements, which have attributes, which in turn have values. 
```html
<!-- Legend -->
<element attribute="value">
</element>
```
Here's a real world example could be for an image of [Sir Tim Berners-Lee](http://en.wikipedia.org/wiki/Tim_Berners-Lee) (inventor of the World Wide Web and director of the W3C), located at `http://i.telegraph.co.uk/multimedia/archive/00682/bernerslee-404_682192c.jpg`
```html
<img src="http://i.telegraph.co.uk/multimedia/archive/00682/bernerslee-404_682192c.jpg" alt="Tim Berners-Lee">
```  
![Sir Tim Berners-Lee](http://i.telegraph.co.uk/multimedia/archive/00682/bernerslee-404_682192c.jpg)  

Some elements have a single tag, such as the `<img>` element. We call elements with only one tag 'void elements'. Other elements, such as the paragraph element `<p></p>` have opening `<p>` and closing `</p>` tags. Elements with opening and closing tags may also have attributes, and sometimes contain other elements within them.  
  
The Anchor element is a great example of an element that has both an opening and a closing tag. We use anchor tags to create hypertext references (links). The following example creates a link to [Google](http://www.google.com).
```html
<a href="http://www.google.com">Google</a>
```  
The layout of a web page consists of a [document type declaration](http://en.wikipedia.org/wiki/Document_type_declaration), followed by an html element, which contains the head and the body.  
  
The head contains information that the server may use to determine how to render the html document, such as the character set to use. The current standard is UTF-8, and we put that value into the charset attribute of a meta element in the head.  
```html
<meta charset="UTF-8">
``` 
```html
<!-- Basic Structure -->
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
  </body>
</html>

<!-- HTML Common Elements -->
<a></a>
<article></article>
<aside></aside>
<body></body>
<button></button>
<br>
<div></div>
<em></em>
<form></form>
<h1></h1>
<h2></h2>
<h3></h3>
<h4></h4>
<h5></h5>
<h6></h6>
<head></head>
<hr>
<html></html>
<i></i>
<img>
<label></label>
<legend></legend>
<li></li>
<link>
<meta>
<nav></nav>
<ol></ol>
<optgroup></optgroup>
<option><option>
<p></p>
<pre></pre>
<script></script>
<select></select>
<section></section>
<small></small>
<span></span>
<strong></strong>
<style></style>
<sub></sub>
<sup></sup>
<table></table>
<td></td>
<textarea></textarea>
<th></th>
<title></title>
<tr></tr>
<ul></ul>
```
**1.) Build out an HTML page with a meta element for the charset and a title element in the head, an unordered list of links for the navigation, a welcome header, a tagline paragraph, and a table for showing products, features and pricing.**  
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>My Super Awesome Services Page</title>
  </head>
  <body>
    <ul>
      <li><a href="/index.html">home</a></li>
      <li><a href="/about.html">about</a></li>
      <li><a href="/blog.html">blog</a></li>
      <li><a href="mailto:drew@codecore.ca">contact</a></li>
    </ul>
    <h1>Welcome to My Super Awesome Services Page!</h1>
    <p>Check out all the awesome services</p>
    <table>
      <tr>
        <th></th>
        <th>Basic</th>
        <th>Pro</th>
        <th>Ultra</th>
      </tr>
      <tr>
        <td>users</td>
        <td>1</td>
        <td>up to 10</td>
        <td>unlimited</td>
      </tr>
      <tr>
        <td>emails</td>
        <td>up to 100/month</td>
        <td>up to 10,000/month</td>
        <td>unlimited</td>
      </tr>
      <tr>
        <td>support</td>
        <td>user forums</td>
        <td>user forums/call center</td>
        <td>priority forums/priority calls</td>
      </tr>
      <tr>
        <td>price</td>
        <td>free</td>
        <td>$10/month</td>
        <td>$25/month</td>
      </tr>
    </table>
  </body>
</html>
```
## CSS
CSS (cascading stylesheets) is used to add styles to websites. Rather than have to specify the color or layout of each element individually, we can set styles for an entire website all in one file. We can select elements by element name, or assign and id for a single item, or a class for multiple items. The precedence is id, class, and element name, respectively.  
  
To add styles to an element, just add the element name then some styles in the stylesheet.
```css
body { background-color: #000; color: #fff; }
``` 
To add styles to a class of elements, add a dot before the class name
```css
.nav { list-style: none; color: #444; }
```
To add styles to an element with an id, add a hash tag before the id.  
```css
#services th { color: #f8f8f8; background-color: #34e; }
```
There are also [psuedo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes), which help us select styles based on certain behavior, or situations, such as when a checkbox is `:checked`.
```css
.nav li:hover { background-color: #34e; }
```
**2.) Practice adding some styles using element, class, and id selectors, and pseudo-classes.**  
```css
body {
  background-color: #f8f8f8;
  color: #444;
}

.nav {
  list-style: none;
}

.nav li {
  padding: 10px;
  background-color: #444;
  display: inline;
}

.nav li:hover {
  background-color: #34e;
}

.nav li a {
  color: #f8f8f8;
  text-decoration: none;
}

h1 {
  color: #34e;
}

#services tr:nth-child(even) {
  background-color: #444;
  color: #f8f8f8;
}

#services th {
  color: #f8f8f8;
  background-color: #34e;
}

#services th:first-child {
  background-color: #f8f8f8;
}
```
## Bootstrap
[Bootstrap](http://getbootstrap.com/) is a framework that is often used to quickly structure and style the look and feel of many web sites and web applications. To have accesses to the bootstrap classes, simply download bootstrap, add the bootstrap.css file to your styles directory, and add import it in your stylesheet.css
```css
@import url(bootstrap.css)
```
We now have access to various classes that will help layout our site. Let's add `.table table-bordered`, and `.table-striped` to our table element, and wrap it in a div `table-responsive`.
```css
      <div class="table-responsive">
        <table class="table table-bordered table-striped" id="services-table">
          <tr>
            <th></th>
            <th>Basic</th>
            <th>Pro</th>
            <th>Ultra</th>
          </tr>
          <tr>
            <td>users</td>
            <td>1</td>
            <td>up to 10</td>
            <td>unlimited</td>
          </tr>
          <tr>
            <td>emails</td>
            <td>up to 100/month</td>
            <td>up to 10,000/month</td>
            <td>unlimited</td>
          </tr>
          <tr>
            <td>support</td>
            <td>user forums</td>
            <td>user forums/call center</td>
            <td>priority forums/priority calls</td>
          </tr>
          <tr>
            <td>price</td>
            <td>free</td>
            <td>$10/month</td>
            <td>$25/month</td>
          </tr>
        </table>
      </div>
```
we also have access to classes like `.jumbotron` for larger content areas. We can also use a class `row` to put columns into, and define their behavrior at various page sizes, on a [twelve column grid](http://getbootstrap.com/examples/grid/), such as `.col-md-4`
```css
      <div class="jumbotron text-center content-jumbo">
        <div class="section-title">
          <h1>Super Awesome Services</h1>
        </div>
        <div class="row">
          <div class="service-box col-md-4">
            <p>Send mail! Not in envelopes, but this icon does look like an envelope.</p>
          </div>
          <div class="service-box col-md-4">
            <p>All your documents in a convenient and fashionable directory of folders</p>
          </div>
          <div class="service-box col-md-4">
            <p>Paper is for airplanes. Email is for mail. Start using it today.</p>
          </div>
        </div>
      </div>
```
Bootstrap also has `.nav` classes, such as `.nav-justified`.
```css
        <ul class="nav nav-justified" id="nav-main">
          <li class="active"><a href="/index.html">home</a></li>
          <li><a href="/about.html">about</a></li>
          <li><a href="/blog.html">blog</a></li>
          <li><a href="mailto:drew@codecore.ca">contact</a></li>
        </ul>
```
## Fontawesome
[Fontawesome](http://fortawesome.github.io/Font-Awesome/) icons give us access to a bunch of icons we can use. Just like with bootstrap, we just need to download and install some files, then reference then import into our stylesheets.  
  
Put the `font-awesome.min.css` in your stylesheets directory, and the `FontAwesome.otf`, and other fontawesome-webfont files in a new directory called `fonts`.  
  
We can add them in place of a logo, for example let's add one to our nav menu. We add the class `fa` to an icon element, then the name of the icon, such as `fa-cube`, and we can set the size, for example if I want it to display four times normal size `fa-4x`.
```css
        <ul class="nav nav-justified" id="nav-main">
          <li><i class="fa fa-cube fa-4x"></i></li>
          <li class="active"><a href="/index.html">home</a></li>
          <li><a href="/about.html">about</a></li>
          <li><a href="/blog.html">blog</a></li>
          <li><a href="mailto:drew@codecore.ca">contact</a></li>
        </ul>
``` 
## Jekyll
[Jekyll](http://jekyllrb.com/) is an HTML framework that allows a sort of dynamic content (such as blogs) with only HTML.
## Github Pages
[Github pages](https://pages.github.com/) offers free hosting for your HTML/CSS and Javascript website, and can even be used with custom domains.
## Twitter API
Add "Tweet" and "Follow" buttons, and personal embedded tweets using [Twitter's API](https://dev.twitter.com/docs/tfw).  
  
To add a Twitter "Tweet" button, there are two parts needed: The script
that defines the functionality of the button, and an element to call the
functionality and display a button.  
  
1.) The script
```html
<script>
  !function(d,s,id){
    var
    js,fjs=d.getElementsByTagName(s)[0];
    if(!d.getElementById(id)){
      js=d.createElement(s);
      js.id=id;
      js.src="https://platform.twitter.com/widgets.js";
      fjs.parentNode.insertBefore(js,fjs);
    }
  }
  (document,"script","twitter-wjs");
</script>
```
2.) The anchor element calling the script
```html
<a href="https://twitter.com/share" class="twitter-share-button"
data-lang="en">Tweet</a>
```
## Facebook API
Add Facebook [like](https://developers.facebook.com/docs/plugins/like-button) and [share](http://jsfiddle.net/subodhghulaxe/QqKKr/) buttons.  
  
As with most social media APIs, with Facebook, to add a like button, we need to include a
script that defines the functionality, and an element to call the
script.  
  
1.) The script
```html
<div id="fb-root"></div>
<script>
  (function(d, s, id) {
  var js, fjs = d.getElementsByTagName(s)[0];
  if (d.getElementById(id)) return;
  js = d.createElement(s); js.id = id;
  js.src = "//connect.facebook.net/en_US/sdk.js#xfbml=1&version=v2.0";
  fjs.parentNode.insertBefore(js, fjs);
  }
  (document, 'script', 'facebook-jssdk'));
</script>
```
2.) The element containing the script. ***note***: Twitter's tweet
button used an anchor element, and Facebook's like is contained within a
div. As the behavior is class based, this is more a matter of personal
preference, and either should work just as well.
```html
<div class="fb-like"
data-href="https://developers.facebook.com/docs/plugins/"
data-layout="button" data-action="like" data-show-faces="false"
data-share="false"></div>
```

## Brace
Add contact forms using [Brace](http://forms.brace.io/).
