> i know .. rather than just google for quick cheatsheet . Made my own references . 


# Basic HTML and HTML5
 tell the browser which version of HTML your page is using. HTML is an evolving language, and is updated regularly. Most major browsers support the latest specification, which is HTML5. However, older web pages may use previous versions of the language.
```
 <!DOCTYPE html>
 <html>
  <!-- Your HTML code goes here -->
  <head>
    Metadata elements, such as link, meta, title, and style, typically go inside the head element.
  </head>
  <body>
  </body>
</html>


```
* **Head**
contains the metadata for a web page. 
Metadata is information about the page that isn’t displayed directly on the web page. 
Unlike the information inside of the <body> tag, the metadata in the head is information about the page itself. 



* **Displaying Text**

to display text in html 

* **Paragraph**
contain a block of plain text 
```
<p> </p>
```

* **Span**
contains short pieces of text , use to separate small pieces of content that are on the same line 
as other content
```
<div>
 <p>
  <span>The brown bear (Ursus arctos) is native to parts of northern Eurasia and North America. Its conservation status is currently Least Concern. There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</span>
 </p>
</div>
```

* **styling text**
built-in style

 * italic
 ```
 <em></em>
 ```
 * bold
 ```
 <strong></strong>
 ```

* **image**
```
<img src="" alt="" />
```

* **videos**
```
<video src="" width="" height="" controls> </video>
```

**Heading**
```
<h1>Top level heading: Maybe a page title</h1>
```

**Paragraph**
```
<p>A paragraph of text. Some information we would like to communicate to the viewer. This can be as long or short as we would like.</p>
```

**HTML Attributes**
Attributes are content added to the opening tag of an element and can be used in several different ways, from providing information to changing styling. Attributes are made up of the following two parts

* name of the attribute
  > use id attribute to specify different content e.g. DIV
  ```
  <div id="intro>
   <h1>Introduction</h1>
  </div>
  ```

* value of the attribute

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

* target is an anchor tag attribute that specifies where to open the link and the value "_blank" specifies to open the link in a new tab

```
  <a href="http://freecatphotoapp.com" target="_blank">cat photos</a>
```

* nested a tags 

```
<p>
  Here's a <a target="_blank" href="http://freecodecamp.org"> link to freecodecamp.org</a> for you to follow.
</p>
```

* dead link , to add a elements to your website before you know where they will link.

```
    <a href="#"></a>
```

* turn html elements into links by nesting them within an a element. use # as your a element's href property in order to turn it into a dead link.

```
<a href="#"><img src="https://bit.ly/fcc-running-cats" alt="Three kittens running towards the camera."></a>
```

**unordered lists**

* Unordered lists start with an opening <ul> element, followed by any number of <li> elements. 

```
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```

* Ordered lists start with an opening <ol> element, followed by any number of <li> elements. Finally, ordered lists are closed with the </ol> tag.

```
<ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
```

**Web Form**

* input elements are a convenient way to get input from your user.

```
<input type="text">
```

* create placeholder text

```
<input type="text" placeholder="this is placeholder text">
```

* build web forms that actually submit data to a server using nothing more than pure HTML.

```
<form action="/submit-cat-photo">
  <input type="text" placeholder="cat photo URL">
</form>
```

* submit button , clicking this button will send the data from your form to the URL you specified with your form's action attribute

```
<button type="submit">this button submits the form</button>
```
```
  <form action="/submit-cat-photo">
    <input type="text" placeholder="cat photo URL">
    <button type="submit">Submit</button>
  </form>
```

* require specific form fields so that your user will not be able to submit your form until he or she has filled them out.

```
  <form action="/submit-cat-photo">
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>

```

**Button : radio**

user to only give you one answer out of multiple options.

```
<label for="indoor"> 
  <input id="indoor" type="radio" name="indoor-outdoor">Indoor 
</label>
```

```
  <form action="/submit-cat-photo">
    <label for="indoor"><input id="indoor" type="radio" name="indoor-outdoor"> Indoor</label>
    <label for="outdoor"><input id="outdoor" type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>

```

**Button : checkboxes**
questions that may have more than one answer.
All related checkbox inputs should have the same name attribute.

```
  <form action="/submit-cat-photo">
    <label for="indoor"><input id="indoor" type="radio" name="indoor-outdoor"> Indoor</label>
    <label for="outdoor"><input id="outdoor" type="radio" name="indoor-outdoor"> Outdoor</label><br>

    <label for="one">
        <input id="one" type="checkbox" name="personality"> Grumpy
    </label>

    <label for="two">
        <input id="two" type="checkbox" name="personality"> Caring
    </label>

    <label for="three">
        <input id="three" type="checkbox" name="personality"> Hasty
    </label>


    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
```

**Webform value**
When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type radio and checkbox report their values from the value attribute.

If you omit the value attribute, the submitted form data uses the default value, which is 'on'.

```
  <form action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
    <label><input type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality" value="loving"> Loving</label>
    <label><input type="checkbox" name="personality" value="lazy"> Lazy</label>
    <label><input type="checkbox" name="personality" value="energetic">Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
```

* defaulted value 

> set a checkbox or radio button to be checked by default using the checked attribute.

```
<input type="radio" name="test-name" checked>
```

**Div**
* div short for division 
* division or container that divides the page into sections 
```
<div>
</div>
```
