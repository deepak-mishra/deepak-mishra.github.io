layout: post
title: "CSS Snippets"
description: "Web design"
category : css
tagline: "CSS Snippets"
tags : [css, tutorial]


{% include JB/setup %}


##Clearfix

A while back, someone decided it was time to clear floated elements without adding any extra markup to the document. They did this by creating a class that can be applied to the container of floated children to clear it. A fantastic way to do so, and something that is nowadays, widely used.


	.clearfix { display: inline-block; }

	.clearfix:after {
	  visibility: hidden;
		display: block;
		font-size: 0;
		content: " ";
		clear: both;
		height: 0;
	}

	/* start commented backslash hack \*/
	* html .clearfix { height: 1%; }
	.clearfix { display: block; }
	/* close commented backslash hack */

## Fixing button element padding in IE

IE 6 and 7 adds extra padding to the text in button elements.

	button {width:auto; overflow:visible;}
	
## Remove textarea scrollbar in IE

Internet Explorer adds a scrollbars to textarea even when the textarea's content is not overflowing. This snippet rectifies this flaw.

	textarea{
		overflow:auto;
	}
## Multiple Background Images

Multiple background images can be a useful feature if you want to put some pictures in a background in different positions. Separate it using a comma with the standard background property.


	#multiple-images {
	   background: url(image_1.png) top left no-repeat,
	   url(image_2.png) bottom left no-repeat,
	   url(image_3.png) bottom right no-repeat;
	}
## Min-height in IE

Microsoft IE’s does not have the capability of handling min-height. In essence, IE interprets height as min-height, so since IE wont implement the auto height, this snippet will fix all this for us (using !important).


	.box {
	   min-height:500px;
	   height:auto !important;
	   height:500px;
	}
	
## Vertical Center

This snippet allows to vertically center the contents of a container without any extra markup by simply displaying it as a table cell. This allows you to use the vertical-align attribute.


	.container {
	   min-height: 10em;
	   display: table-cell;
	   vertical-align: middle;
	}
## Highlight Text Selection

Probably you are unaware that it is possible to change the color of the highlight text in your browser. It is so easy to use and also risky! Just be careful using this two selectors that you don’t ruin your site with it.


	::selection {
	   color: #000000;
	   background-color: #FF0000;
	}

	::-moz-selection {
	   color: #000000;
	   background: #FF0000;
	}
	
Reference URL:- 
<a href="#">http://www.djavupixel.com/development/css-development/master-css3-ultimate-css-code-snippets/</a>
