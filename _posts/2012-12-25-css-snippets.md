---
layout: post
title: "CSS Snippets"
description: "Web design"
category : css
tagline: "CSS Snippets"
tags : [css, tutorial]
---

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

