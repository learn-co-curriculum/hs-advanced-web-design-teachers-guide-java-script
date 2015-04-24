###SWABATs 

+ Review:
	+ declare JavaScript variables and constants
	+ perform math with JS
	+ understand JS datatypes
	+ understand datatype conversion and why/when to use it
	+ utilize string methods
	+ use different types of dialogue boxes like alerts and display text in the console
	+ understand comparison and logic operators
	+ use conditional statements to control program flow (if/else and switch)

+ New material:
	+ declare JS functions with and without parameters
	+ call JS functions with and without passing arguments
	+ understand the concept of a return value
	+ understand local and global variable scope
	+ understand when to use semicolons with functions

###Motivation
You guys have all of the basics for creating fantastic, responsive web designs and you had a little taste of how JavaScript and jQuery can be used to make websites even more dynamic. In this class we’re going to dive much deeper in JS so that you can create full scale dynamic web applications! To make sure we’re all ready to go deep into JS we’re going to do a little review of JS fundamentals - datatypes, data structures and program flow - and then launch into building JS functions - which are the real building bricks behind building programs with JS. Let the programming begin!

###Lesson Plan
+ Let’s go over some basics real quick. <b>(Open up a JSfiddle and to demo this material for the class as you review.)</b>
+ <u>Variables</u>
	+ <b>What is a variable and how do we use them?</b>
	+ A variable is like a bucket that we can store some data inside and then later change the data it stores.
	+ You need to declare variables explicitly in JavaScript with the var keyword like this:
		+ var x; 
		+ //var is a keyword that declares a variable
	+ Naming variables: start with letter a-z A-Z remaining 0-9 a-z A-Z, you can also use _ never use spaces ' ' or or illegal characters (! % ?)
	+ For variable names consisting of multiple words you should use camelCase or snake_case (camelCase is generally what JS developers use by convention)
+ <b>What are the types of values that I can store inside of variables?</b>
+ <u>JavaScript data types:</u>
	+ Numbers: integers (whole numbers) like 2, floats (decimals) like 3.56789
	+ Strings: (text) like 'hello' or "hello"
	+ Boolean: true or false
	+ null (empty)
	+ undefined (not yet defined)
+ <u>Checking the data type:</u>
	+ `typeof` is a keyword that allows us to check the data type.
+ <u>Data Conversion</u>
+ <b>Why would we want to convert from one datatype to another?</b>
	+ This is most relevant when we are trying to do math. If we want to do math with the string ‘10’ we’ll need to convert it to a number first with parseInt(‘10’)
	+ combineStuff = parseInt('10') + 5;
	+ //parseInt changes a string to a whole number.
	+ combineStuff; //prints 15

	+ //what the heck happens if I try converting text to a number?
	+ var userName = parseInt('bob'); //returns NaN
	+ //NaN stands for Not a Number!
	+ What if I want to convert to a floating number instead of an integer? What is a float?

	+ var gallonsGas = parseFloat('10.25');
	+ gallonsGas; //reports 10.25 as number

	+ //parseInt stops as whole number and ignores characters that are not numbers. 10xffffff same as 10.12345 becomes 10. Where as parseFloat maintains decimal values. 
+ <b>What is concatenation?</b>
	+ JavaScript uses + symbol for math when surrounded by numbers, but when any content is a string, it will concatenate the text. This can produce unexpected results unless we are careful how we use + symbol. It’s always a good idea to be aware what data types are involved.
		+ var combineStuff = '10' + 5; //string concatenation	
		+ 'Adding a string to a number does this: '+combineStuff+' weird! ';
		+ This prints 105 weird!
+ <b>What are some string methods that we can use?</b>
	+ String methods can be called on a string to modify the string in some way. Usually you can figure out what a method is going to do just based on its name. Some examples:
	+ //toUpperCase
	+ "Foobar”.toUpperCase(); //returns "FOOBAR"

	+ //toLowerCase
	+ "Foobar".toLowerCase(); //returns "foobar"

	+ //replace
	+ "Foobar".replace("bar", "baz"); //returns "Foobaz"
	+ "Foobar".replace(/o/g, "x"); //returns "Fxxbar"

	+ //method chaining
	+ "Foobar".replace(/o/g, "x").toUpperCase(); //returns "FXXBAR"
+ <u>Dialog Boxes and JS Console</u>
	+ //alert
	+ alert('warning do not attempt to cook food using this website!');

	+ //confirm
	+ var delete = confirm('Are you sure you want to delete this?'); //true or false

	+ //prompt
	+ var age = prompt('Please enter your age: '); //captures the value inserted.

	+ //log
	+ console.log(age); //reports the age they entered into the JS Console located in the developer too window.
+ <u>Doing math with JavaScript.</u>
+ <b>What kind of operations can we perform with JavaScript?</b> 
	+ all the standard one -,+,*,/
	+ we can also use modulus % to find the remainder
	+ and ++ to increment and -- to decrement
