# jQuery Tutorial

jQuery is a JavaScript Library.

jQuery greatly simplifies JavaScript programming.

Example

```javascript
$(document).ready(function() {
  $('p').click(function() {
    $(this).hide();
  });
});
```

## jQuery Introduction

The purpose of jQuery is to make it much easier to use JavaScript on your website.

## What You Should Already Know

Before you start studying jQuery, you should have a basic knowledge of:

- HTML
- CSS
- JavaScript

## What is jQuery?

jQuery is a lightweight, "write less, do more", JavaScript library.

The purpose of jQuery is to make it much easier to use JavaScript on your website.

jQuery takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code.

jQuery also simplifies a lot of the complicated things from JavaScript, like AJAX calls and DOM manipulation.

The jQuery library contains the following features:

- HTML/DOM manipulation
- CSS manipulation
- HTML event methods
- Effects and animations
- AJAX
- Utilities

**Tip:** In addition, jQuery has plugins for almost any task out there.

## Why jQuery?

There are lots of other JavaScript libraries out there, but jQuery is probably the most popular, and also the most extendable.

Many of the biggest companies on the Web use jQuery, such as:

- Google
- Microsoft
- IBM
- Netflix

## Will jQuery work in all browsers?

The jQuery team knows all about cross-browser issues, and they have written this knowledge into the jQuery library. jQuery will run exactly the same in all major browsers.

# jQuery Get Started

## Adding jQuery to Your Web Pages

There are several ways to start using jQuery on your web site. You can:

- Download the jQuery library from jQuery.com
- Include jQuery from a CDN, like Google

## Downloading jQuery

There are two versions of jQuery available for downloading:

- Production version - this is for your live website because it has been minified and compressed
- Development version - this is for testing and development (uncompressed and readable code)

Both versions can be downloaded from jQuery.com.

The jQuery library is a single JavaScript file, and you reference it with the HTML `<script>` tag (notice that the `<script>` tag should be inside the `<head>` section):

```html
<head>
  <script src="jquery-3.4.1.min.js"></script>
</head>
```

**Tip:** Place the downloaded file in the same directory as the pages where you wish to use it.

Do you wonder why we do not have type="text/javascript" inside the `<script>` tag?

This is not required in HTML5. JavaScript is the default scripting language in HTML5 and in all modern browsers!

## jQuery CDN

If you don't want to download and host jQuery yourself, you can include it from a CDN (Content Delivery Network).

Both Google and Microsoft host jQuery.

To use jQuery from Google or Microsoft, use one of the following:

### Google CDN:

```html
<head>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
</head>
```

### Microsoft CDN:

```html
<head>
  <script src="https://ajax.aspnetcdn.com/ajax/jQuery/jquery-3.4.1.min.js"></script>
</head>
```

### One big advantage of using the hosted jQuery from Google or Microsoft:

Many users already have downloaded jQuery from Google or Microsoft when visiting another site. As a result, it will be loaded from cache when they visit your site, which leads to faster loading time. Also, most CDN's will make sure that once a user requests a file from it, it will be served from the server closest to them, which also leads to faster loading time.

# jQuery Syntax

With jQuery you select (query) HTML elements and perform "actions" on them.

## jQuery Syntax

The jQuery syntax is tailor-made for selecting HTML elements and performing some action on the element(s).

Basic syntax is: **\$(selector).action()**

- A \$ sign to define/access jQuery
- A _(selector)_ to "query (or find)" HTML elements
- A jQuery _action()_ to be performed on the element(s)

Examples:

`$(this).hide()`-hides the current element.

`$("p").hide()`- hides all `<p>` elements.

`$(".test").hide()`- hides all elements with class="test".

`$("#test").hide()` - hides the element with id="test".

### Are you familiar with CSS selectors?

jQuery uses CSS syntax to select elements. You will learn more about the selector syntax in the next chapter of this tutorial.

## The Document Ready Event

You might have noticed that all jQuery methods in our examples, are inside a document ready event:

```javascript
$(document).ready(function() {
  // jQuery methods go here...
});
```

This is to prevent any jQuery code from running before the document is finished loading (is ready).

It is good practice to wait for the document to be fully loaded and ready before working with it. This also allows you to have your JavaScript code before the body of your document, in the head section.

Here are some examples of actions that can fail if methods are run before the document is fully loaded:

- Trying to hide an element that is not created yet
- Trying to get the size of an image that is not loaded yet

**Tip:** The jQuery team has also created an even shorter method for the document ready event:

```javascript
$(function() {
  // jQuery methods go here...
});
```

Use the syntax you prefer. We think that the document ready event is easier to understand when reading the code.

# jQuery Selectors

jQuery selectors are one of the most important parts of the jQuery library.

## jQuery Selectors

jQuery selectors allow you to select and manipulate HTML element(s).

jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more. It's based on the existing CSS Selectors, and in addition, it has some own custom selectors.

All selectors in jQuery start with the dollar sign and parentheses: \$().

## The element Selector

The jQuery element selector selects elements based on the element name.

You can select all `<p>` elements on a page like this:

```javascript
$('p');
```

Example
When a user clicks on a button, all `<p>` elements will be hidden:

```javascript
$(document).ready(function() {
  $('button').click(function() {
    $('p').hide();
  });
});
```