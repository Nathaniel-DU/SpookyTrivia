# SpookyTrivia
SpookyTrivia

About
This is a simple trivia game, have fun, get spooked!

Demo
https://nathaniel-du.github.io/SpookyTrivia/

Requirements

function start(){
	
	$("#start").attr("disabled", true);
	$("#allQuestions").css("display", "block");
	countDown = setInterval(decrement, 1000);

}

function decrement(){
	number--;

	$("#time").text(number);

	if(number <= 0){
		stop();
		alert("JASON GOT YOU AND YOU ARE NOW DEAD!");
		
		$("#start").attr("disabled", false);

Here is my game start and countdown functions, along with my alert if countdown hits zero. 

function submit(){
	
	$("#answers").css("display", "block");
	stop();
	 
	var trueRadios = $("input:radio[value=true]:checked");
		console.log(trueRadios);
		trueRadios = trueRadios.length;
		$("#correctAnswers").html(trueRadios);
		
	var falseRadios = $("input:radio[value=false]:checked"); 
		console.log(falseRadios);
		falseRadios = falseRadios.length;
		$("#incorrectAnswers").html(falseRadios);

	var unansweredCount = 0; 
	for (var i = 1; i <= 10; i++){ 
		var unanswered = $("input:radio[name=q" + i + "]");	 
		for (var j = 0; j < unanswered.length; j++) { 
			if (unanswered[j].checked) {  
				break; 
			} else if (j === unanswered.length - 1){ 
				unansweredCount++; 
			}
		}
		$("#unansweredQuestions").html(unansweredCount);

This is my true/false radio fuction and html display.        

Technologies used:

Javascript
jQuery
