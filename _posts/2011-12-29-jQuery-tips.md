---
layout: post
category : javascript
tagline: "jQuery tips"
tags : [jQuery, tutorial]
---
{% include JB/setup %}
## Check if jQuery is Loaded

	if (typeof jQuery == 'undefined') {
		// do stuff here.
	}

## Keep your Code Safe
### NoConflict

	var j = jQuery.noConflict();  
	
	// Now, instead of $, we use j. 
	j('#someDiv').hide();  
	
	// The line below will reference some other library's $ function.  
	$('someDiv').style.display = 'none';  


###Passing jQuery

	(function($) {  
		// Within this function, $ will always refer to jQuery  
	})(jQuery);  

## Passing $ via the Ready Method

	jQuery(document).ready(function($) {  
	 // $ refers to jQuery  
	});  
	// $ is either undefined, or refers to some other library's function. 

## Checking types
Few methods for determining the type of a specific value.


	var myValue = [1, 2, 3];
	// Using JavaScript's typeof operator to test for primative types
	typeof myValue == 'string'; // false
	typeof myValue == 'number'; // false
	typeof myValue == 'undefined'; // false
	typeof myValue == 'boolean'; // false

	// Using strict equality operator to check for null
	myValue === null; // false

	// Using jQuery's methods to check for non-primative types
	jQuery.isFunction(myValue); // false
	jQuery.isPlainObject(myValue); // false
	jQuery.isArray(myValue); // true


## Check if Element Exists


	if ($("#myElement").length) {
	  // it exists 
	}


## Test if something is hidden using jQuery
We use .hide(), .show() methods in jquery to change the visibility of an element. Use following code to check the whether an element is visible or not.


	if($(element).is(":visible") == "true") {
		   //The element is Visible
	}


##Binding Multiple Events


	$('p').bind({
	  'click': function() { console.log('clicked!'); },
	  'mouseover': function() { console.log('hovered!'); }
	});



##Selecting Child Elements Only


	jQuery('#nav li > a');


##Use $.data Instead of $.fn.data


	// regular
	$(elem).data(key,value);

	// 10x faster
	$.data(elem,key,value);


## Check the Index


	var index =  $('#ul>li').index( liDomObject );
	$("ul > li").click(function ()
	{
		var index = $(this).prevAll().length;
	});


## Creating New Elements


	var newDiv = $('<div></div>');
	newDiv.attr("id","myNewDiv").appendTo("body");

## Which mouse button clicked using jQuery


$(document).ready(function() {
	$('#btnClick').mousedown(function(event){
		switch (event.which) {
			case 1:
				alert('Left mouse button pressed');
				break;
			case 2:
				alert('Middle mouse button pressed');
				break;
			case 3:
				alert('Right mouse button pressed');
				break;
			default:
			   break;
		}
	});
});


##	Disable Cut, Copy and Paste function using jQuery


	$(document).ready(function(){
	  $('#txtInput').bind("cut copy paste",function(e) {
		  e.preventDefault();
	  });
	});
