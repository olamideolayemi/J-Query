How to incomporate jquery into our website:
Use google CDN

selecting of an element with jquery:
document.querySelector("h1");
instead we use the dollar sign
$("h1");

same works for the document.querySelectorAll("h1");
replaced with $("h1");

Manipulating the css style
$("h1").css("color", "green");

$("h1").addClass("big-title");
$("h1").removeClass("big-title");

// To add or remove multiple classes
$("h1").addClass("big-title margin-50");
// To check if the element has a class
$("h1").hasClass("big-title");

// Change the text of an element using jquery
$("h1").text("Hello");

$("h1").html("<em>Hello</em>");

// Manipulate attributes using Jquery
$("img").attr("src"); - get the attribute
$("a").attr("href", "https://yahoo.com"); - set the value of the attribute

// Add eventListeners to HTML elements using Jquery
$("h1").click(function() {
	$("h1").css("color", "red"); 
});
------------------------------------------
$("button").click(function() {
	$("h1").css("color", "purple"); 
}); 

// We could bined a keypress 
$("document").keypress(function(event) {
	console.log(event.key);
}); 
for example we want to change the h1 element to whatever button is pressed
$("document").keypress(function(event) {
	$("h1").text(event.key);
}); 
another way to add an event listener is using the on param
$("document").on("keypress", function(event) {
	console.log(event.key);
}); 


// Add an element before or after an element in html using Jquery
for example we have an already existing h1 element and we need to add a button right above it
$("h1").before(<button>New</button>)
// same syntax goes for the after which adds immediately after the h1 element
$("h1").after(<button>New</button>)
Other methods to add elements include:
append & prepend 

// Add animation 
$("h1").slideToggle();
$("h1").slideToggle.slideDown.animate({opacity: 0.5});
$("h1").animate({opacity: 0.5});