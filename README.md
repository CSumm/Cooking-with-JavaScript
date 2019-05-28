# Cooking-with-JavaScript
We're here to learn JavaScript, but in a fun way. Most of the time, things get too theoretical and you're left scratching your head and feeling like giving up. It doesn't need to be that way. Today, we're going to make an omelette recipe in JavaScript.

Ok first things first, here's the recipe we're going to use: https://www.incredibleegg.org/recipe/basic-french-omelet/

Nothing too fancy, just a basic omelette.

The first thing is to get our ingredients prepped. We need 2 eggs, 2tbps. of water, 1/8 tsp. of salt, a dash of pepper, 1 tsp of butter, and 1/3 cup of filling (anything we want :P);

So, let's break our ingredients into their own containers, or in this case variables.

We know we need two eggs. So we would write it like this in JavaScript:

```var eggs = 2;```

Alright, next is water. We have to do some math here since we're going to convert tablespoons to cups. A half cup is 8 tablespoons, so 2 tablespoons is 1/2 or 0.5/2...which is...um...0.25 cups, so 1/4. Let's store this in a variable too!

```var water = 0.25;```

Next is salt. We're just going to use it's actual amount in a string, which is text:

```var salt = "1/8 tsp;```

Next, we have a dash of pepper. Since there's no number attach to it, we're going to write some arbitrary text to say it's a dash

```var pepper = "a dash";```