+ Some other useful shorthand operators
	+ shortcut		original
	+ x += y			x = x + y
	+ x -= y			x = x - y
	+ x *= y			x = x * y
	+ x /= y			x = x / y
	+ x %= y			x = x % y
+ <b>Let’s practice this with a little mini-lab.</b>
	+ Everyone open up Sublime Text and create a new file called senior.js. 
	+ We’re going to build a little Senior Citizen calculator.
	+ Being a senior citizen is awesome - you get to retire and get all those sweet senior citizen discounts. You don’t officially become a senior citizen until you are 64 years old though.
	+ Write a little program that prompts a user for their age and then alerts them to how many years they have left until they reach retirement - age 64. 
	+ <b>When you are ready to test your code go to JSfiddle.net and paste your code in the JavaScript box and press run.</b>
+ <u>Conditional Statements</u>
	+ <b>What are conditional statements and why would we want to use them?</b>
	+ We use the if statement to execute a statement if a logical condition is true. Use the optional else clause to execute a statement if the condition is false. An if statement looks as follows:
		+ if (condition)
		  + statement_1
		+ else
		  + statement_2
	+ JS requires that the conditions in your if statement be surrounded by ()
	+ You’ll need to encapsulate your conditional statement with {}
	+ (almost) every line of JS ends with a ;
	+ We have to use that funny looking triple equals for comparision. This is how we compare the values of two things. One equal to assign value, triple equals to compare values.
	+ Here is a list of all of JS comparison values and what they do
	+ COMPARISON Operators
<img src= "https://s3.amazonaws.com/after-school-assets/java_script.png">
	+ You can add additional branches to your if statement with else if. 
	+ <b>Let’s practice. Everyone go to Sublime Text and create a new doc called gastank.js.</b>
	+ <b>You are designing a car with a gas tank alert. This is what your program should do:</b>
		+ Prompt the user for how many gallons are in their gas tank.
		+ If they say 20 then alert that the tank is full
		+ If they say more than 20 alert that the tank is overfilled
		+ Otherwise tell them to refill their tank 
		+ <b>When you are ready to test your code go to JSfiddle.net and paste your code in the JavaScript box and press run.</b>
	+ Before we move on let’s go over one more piece of conditionals
	+ We can make more complex conditional statements with logical operators, like this:
	+ Here is a list of all the Logical Operators and what they do:
<img src= "https://s3.amazonaws.com/after-school-assets/java_script2.png">
	+ Let’s say we want to make our alert system a little smarter and add one more else if.
	+ If the user says that the tank has less than 20 gallons but more than 5 we will alert that a refill is suggested else we’ll say a refill is mandatory.
	+ <b>Walk me through how to do this.</b>
+ Now that we’re getting comfortable with the basics of JS we’re going to move on to JS functions.
+ A JS function is essentially a set of instructions that we write out and can reuse over and over again.
+ (Pick a kid in the class to call on). Joe - I want you to close your computer, stand up and walk out the door.
+ Jk, come back. These essentially are the steps that Joe would follow if he was getting ready to head out to lunch.
+ Computers need explicit step by step instructions like this because they cannot infer what you mean when you say something like go get lunch.
+ But we can essentially teach the computer what go get lunch means by wrapping up these instructions in a function called goGetLunch.
+ Let’s create a goGetLunch function in JSfiddle.
+ The syntax for writing JS functions is very specific. It looks like this:
	+ function goGetLunch() {
	+ };
+ The instructions go inside this function. Let’s alert each of the steps inside of our function and try running the program.
+ Nothing happened. Why is that? We declared our function - which is like adding the goGetLunch function to the computer’s dictionary - but we didn’t actually tell the computer to execute the function.
+ We need call a function like this goGetLunch(); to make it run.
+ This is the equivalent of telling the computer - do those steps in the goGetLunch function. Test it out.
+ What’s up with those parentheses? Those are like a placeholder for something called an argument. 
+ Our instructions are pretty generic right now. What if we wanted to direct them towards a specific student? Like adding a step that says “hey, Joe”.
	+ function goGetLunch(student) {
	   + alert('hey, '+student);
	    + alert('close your computer');
	    + alert('stand up');
	    + alert('walk out the door');
	+ }
+ We can reuse this function and just change the name of the student we address by adding a student argument.
+ Then we can call it like this:
	+ goGetLunch("Joe");
	+ goGetLunch("Jill");
	+ goGetLunch("Josie");
+ There is one more VERY IMPORTANT thing about functions - return values.
+ We are going to get some help explaining this concept from Cheddar the mouse.
+ https://docs.google.com/a/flatironschool.com/presentation/d/1USGrpdEBhsYdP4b8LpVTabOHzMVKDLb0ZXen0Un3MPA/edit#slide=id.gacf625b88_0_11
+ A function is kind of like placing a mouse in a box and that mouse will only perform the actions he was trained to do whenever you tell him to do a certain action.
+ Here is Cheddar in his box. We’ve trained him to doMath (addition really) with two variables x and y.
+ function doMath(x,y){
	+ return x+y;
	+ }
