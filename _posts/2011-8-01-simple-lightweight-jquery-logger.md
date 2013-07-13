---
layout: post
title: "Simple, Lightweight, jQuery logger"
description: "Web design"
category : jQuery
tagline: "jQuery logger"
tags : [jQuery, tutorial]
---

{% include JB/setup %}

## Simple, Lightweight, jQuery logger .

###Installation

Copy below code and put in your jQuery based project

	;(function($){  
		function log(debugtext) {
			if ( $('#logger').length == 0 ){ 
				var $logger = '<div id=\'logger\' style=\'position: absolute;bottom:10px;right: 12px;width:25%;height:150px;overflow: auto; background:rgba(0, 0, 0, 0.5); padding:10px; color:#fff; opacity:0.8; \'></div>';
				$('body').append($logger); 
				$('#logger').prepend(navigator.userAgent);
			}
			if (log && typeof (window['console']) != "undefined") { 
				jQuery.error = console.error; console.log(debugtext);
			}
			$('#logger').append('<p style=\'font-size:13px;padding:2px;border-bottom: 1px solid #ccc;margin: 0;\'>'+debugtext+'</p>').scrollTop(999999);
			$('#logger p:nth-child(even)').css('background-color','#FFFFE8');
		}
		this.log = log; 
	})(jQuery);

OR

Add this script tag to your page

	<p><script src="https://raw.github.com/deepak-mishra/dee/master/logger.js"></script></p>

## Usage

	$('#test').click( function(){ log('me') }); 

