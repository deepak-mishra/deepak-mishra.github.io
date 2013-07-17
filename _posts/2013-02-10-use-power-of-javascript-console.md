---
layout: post
title: "Use power of  javascript Console"
description: "javaScript"
category : javaScript
tagline: "Console.log"
tags : [css, tutorial]
---

{% include JB/setup %}

	console.dir(object);
	
Displays an interactive listing of the properties of a specified JavaScript object. This listing lets you use disclosure triangles to examine the contents of child objects.
	
	console.warn();
Outputs a warning message
	
	console.info();
	
Informative logging information
	
	console.error();
	
Outputs an error message

	console.time();
	
Starts a timer with a name specified as an input parameter. Up to 10,000 simultaneous timers can run on a given page.
	
	console.timeEnd();
	
Stops the specified timer and logs the elapsed time in seconds since its start. See Timers.
	
	console.timeStamp();
	
See Time stamp

	console.trace(); 
	
Outputs a stack trace

	$0 
	
References the object selected in the elements tab

	$$
	
Convenience wrapper around document.querySelectorAll.appl­y(document, arguments)

	monitor(el);
	
monitors all events on a dom element

	monitor(el, 'key|mouse'); 
	
monitors key or mouse events on a dom element

	monitor(myFunction); 
	unmonitor(myFunction)
	
monitors fuction or mouse events on a dom element; 

	debug(fn) and undebug(fu) 
	
Debug function 

	inspect(object[,tabName])
	
Insepect element 

	keys(obj)
	
shows all the keys of an object

	values(obj)
	
shows all the values of an object

	copy(obj)

copies to your clipboard
