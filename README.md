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


# HTML Structure

```
<html>
 <head>
 </head>
 <header>
 </header>
 <body>
 </body>
 <footer>
 </footer>
</html>
```


```
* **Head**
contains the metadata for a web page. 
Metadata is information about the page that isn’t displayed directly on the web page. 
Unlike the information inside of the <body> tag, the metadata in the head is information about the page itself. 

* **Title**
A browser’s tab displays the title specified in the <title> tag
```
 <title> </title>
```


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

# target="_blank"
for a link to open in a new window

<a href="" target="_blank"></a>

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

* **Folder Organize**
```
project-folder/
|—— about.html
|—— contact.html
|—— index.html
```
---

# HTML Tables

## Create Table 

* to add rows using the table row element: <tr>
```
<table>
  <tr>
  </tr>
  <tr>
  </tr>
</table>
```

* to add data to a table
```
<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```

* To add titles to rows and columns, you can use the table heading element: <th>

Note, also, the use of the scope attribute, which can take one of two values:

row - this value makes it clear that the heading is for a row.
col - this value makes it clear that the heading is for a column.
 
 
 ```
 <table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
 ```
 * Table Head
 ```
 <thead>
    <tr>
      <th></th>
      <th scope="col">Saturday</th>
      <th scope="col">Sunday</th>
    </tr>
  </thead>
 ```
 
 * add border
 ```
table, th, td {
  border: 1px solid black;
  font-family: Arial, sans-serif;
  text-align: center;
}
 ```
 * Spanning Columns
 ```
 <table>
  <tr>
    <th>Monday</th>
    <th>Tuesday</th>
    <th>Wednesday</th>
  </tr>
  <tr>
    <td colspan="2">Out of Town</td>
    <td>Back in Town</td>
  </tr>
</table>
 ```
* Spanning Rows
```
<table>
  <tr> <!-- Row 1 -->
    <th></th>
    <th>Saturday</th>
    <th>Sunday</th>
  </tr>
  <tr> <!-- Row 2 -->
    <th>Morning</th>
    <td rowspan="2">Work</td>
    <td rowspan="3">Relax</td>
  </tr>
  <tr> <!-- Row 3 -->
    <th>Afternoon</th>
  </tr>
  <tr> <!-- Row 4 -->
    <th>Evening</th>
    <td>Dinner</td>
  </tr>
</table>
```

* table body
Long tables can be sectioned off using the table body element: <tbody>.
The <tbody> element should contain all of the table’s data
used to separate the body of the table from its headers and footers
 ```
     <tbody>
    <tr>
      <th>Company Name</th>
      <th>Number of Items to Ship</th>
      <th>Next Action</th>
    </tr>
    </tbody>
 ```
 
* table footer
Footers are often used to contain sums, differences, and other data results.
bottom part of a long table can also be sectioned off using the <tfoot> element.
 ```
   <tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
 ```
 ---
 # DOM
 
 ```
 document.object.innerHTML = 'text'
 ```
 
 
 All HTML elements are objects.
 The document object has methods that allow you to select the desired HTML element.
 
 ```
 //finds element by id
document.getElementById(id) 

//finds elements by class name
document.getElementsByClassName(name) 

//finds elements by tag name
document.getElementsByTagName(name)

var elem = document.getElementById("demo");
elem.innerHTML = "Hello World!";


var arr =  document.getElementsByClassName("demo");
//accessing the second element
arr[1].innerHTML = "Hi";


<p>hi</p>
<p>hello</p>
<p>hi</p>
<script>
var arr = document.getElementsByTagName("p");
for (var x = 0; x < arr.length; x++) {
  arr[x].innerHTML = "Hi there";
}
</script>
 ```
 
 
### Working with DOM

```
Each element in the DOM has a set of properties and methods that provide information about their relationships in the DOM:
element.childNodes returns an array of an element's child nodes.
element.firstChild returns the first child node of an element.
element.lastChild returns the last child node of an element.
element.hasChildNodes returns true if an element has any child nodes, otherwise false.
element.nextSibling returns the next node at the same tree level.
element.previousSibling returns the previous node at the same tree level.
element.parentNode returns the parent node of an element.
```
```
<html>
  <body>
    <div id ="demo">
      <p>some text</p>
      <p>some other text</p>
    </div>

    <script>
     var a = document.getElementById("demo");
     var arr = a.childNodes;
     for(var x=0;x<arr.length;x++) {
       arr[x].innerHTML = "new text";
     }
    </script>

  </body>
</html>
```
## Changing Attributes

```
<img id="image" src="a.png" alt=""/>
<script>
  var el = document.getElementById("image");
  el.src = "apple.png"
</script>
```

```
<a href="http:// "></a>
<script>
  var el = document.getElementsByTagName("a");
  el[0].href = "http://";
</script>
```

## Changing Style

```
<div id="demo" style="width:200px">some text</div>
<script>
  var x = document.getElementById('demo');
  x.style.color = '6600FF';
  x.style.width = '100px';
</script>
```

## Creating elements 

* element.cloneNode() clones an element and returns the resulting node.
* document.createElement(element) creates a new element node.
* document.createTextNode(text) creates a new text node.

```
var node = document.createTextNode("Some new text");
```

This will create a new text node, but it will not appear in the document until you append it to an existing element with one of the following methods:
```
element.appendChild(newNode) adds a new child node to an element as the last child node.
element.insertBefore(node1, node2) inserts node1 as a child before node2.
```
```
<div id ="demo">some content</div>

<script>
  //creating a new paragraph
  var p = document.createElement("p");
  var node = document.createTextNode("Some new text");
  //adding the text to the paragraph
  p.appendChild(node);

  var div = document.getElementById("demo");
  //adding the paragraph to the div
  div.appendChild(p);
</script>
```

```

var el = document.createElement("li");
var txt = document.createTextNode("B");
el.appendChild(txt);
var ul = document.getElementById("list");
ul.appendChild(el);
```

## Removing Elements

To remove an HTML element, you must select the parent of the element and use the removeChild(node) method.

```
<div id="demo">
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>

<script>
var parent = document.getElementById("demo");
var child = document.getElementById("p1");
parent.removeChild(child);
</script>
```

alternative way
```
var child = document.getElementById("p1");
child.parentNode.removeChild(child);
```

## Replacing Elements

To replace an HTML element, the element.replaceChild(newNode, oldNode) method is used

```
<div id="demo">
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>

<script>
var p = document.createElement("p");
var node = document.createTextNode("This is new");
p.appendChild(node);

var parent = document.getElementById("demo");
var child = document.getElementById("p1");
parent.replaceChild(p, child);
</script>
```


# navigating in same page 

```
<a href="#s1">Go to S1</a>
<h2 id="s1">Section 1</h2>
```
