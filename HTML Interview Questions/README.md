[![MasterHead](https://github.com/Sakib963/bistro-boss-server/assets/66853064/51508d0e-6e5d-47bb-892c-433205f28283)](https://github.com/Sakib963)

<h1 align="center">👀 HTML INTERVIEW QUESTIONS AND ANSWERS 👀 </h1>

## 1. Are the HTML tags and elements the same thing?

No. HTML elements are defined by a starting tag, may contain some content and a closing tag.For example, < h1>Heading 1< /h1> is a HTML element but just < h1> is a starting tag and < /h1> is a closing tag.

## 2. What are tags and attributes in HTML?

Tags are the primary component of the HTML that defines how the content will be structured/ formatted, whereas Attributes are used along with the HTML tags to define the characteristics of the element. For example, < p align=” center”>Interview questions< /p>, in this the ‘align’ is the attribute using which we will align the paragraph to show in the center of the view.

## 3. What are different types of lists in HTML?

There are two types of lists in HTML. These are: Ordered List and Unordered List.

```
<ul>
    <li>Hello</li>
    <li>This is</li>
    <li>Unordered List</li>
</ul>
<ol>
    <li>Hello</li>
    <li>This is</li>
    <li>Ordered List</li>
</ol>
```

## 4. What is the ‘class’ attribute in HTML?

The class attribute is used to specify the class name for an HTML element. Multiple elements in HTML can have the same class value. Also, it is mainly used to associate the styles written in the stylesheet with the HTML elements.

## 5. What is the difference between the ‘id’ attribute and the ‘class’ attribute of HTML elements?

Multiple elements in HTML can have the same class value, whereas a value of id attribute of one element cannot be associated with another HTML element.

## 6. What are the different kinds of Doctypes available?

The three kinds of Doctypes which are available:

- Strict Doctype
- Transitional Doctype
- Frameset Doctype

## 7. What is the difference between < strong>, < b> tags and < em>, < i> tags?

The effect on a normal webpage of the tags < strong>, < b> and < em>, < i> is the same. < b> and < i> tags stands for bold and italic. These two tags only apply font styling and bold tag < b>, just adds more ink to the text, these tags don't say anything about the text.

Whereas, < strong> and < em> tags represent that the span of text is of strong importance or more importance and emphatic stress respectively than the rest of the text. These tags have semantic meaning.

## 8. Can we display a web page inside a web page or Is nesting of webpages possible?

Yes, we can display a web page inside another HTML web page. HTML provides a tag < iframe> using which we can achieve this functionality.

```
<iframe src=”url of the web page to embed” />
```

## 9. Is it possible to change an inline element into a block level element?

Yes, it is possible using the “display” property with its value as “block”, to change the inline element into a block-level element.

## 10. How can we club two or more rows or columns into a single row or column in an HTML table?

HTML provides two table attributes “rowspan” and “colspan” to make a cell span to multiple rows and columns respectively.

## 11. What is the difference between “display: none” and “visibility: hidden”, when used as attributes to the HTML element.

When we use the attribute “visibility: hidden” for an HTML element then that element will be hidden from the webpage but still takes up space. Whereas, if we use the “display: none” attribute for an HTML element then the element will be hidden, and also it won’t take up any space on the webpage.

## 12. How to specify the link in HTML and explain the target attribute?

HTML provides a hyperlink - < a> tag to specify the links in a webpage. The ‘href’ attribute is used to specify the link and the ‘target’ attribute is used to specify, where do we want to open the linked document. The ‘target’ attribute can have the following values:

- \_self: This is a default value. It opens the document in the same window or tab as it was clicked.
- \_blank: It opens the document in a new window or tab.
- \_parent: It opens the document in a parent frame.
- \_top: It opens the document in a full-body window.

## 13. In how many ways can we specify the CSS styles for the HTML element?

There are three ways in which we can specify the styles for HTML elements:

- Inline: Here we use the ‘style’ attribute inside the HTML element.
- Internal: Here we use the < style> tag inside the < head> tag. To apply the style we bind the elements using ‘id’ or ‘class’ attributes.
- External: Here we use the < link> tag inside < head> tag to reference the CSS file into our HTML code. Again the binding between elements and styles is done using ‘id’ or ‘class’ attributes.

## 14. Difference between link tag < link> and anchor tag < a>?

The anchor tag < a> is used to create a hyperlink to another webpage or to a certain part of the webpage and these links are clickable, whereas, link tag < link> defines a link between a document and an external resource and these are not clickable.

## 15. How to include javascript code in HTML?

HTML provides a < script> tag using which we can run the javascript code and make our HTML page more dynamic.

```
<!DOCTYPE html>
<html>
   <body>
    <h1>
        <span>This is a demo for </span>
        <u><span id="demo"></span></u>
   </h1>
   <script>
       document.getElementById("demo").innerHTML = "script Tag"
   </script>
   </body>
</html>
```

## 16. What are some of the advantages of HTML5 over its previous versions?

Some advantages of HTML5 are:-

- It has Multimedia Support.
- It has the capabilities to store offline data using SQL databases and application cache.
- Javascript can be run in the background.
- HTML5 also allows users to draw various shapes like rectangles, circles, triangles, etc.
- Included new Semantic tags and form control tags.\*

## 17. How can we include audio or video in a webpage?
HTML5 provides two tags: < audio> and < video> tags using which we can add the audio or video directly in the webpage.

## 18. Inline and block elements in HTML5?
![plot](./images/inline%20vs%20block.PNG)

## 19. What is the difference between < figure> tag and < img> tag?
The < figure> tag specifies the self-contained content, like diagrams, images, code snippets, etc. < figure> tag is used to semantically organize the contents of an image like image, image caption, etc., whereas the < img> tag is used to embed the picture in the HTML5 document.

## 20. What are Semantic Elements?
Semantic elements are those which describe the particular meaning to the browser and the developer. Elements like < form>, < table>, < article>, < figure>, etc., are semantic elements.