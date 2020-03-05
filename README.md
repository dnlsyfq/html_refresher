> i know .. rather than just google for quick cheatsheet . Made my own references . 


# Basic HTML and HTML5


**Heading**
```
<h1>Top level heading: Maybe a page title</h1>
```

**Paragraph**
```
<p>A paragraph of text. Some information we would like to communicate to the viewer. This can be as long or short as we would like.</p>
```

**Main**

* main HTML5 tag helps search engines and other developers find the main content of your page.

```
<main> 
  <h1>Hello World</h1>
  <p>Hello Paragraph</p>
</main>
```

**img**

```
<img src="https://www.your-image-source.com/your-image.jpg">
```

* alt attribute is used for screen readers to improve accessibility and is displayed if the image fails to load.

```
<img src="https://www.your-image-source.com/your-image.jpg" alt="Author standing on a beach with two thumbs up.">
```

**a**

* to link to content outside of your web page.

```
<a href="https://freecodecamp.org">this links to freecodecamp.org</a>

```
* a (anchor) elements can also be used to create internal links to jump to different sections within a webpage.

* To create an internal link: 
    1. assign a link's href attribute to a hash symbol # plus the value of the id attribute for the element that you want to internally link to
    2. add the same id attribute to the element you are linking to. 

```
    <a href="#contacts-header">Contacts</a>

    <h2 id="contacts-header">Contacts</h2>
```