Cool! 1 tsp of butter. Using my trusty power of Google searching, we find out it's translated into 0.02 cups

 ```var butter = 0.02;```
 
 Alright here comes the fun ingredients! I'll just throw in my favs, but you can throw in whatever you would like:
 
 ```var mushrooms = 4;
 var onion = 1;
 var garlic = 3;
 var cheese = "YES!"
 ```
 
 Before we go any further into cooking, we need some other variables. More specifically, we need to check when the omelette is done. Usually, it's either done, or it's not. We call this a boolean statement. So, without further a do, a boolean statement called done:
 
 ```var done = false```
 
 We start it off with false since we have all raw ingredients, and if you've cooked eggs before, you know they are never done to begin with.
 
 *Sidenote: Ever noticed how recipes have action verbs? They are actions or things to do, and that's what we're covering next!*
 
 We got all our ingredients ready to go, let's get cooking. First thing is to beat the eggs, water, salt and pepper. We can do this as a task, or in JavaScript terms, a function, like this:
 
 ```function beat(){
 
 }
 ```
 This is how a basic function looks in JavaScript. We'll take it step by step. We need the ingredients we have from before to use inside this task, so we can get them like this:
 
 ```function beat(eggs, water, salt, pepper){
 
 }
 ```
 This function can take as many parameters as it needs to get the job done, so here we need eggs, water, salt and pepper. Let's take a look what's next. It says *until blended*, so it's safe to say it's not blended to start with? Cool, another boolean:
 ```function beat(eggs, water, salt, pepper){
 var blended = false;
 }
 ```
 You can keep the blended boolean in or out of the function, but if it's related to a specific task, keep it inside. It's probably happier to be there too.
 
 So how long does it say until blended? We don't really know. But let's do a certain amount of turns of our spatula to make sure it's nice and smooth. Next up is what we call a for loop.
 
 ```function beat(eggs, water, salt, pepper){
 var blended = false;
 
 for(var turns = 0; turns <=10; turns++){
 
 }
 }
 ```
 
 So there's a lot going here. Let's break it down: you got for with brackets, that means for every turn you make. Turns start at zero, since you haven't turn the spatula, turns is less than or equals to 10, since 10 is the amount of turns you want to do. Since you want to go from zero to 10, you need to do more turns, in this case increment the value of turns made.
 
 Alright, next up is what goes inside of that beastly thing. Simple!
 ```
 function beat(eggs,water,salt,pepper){
 var blended = false;
 
 for(var turns = 0; turns <=10; turns++){
 console.log("TURN! the " + eggs + " eggs, " 
 + water + " cups of water, " + salt + " of salt, and a" + pepper + " of pepper.");
 }
 }
 ```
 Console.log is a way of displaying a message to the console, which is this box thing that nobody ever sees on the internet. It's only for you, the developer to see and know if something is going right or wrong. It takes the values from each of the variables, and adds it to a string with other strings. Here, it's for you to know that you're turning the spatula around, and it's totally fun.
 
 But what happens after it's all blended? We have to turn blended to true:
 
 ```
 function beat(eggs,water,salt,pepper){
 var blended = false;
 
 for(var turns = 0; turns <=10; turns++){
 console.log("TURN!");
 }
 blended = true;
 }
 ```
 This comes after turning 10 times, since now it's fully blended.
 
 But let's take it a step further!! You want to keep the result of this task somewhere to use for later on. That's where the return keyword comes in!
 
  ```
 function beat(eggs,water,salt,pepper){
 var blended = false;
 
 for(var turns = 0; turns <=10; turns++){
 console.log("TURN!");
 }
 blended = true;
 return blended;
 }
 ```
 What this does is outputs the result of the task; here, we want to know that everything is fully blended. So we return the blended boolean since it's true - it IS blended! And we can do something like this:
 
 ```var isBlended = beat();```
 
 Which keeps the result in a safe place for later use. When we do beat(), this means we're calling the function, meaning we want the task to run and output the result.
 
 Alright, so that's the basics. Let's continue at a faster pace now.
 
 We're going to need heat the butter in a skillet over medium high heat. Ok, let's write a function for that:
 
 ```
 function heatUpSkillet(){
 var isHeated = false;
 
 for(var time=0; time<2; time++){
 if(time=0)
 console.log("heating - not hot");
 if(time=1)
 console.log("heating - kinda hot");
 }
 console.log("Hot - butter is melting now");
 isHeated = true;
 tilt();
 if(isBlended){
 pourInEggs();
 }
 }
 ```
 Ok, lot is going on here. Let's break it down:
 1. We have a heatUpSkillet function, that has isHeated boolean set to false to start. 
 2. Then, we have a for loop that checks the amount of minutes and increases the minute by one until 2. 
 3. Each minute has it's own console.log which indicates how hot the skillet is. 
 4. When it reaches 2, we get a message saying the butter is melting, and that the skillet is now heated, setting isHeated to true.
 5. There's a function called tilt which we haven't seen yet, but we're calling that function here. 
 6. We're also checking our stored isBlended boolean variable if it is true, so we can call pourInEggs. We're not explicitly saying it's true, as the variable itself is truthy or falsey. This means if it is set to true or false, we can omit saying it because it becomes that.
 
 Let's do the the functions called here fast:
 ```
 function tilt(){
 console.log("eggs are tilted");
 }
 
 function pourInEggs(){
 console.log("eggs are poured in");
 }
 ```
 
 These are straightforward. Let's continue cookin'!
 
 ```function gentlyPush(){
 console.log('push eggs into center to cook uncooked egg');
 }
 
 function keepCooking(){
 gentlyPush();
 tilt();
 }
 
 function placeFilling(){
var fillings = mushrooms + " mushrooms " + onions + " onions " + garlic + " garlic ";
 console.log(fillings + " and cheese " + cheese);
 fold();
 serve();
 }
 
 function fold(){
 console.log("fold egg");
 }
 
 function serve(){
 console.log("EATING TIME!");
 }
 ```
 Let's look at the last few functions:
 
 1. gentlyPush() gives instructions to cook any uncooked eggs. keepCooking calls gentlyPush() and the tilt() function.
 2. placeFillings has a variable called fillings which takes all the variables and the names of the filling, and puts them into a string. It console.log's that variable, a string " and cheese" and the cheese variable into one big string). Fold and serve are both called which gives the final instructions.
 
 So let's put what we have ALL together now as one big happy picture!
 
 
 ```var eggs = 2;
var water = 0.25;
var salt = "1/8 tsp"
var pepper = "a dash";
 var butter = 0.02;
 
var mushrooms = 4;
 var onion = 1;
 var garlic = 3;
 var cheese = "YES!"

var done = false;
  var isBlended = beat();
  
  
 function beat(eggs,water,salt,pepper){
 var blended = false;
 
 for(var turns = 0; turns <=10; turns++){
 console.log("TURN! the " + eggs + " eggs, " 
 + water + " cups of water, " + salt + " of salt, and a" + pepper + " of pepper.");
 }
 blended = true;
 return blended;
 }
 
function heatUpSkillet(){
 var isHeated = false;
 
 for(var time=0; time<2; time++){
 if(time=0)
 console.log("heating - not hot");
 if(time=1)
 console.log("heating - kinda hot");
 }
 console.log("Hot - butter is melting now");
 isHeated = true;
 tilt();
 if(isBlended){
 pourInEggs();
 }
 }

 function tilt(){
 console.log("tilting happened 0w0");
 }
 
function pourInEggs(){
 console.log("eggs are poured in");
 }

function gentlyPush(){
 console.log('push eggs into center to cook uncooked egg');
 }
 
 function keepCooking(){
 gentlyPush();
 tilt();
 }
 
 function placeFilling(){
var fillings = mushrooms + " mushrooms " + onions + " onions " + garlic + " garlic ";
 console.log(fillings + " and cheese " + cheese);
 fold();
 serve();
 }
 
 function fold(){
 console.log("fold egg");
 }
 
 function serve(){
 console.log("EATING TIME!");
 }
 ```
 
 And that's it! Not only you can make eggs, you can make a decent amount of JavaScript code in the process. Soon, you'll be a pro chef in no time, in the kitchen AND in the code editor.
 
 --If you liked this tutorial and want more, please let me know. Feel free to add to the repo.
