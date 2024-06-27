# 20.2.5-tracking-inventory

**note to future me** review how [flag variables work](https://youtu.be/lZ51aXq-VIg?si=zanp8y2APElS-2mC)

**another note to future me** show how to use conditionals with .includes()


# Data Structures Assign- Tracking Inventory Game

While this assignment will take on the theme of a game, it is not a game.  The user gets no choice and it flows linearly.  That said, it should plant seeds of ideas for future games.

The focus of this assignment is to manipulate arrays, you need to show that you know how to use `push()`, `splice()`
  - Array methods docs, this is where to find [info on `push` and `splice`](https://www.w3schools.com/js/js_array_methods.asp)

## The Structure of the Program

- The program will consist of 11 Scenes. Each scene displays one after the other when the mouse is clicked.
- Create a sceneNum variable and prepare your draw function to call the scene functions when they are ready.
- In mousePressed, you simply need sceneNum++ and set a flag variable.  The flag variable will be discussed in class

## Set up the following global variables:
- An inventory array.  
- To start the program, the inventory will contain: water, a knife, a shield, a hat
- A coins variable. To start the program, the coins variable will start at 10.

NEED HELP?  The above setup code is provided at the end of this document.

## On Every Scene you will do the following:
- Print a sentence or two about the story
- Add an if statement that will ensure that ‘an update’ happens only once, or use the flag variable
- Print out of the inventory array after the update occurs
- Print your current number of coins.



## The Scenes

### Scene 1
Something has caused a monster apocalypse.  Write a couple of sentences to start the story.
You are welcome to add an image to the first scene but do not do so for the others unless you have time at the end.

### Scene 2
You meet a nice granny on the street who gives you a map and 5 coins to help you on your quest.
Use the `PUSH` function to add the map to your inventory and add 5 coins to your variable.

You will find that you have a lot of maps being pushed into your inventory, and you will have an infant money gitch. 
use this code to help, it check if ` map` is not (not is the! part of `!inventory.includes(' map'))`
```
  if (!inventory.includes(' map')) {
    inventory.push(' map');
    coins += 5;
  }
```

### Scene 3
You come across a horrible ____.  You win the fight but in the process, your shield is broken.
Use the `splice` function to remove the shield.

### Scene 4
Getting hungry, you enter an abandoned restaurant and gather supplies.  
You decide to keep your food and water supplies at the beginning of the list.  Use the `SPLICE` to add two food supplies at slot 1 in your inventory.
- Did you do it right? Your first 3 items should now be something like: water, hot dog, pizza pocket.

### Scene 5
You come across a small group of hungry children who are desperate for supplies.  You decide to check out what you have for supplies but then decide to be mean and do not give them any.
Printing your entire inventory as usual.  Then separately, print just the first 3 items in your inventory, you want to taunt them by saying something like "look at these things we have and you don't.... muahahahahah".  (Reminder: The first 3 are at index 0, 1, 2 and should be your 3 food items.)

  
### Scene 6
Your choice.  Use `PUSH` or `SPLICE` in some way.


### Scene 7
You meet a blacksmith who offers to sell you a magical sword.  
Give her 5 coins and add the sword to your inventory.


### Scene 8
You fall asleep and when you wake up, you think you notice some new footprints.
Use `SPLICE` to remove the water from your inventory.


### Scene 9
Your choice.  Use an `IF` statement in the scene in some way.


### Scene 10
You discover the Queen Monster and face her in an epic battle. You save the world but your weapons are destroyed in the process.  
Use `SPLICE` to remove the weapons from your inventory.


### Scene 11
The End




```
let inventory = ["water", " knife", " shield", " hat"];
let sceneNum = 1;



function setup() {
  createCanvas(800, 600);
}//end setup

function mousePressed() {
    sceneNum++;
}//end mousePressed

function draw() {
  background(242, 48, 101);
  if(sceneNum === 1){
    scene1();
  }
  if(sceneNum === 2){
    scene2();
  }
}//end draw

function scene1(){
  text("scene 1", 300,40)
  textSize(15);
  text("Welcome intrepid hero! A treacherous member of the King's Council has \nreleased hordes of bloodthirsty monsters into all corners of the kingdom. \nAs a member of the Hero's Guild, it is your duty to protect the kingdom \nfrom all threats of the mystical kind.", 20, 450);
  text("Inventory: " + inventory, 20, 550);
  text("Coins: " + coins, 20, 565);  
}//end scene 1

function scene2(){
  text("scene 2", 300,40)
  textSize(15);
  text("Scene 2", 20, 450);
}//end scene 2
```

## Grades 

| **Proper use of functions and if()**   (1 Point) | |
|---------------------------------------------|--------------------------------------|
| **Code Clarity and Organization** (5 points) |                                      |
|---------------------------------------------|--------------------------------------|
| **Structure**                   | Code is well-organized into logical sections with clear separation of concerns. |
| **Comments and Documentation**     | Concise and informative comments aid understanding of the code. |
| **Indentation and Formatting**   | Consistent indentation and spacing enhance readability. |
| **Naming Conventions**          | Descriptive variable and function names improve code clarity. |
| **Readability and Maintainability**  | Code is easy to read, understand, and maintain. |
| Total Points: 5                             |                                      |

| **Inventory Manipulation** (5 points)      |                                      |
|--------------------------------------------|--------------------------------------|
| **Array Methods Usage**          | Proper use of array methods to update inventory. |
| **Inventory Update Accuracy**   | Inventory updates accurately reflect the game progression. |
| **Inventory Printing**            | Clear printing of inventory after updates. |
| **Storyline Integration**         | Inventory changes are seamlessly integrated with the storyline. |
| Total Points: 5                            |                                      |
