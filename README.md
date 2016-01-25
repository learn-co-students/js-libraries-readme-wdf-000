# JS Libraries

## Objectives
+ Explain what a JS library is
+ Explain why jQUery was invented
+ Include jQuery in an HTML page


## Intro 

A JavaScript library is prewritten JavaScript code that allows for easy integration to streamline your own code base

There are many JavaScript libraries designed for different purposes. Jasmine is the library we use for writing tests. D3.js is a library for data visualization, Bootstrap has a JavaScript library for adding animations and effects to our sites, Node.js is a library for writing server side JavaScript.

One of the most widely used JavaScript libraries is **jQuery**. 

## The Problem with JavaScript

As you've learned from CSS, not all browsers are created equal. There are properties specific to each browser, and code you have to write for designs and features to be cross-browser compatible. Even though things have improved drastically from the earlier versions of browsers (Internet Explorer 6, etc.), because of the core browser standers, we still have to pay attention to browser differences.

JavaScript has evolved in much the same way as CSS. Even though things have improved considerably, there are definitely differences in the way JavaScript must be handled across browsers.

Let's say we want to use JavaScript to add a CSS property to an HTML element.

We'll be working with the following HTML (which is also in `html/index.html` for you to test yourself with the console) for this example.

```html
<!doctype html>
<head>
  <title> JavaScript Madness</title>
</head>
<body>
  <p id="hey">HEY HEY HEY HEY HEY</p>
</body>
```

This HTML renders as a white page with black text displaying `"HEY HEY HEY HEY HEY"` in the top left corner of the page.

Let's say we want to change the font color to blue and the background color of the `p` tag to gray using JavaScript. We could do that with the following JavaScript:

```js
document.getElementById("hey").style.color = "blue";
document.getElementById("hey").style.backgroundColor = "#ccc";
```

The `document` is the JavaScript object that represents the HTML document that gets loaded to render the page. We can use JavaScript functions to select and manipulate different HTML elements via the `document`. 

The functions `getElementById()` selects an HTML element by an ID. In this case we're passing in the ID `"hey"` which will select the `p` tag on our page. We're then using the JavaScript `style.property = "value"` function which allows us to change the CSS of an element.

Now that we're familiar with using JavaScript to change the CSS, let's try to float the text to the right side of the page.

For earlier versions of Firefox and Chrome, you could achieve that with the following JS:

```js
document.getElementById("header").style.cssFloat = "left";
```

But this code wouldn't work with earlier versions of Internet Explorer. Instead, you would have to write:

```js
document.getElementById("header").style.styleFloat = "left";
```

This need for different JavaScript code for different browsers can get very messy very quickly. Suddenly you need crazy if-statements and browser detection to trigger different lines of code for each browser, all just for a simple CSS change. 

## jQuery To The Rescue

jQuery was created to solve this problem of needing different lines of code for different browsers. If you include the jQuery library in your code, you can write one single line of code that handles each browser on it's own. AMAZING!

jQuery provides us with immense convenience methods that make our jobs as developers much easier, especially when dealing with AJAX and API calls. We can write significantly fewer lines of code and still achieve the same effect. jQuery is also an open source library and has a tremendous community around it. At the time of this writing, over [78% of the top million sites on the web use jQuery](http://trends.builtwith.com/javascript/jQuery) - crazy! There are many many jQuery plugins (like Ruby gems) which provide additional functionality, and allow us to build complex applications very quickly.



