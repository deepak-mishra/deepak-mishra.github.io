---
layout: post
title: "Browser CSS hacks"
description: "Web design"
category : css
tagline: "CSS Snippets"
tags : [css, tutorial]
---

{% include JB/setup %}

## Browser CSS hacks
### Selector Hacks - IE
IE6 and below

	* html #uno { color: red }

IE7

	*:first-child+html #dos { color: red }

IE7, FF, safari, Opera

	html>body #tres { color: red }

IE8, FF, safari, Opera (Everything but IE 6,7)

	html>/**/body #cuatro { color: red }

IE7

	*+html #dieciocho { color: red }

### Attribute Hacks - IE
IE6, IE7

	#once { _color: blue } #doce { *color: blue;} 

IE6, IE7 — acts as an !important

	#veintesiete { color: blue !ie; } /* string after ! can be anything */

Everything but IE6

	#diecisiete { color/**/: blue }

IE6, IE7, IE8, but also IE9 in some cases

	#diecinueve { color: blue\9; }

IE7, IE8

	#veinte { color/*\**/: blue\9; }

IE8, IE9

	#anotherone {color: blue\0/;} /* must go at the END of all rules */

Everything but IE6-8

	:root *> #quince { color: red }

### @media rule hacks - IE
IE 6 , IE 7

	@media screen\9 { 
	 body { background: red; } 
	} 

IE 6, 7, 8

	@media \0screen\,screen\9 { 
	 body { background: green; } 
	} 

IE 8

	@media \0screen { 
		body { background: blue; }
	} 

IE8, IE9, IE10

	@media screen\0 { 
	 body { background: orange; } 
	} 

IE9, IE10

	@media screen and (min-width:0\0) { 
	 #veintidos { color: red}
	} 

IE 10+

	@media screen and (-ms-high-contrast: active), (-ms-high-contrast: none) { 
	 #veintiun { color: red; } 
	} 

### IE 10 using JS

	if(Function('/*@cc_on return document.documentMode===10@*/')()){ document.documentElement.className+=' ie10' }

### Safari & Chrome, Opera
safari3+, chrome1+

	@media screen and (-webkit-min-device-pixel-ratio:0) { 
	 #diez{ color: red } 
	} 

safari 3+, chrome 1+, opera9+, ff 3.5+

	body:nth-of-type(1) #siete { color: red }

safari 3+, chrome 1+, opera9+, ff 3.5+

	body:first-of-type #ocho { color: red }

Safari 2 - 3.1

	html[xmlns*=""]:root #trece { color: red }

Safari 2-3

	html[xmlns*=""] body:last-child #seis { color: red }

Safari 2 - 3.1, Opera 9.25

	*|html[xmlns*=""] #catorce { color: red }

Opera 9.27 and below, safari 2

	html:first-child #cinco { color: red }

Mozila FF 3.5+

	body:not(:-moz-handler-blocked) #cuarenta { color: red; }

Mobile - iPhone / mobile webkit

	@media screen and (max-device-width: 480px) { 
	 #veintiseis { color: red } 
	} 

Reference URL:-

<p><a href="#">http://msdn.microsoft.com/en-us/library/ms537512.aspx/</a></p>

<p><a href="#">http://paulirish.com/2009/browser-specific-css-hacks/</a></p>

<p><a href="#">http://blog.keithclark.co.uk/moving-ie-specific-css-into-media-blocks/</a></p>
