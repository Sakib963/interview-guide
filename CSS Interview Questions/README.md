[![MasterHead](https://github.com/Sakib963/bistro-boss-server/assets/66853064/51508d0e-6e5d-47bb-892c-433205f28283)](https://github.com/Sakib963)

<h1 align="center">👀 CSS INTERVIEW QUESTIONS AND ANSWERS 👀 </h1>


## 1. What is CSS?
CSS stands for Cascading Style Sheet. It’s a style sheet language that determines how the elements/contents in the page are looked/shown. CSS is used to develop a consistent look and feel for all the pages.

## 2. What is the Box model in CSS? Which CSS properties are a part of it?
A rectangle box is wrapped around every HTML element. The box model is used to determine the height and width of the rectangular box. The CSS Box consists of Width and height (or in the absence of that, default values and the content inside), padding, borders, margin.
![plot](./images/Box_Model_in_CSS.jpg)

* Content:  Actual Content of the box where the text or image is placed.
* Padding: Area surrounding the content (Space between the border and content).
* Border: Area surrounding the padding.
* Margin: Area surrounding the border.

## 3. What are the advantages of using CSS?
The main advantages of CSS are given below:

* Separation of content from presentation - CSS provides a way to present the same content in multiple presentation formats in mobile or desktop or laptop.
* Easy to maintain - CSS, built effectively can be used to change the look and feel complete by making small changes. To make a global change, simply change the style, and all elements in all the web pages will be updated automatically.
* Bandwidth - Used effectively, the style sheets will be stored in the browser cache and they can be used on multiple pages, without having to download again.

## 4. What are the limitations of CSS?
Disadvantages of CSS are given below:

* Browser Compatibility: Some style selectors are supported and some are not. We have to determine which style is supported or not using the @support selector.
* Cross Browser issue: Some selectors behave differently in a different browser.
* There is no parent selector: Currently, Using CSS, you can’t select a parent tag.

## 5. How to include CSS in the webpage?
There are different ways to include a CSS in a webpage, 

1 - External Style Sheet: An external file linked to your HTML document: Using link tag, we can link the style sheet to the HTML page.
```css
<link rel="stylesheet" type="text/css" href="mystyles.css" />
```
2 - Embed CSS with a style tag: A set of CSS styles included within your HTML page.
```css
<style type="text/css">

/*Add style rules here*/

</style>
```
3 - Add inline styles to HTML elements(CSS rules applied directly within an HTML tag.): Style can be added directly to the HTML element using a style tag.
```css
<h2 style="color:red;background:black">Inline Style</h2>
```
4 - Import a stylesheet file (An external file imported into another CSS file): Another way to add CSS is by using the @import rule. This is to add a new CSS file within CSS itself.
```javascript
@import "path/to/style.css";
```
## 6. What are the different types of Selectors in CSS?
* Universal Selector: The universal selector works like a wildcard character, selecting all elements on a page. In the given example, the provided styles will get applied to all the elements on the page.
```css
* {
  color: "green";
  font-size: 20px;
  line-height: 25px;
}
```
* Element Type Selector: This selector matches one or more HTML elements of the same name. In the given example, the provided styles will get applied to all the ul elements on the page.
```css
ul {
  line-style: none;
  border: solid 1px #ccc;
}
```
* ID Selector: This selector matches any HTML element that has an ID attribute with the same value as that of the selector. In the given example, the provided styles will get applied to all the elements having ID as a container on the page.
```css
#container {
  width: 960px;
  margin: 0 auto;
}

<div id="container"></div>
```
Class Selector: The class selector also matches all elements on the page that have their class attribute set to the same value as the class.  In the given example, the provided styles will get applied to all the elements having ID as the box on the page.
```css
.box {
  padding: 10px;
  margin: 10px;
  width: 240px;
}

<div class="box"></div>
```
## 7. What is VH/VW (viewport height/ viewport width) in CSS?
It’s a CSS unit used to measure the height and width in percentage with respect to the viewport. It is used mainly in responsive design techniques. The measure VH is equal to 1/100 of the height of the viewport. If the height of the browser is 1000px, 1vh is equal to 10px. Similarly, if the width is 1000px, then 1 vw is equal to 10px.
## 8. Difference between reset vs normalize CSS?. How do they differ?
Reset CSS: CSS resets aim to remove all built-in browser styling. For example margins, paddings, font-sizes of all elements are reset to be the same. 

Normalize CSS: Normalize CSS aims to make built-in browser styling consistent across browsers. It also corrects bugs for common browser dependencies.

## 9. What is the difference between inline, inline-block, and block?
* Block Element: The block elements always start on a new line. They will also take space for an entire row or width. List of block elements are < div>, < p>.

* Inline Elements: Inline elements don't start on a new line, they appear on the same line as the content and tags beside them. Some examples of inline elements are < a>, < span> , < strong>, and < img> tags. 

* Inline Block Elements: Inline-block elements are similar to inline elements, except they can have padding and margins and set height and width values.

## 10. Does margin-top or margin-bottom have an effect on inline elements?
No, it doesn’t affect the inline elements. Inline elements flow with the contents of the page.