+ Notice there is a return statement. We need to include return in order to get something back from the function. In essence if we left of the return statement Cheddar might perform the math in his head but not give us the answer. By saying return we’re telling the function give us back the answer.
+ This is important because most of the time functions don’t live all alone by themselves they rely on other functions - so getting something back is very important. Don’t forget the return! 
+ So functions are pretty cool, huh? From now on ALL of your code should be wrapped in functions. 
+ Let’s get some practice with a lab. Everyone go to Learn.co and fork and clone the Teenager.js lab.
+ From now on we’ll be working on labs that have built in tests to tell you whether or not your code is correct.
+ Testing is an important part of building and maintaining applications. Automated testing is <u>essential</u> for large scale programs like Facebook and Twitter.
	+ When you have a very simple application it’s easy to test it by just running it - like we’ve been doing with JSfiddle.
	+ If you have a really large complex application it would take a ton of time for someone to manually go through thousands of lines of code and check every piece of the application.
	+ So instead we write tests - essentially code to test our code.
+ Let’s dive right in.
+ We’ll be using a JS library called Jasmine to test our code. And you can find all the tests in the spec folder. Spec is short for specifications - as in we expect this program to run according to these specifications. Let’s take a look at isTeenager.spec.js.
+ The first thing you see at the top of the page is ‘use strict’ which just means that the spec should follow the conventions of the latest version of JS (ECMA script 5).
+ The next word is describe - as in the following will describe what the isTeenager function should do.
+ There are several different specs that are being tested inside of this describe block:
	+ it tells you what the test is expecting to get back
	+ expect is where Jasmine is actually going to call the function
	+ .toBe is where Jasmine states what it expects will happen when that function is called
	+ <b>Can anyone walk me through this in their own words?</b>
+ Now let’s take a look at isTeenager.js. We’ve already gotten you started by declaring the function. Now you just have to fill it in. Give it a shot!
+ To test run “learn -b” in your terminal. You’ll see the tests run in your terminal and also in your browser. The browser will probably be more helpful.
+ We have one more lab for you guys to practice flow control. One thing I want to point out about this lab - if you take a look at fizzbuzz.js the function is declared in a slightly different way. 
+ This style of declaring a function is called function expression instead of a function declaration. We’re going to stick with function declarations but other people use this style so it’s good for you to know that it exists. Take a look at the README and spec and then give this lab a shot.
+ There are a few more things that you need to know about functions.
+ One is called hoisting. JavaScript tries to be helpful and it will go through a function and look for all of your variables before it runs the function. This seems like a good thing because if you try to use a variable x at the top of your function (before you declare it like this - var x) JS will be like - oh ok, I know there is a variable x in here somewhere. BUT it’s not really that helpful because JS will only know that the variable exists. So if you declare var x = 10 somewhere lower down in the function it will know that var x exists but it will not know that you set the variable x equal to 10. 
+ This is really just a roundabout way to tell you DECLARE ALL OF YOUR VARIABLES AT THE TOP OF A FUNCTION. It’s best practice and it will help you avoid complications later. DECLARE YOUR VARIABLES AT THE TOP OF YOUR FUNCTION.
+ Another thing that is important to understand about JS functions is variable scope. 
	+ When you declare a variable outside of a function it will also be available inside of the function. For example (open up the console in Chrome and paste this in):
	+ var milkType = "whole milk";
	+ function isWholeMilk() {
	      + if (milkType === "whole milk”) {
	          + return true;
	      + } else {
	         + return false;         
	      + }
	+ }
	+ If I run isWholeMilk(); we’ll get back true. The function isWholeMilk has access to the variable milkType that was declared outside of the function.
	+ BUT if you declare a variable inside of a function it will only be available inside of the function.
	+ Here is an example:
	+ function milkTheCow() {	
	      + var bessyCow = 'milked'; //local var
	      + return bessyCow;
	+ }
	+ If we type bessyCow we’ll get back undefined. We are trying to access bessyCow from outside of the function and she only exists inside of the function.
	+ The only way you can get access to bessyCow is if you run the function. Then bessyCow will be returned - like when Cheddar tossed out the answer to those math equations - and we’ll be able to see the value that way.
	+ One last brain teaser for you guys. 
	+ var tiger = 2,
	      + lion = 3; \\we can declare two variables at the same time like this
		
	+ function countAnimals(giraffe) {
	      + tiger = tiger - 1;
	      + var total = lion + tiger + giraffe;
	      + return total;	
	+ }
	+ What will the total equal (what value will be returned when I run countAnimals(3);
+ Variable scope - and not being able to access variables outside of a function - seems annoying but it’s really important and helpful because you will know exactly what your variable is equal to - it can only be set from within your function so it can only be equal to the value that you set within your function.
Every head to Learn.co and fork and clone LAB I NEED TO CREATE for more practice. 
