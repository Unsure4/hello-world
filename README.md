<!DOCTYPE html>

<head>
<script src="/assets/jquery.js"></script>
<style>
</style>
</head>

<body>
<div class="prompt"></div>
<button>Next</button>
<script>
// List of prompts for the user
var prompts = [
	'Type your name',
	'Type an adjective',
	'Type a noun'
   ];

// Keep track of current prompt we're on
var currentPrompt = 0;

// A function that will call the next prompt
var nextPrompt = function() {
	// if there is a next prompt
	if (currentPrompt < prompts.length) {
		// put first prompt in all html elements with class 
		$('.prompt').html(prompts[currentPrompt]);
		// move the next prompt into variable currentPrompt 
		currentPrompt = currentPrompt + 1;
	}
	//or else if were at the end of the array
	else {
		// put a new message into the html.
		$('.prompt').html("that's all for now!");
	}
}

// run nextPrompt function when button is clicked
$('button').click(function() {
	nextPrompt();
});

// Show the first prompt as soon as js loads
nextPrompt();
</script>

</body>
