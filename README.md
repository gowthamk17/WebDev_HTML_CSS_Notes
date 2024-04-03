# HTML

## Overview of HTML
+ An html element started and closed with same valid html keyword and surrounded by anckle brackets, it may contain other elements inside them
+ Unclosed elements are closed automatically but not recommended
+ Html attributes the included in the starting tag with space between them
    + they have either key/value format or only name which is a boolean format
+ html has default appearance for the the user-agent (browser)
+ html tags have semantic value in them
+ DOM is the object representation of the html document in the page
+ All html objects in the dom are inherit from HTMLElement class also some specific tag's have their own class inherited from HTMLElement class like HTMLImageElement

## Document Structure
+ All webpages are enclosed with `<html>` which if not exist will be added automatically
+ it has two childs `<head>` and `<body>`. body is the one we can see on screens, head contain meta information about the web page
+ `<!DOCTYPE html>` not and html element but a special kind of node. this means the web page should be rendered as modern html content.
+ lang attribute to html element tells the browser which language is the content
+ Components in head tag
    + Charecter ecoding should be the first chlid of head with value utf-8
    + title tag with name of the page
    + viewport meta data how much width of the site should be considered usually device width
    + links to the css files
    + link tag with rel icon to add favicon to the page
    + script tag to add js scripts

## Metadata
+ "refresh" - `<meta http-equiv="refresh" content="60; https://example.com/timeout />` to refresh the page for every 1 mins
+ "CSP" - `<meta http-equiv="content-security-policy" content="default-src https:" />` 
+ "robots" - `<meta name="robots" content="index, allow" />`
+ "theme-color" - `<meta name="theme-color" content="#226DAA" />` set background color for page before rendering html
+ "open-graph" with property for sharing page to social media
+ "manifest" - `<link rel="manifest" href="/mlw.webmanifest" />` adding pwa configurations

## Semantic HTML
+ using semantic html ensure accessibility for the user
+ role attribute helps to add semantic to an element

## Headings and Sections
+ `<header>` - when added to the top level considered as banner in nested level considered as local header good for accessibility
+ `<footer>` - same as header
+ `<main>` - main content of the page, there should be only one main content per page
+ `<aside>` - mostly contains details realted to the main
+ `<article>` - representing a section of self contained content
+ `<section>` - indicating a region on page
+ Heading `<h1> - <h6>` - inside body top h1 incates header for page inside section or article it will incate title for that section

## Attributes
+ Attributes can be modified in the elements object
+ `id` - unique to the document, serve as identifier for the html element
    + link poiting to a id will make the element visible in the page
    + for css identifier => `[id="idName"]`
    + labels for attribute points to an for element with the given id
+ `class` - for adding styles
+ `style` - adding style in inline
+ `tabindex` - making an element focus by clicking tab
+ `role` - for screen readers
+ `contenteditable` - for making an element editable, focusable, default index to 0
+ `data-` - for adding custom attributes 

## Text Basics
+ `aria-labelledby` - to make a section as a landmarked region for screen readers
+ `<p>` - for normal paragraphs
+ `blockquote` - for quotes does not add quotation
+ `q` - adds quotation
    + `cite` - attribute for citations
+ HTML entities such as &lt; &gt; for avoiding conflict with html'

## Links
+ `href` - attribute indicating the following link
+ `download` - attribute for indicating the file name for the href pointed content
+ `ping` - attribute for tracking link clicks
+ links property in document element contains all the links in the doucment as HTMLCollection

## Lists
+ `<ul>` - parent of unorderedlist
+ `<ol>` - parent of orderedlist
+ `reversed` - an attribute for reversing orderedlist
+ `list-style-type` - an attribute for changing list style type
+ `<li>` - list element child of the above parent elements
+ `<dl>` - definition list condtaining
    + `<dt>` - definition term
    + `<dd>` - definition description

## Navigation
+ "skip to content link" - add main id to main element
+ Table of contents
+ Breadcrums
+ Local Navigation with id's
+ Global Navigation

## Table
+ `<table>` - parent table element
+ `<caption>` - caption for the table
+ Data sectioning
    + `<thead>`
    + `<tbody>`
    + `<tfoot>`
+ Table Content
    + `<tr>` - table row element
    + `<th>` - table head element child of table row
    + `<td>` - table data child of row element
+ Merging cells with rowspan and colspan

## Forms
+ when submitting data alwasy use POST
+ radio buttons should have unique name and value property
+ provide for for labels or insert input elements into the label tag
+ use accept attribute to control the upload file type
+ use pattern attribute to get the correct type of input

## Images
+ use srcset for alternative version of image for different screen size
+ the above can also done with picture element with source element
+ add height and width to reduce layout shifting when loading image
+ add loading attribute to change img loading behavirous (set to lazy)

## Audio && Video
+ the poster attribute is for showing till video start playing
+ track tag for adding subtitle

## Template 
+ template element stored in dom but not displayed we can clone it later and add it to dom
+ slott attribute replace element within template when cloning
+ using style inside templete only applies to that template

# CSS

## Box Model
+ content box -> padding -> border -> margin

## Selector
+ `tag tag:first-of-type` - to select first type of element
+ `*` - universal selector, selects every element
+ `typeName` - type selector example `p`
+ `.className` - class selector
+ `#id` - id selector
+ `[attribute=value]` - attribute selector
+ `:` - to access pseudo class like hover
+ `::` - to ccess pseudo element
+ use space to select childs like `parentselector childselector`
+ `+` - for selecting next sibling
+ `>` - only direct child

## Inherit
+ use property name and inherit value to implicitly inherit it

## Colors
+ hex colors: `#ffffff`
+ rgb colors: `rgb(x, x, x)`
+ hsl colors: `hsl(x, x, x)`
+ keywords : `blue`