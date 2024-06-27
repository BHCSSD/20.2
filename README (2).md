# 20.2.1-wages


```
let wage = 13.50;
let allShifts = [];

function setup() {
	createCanvas(800, 600);
//Two ways to add data to an array 
//1. By index number
//2. By PUSH, which adds to the end of the array. Look for push in mousePressed

    allShifts[0] = 4;
    allShifts[1] = 6;

}//end setup

function draw() {
    background(200,200,80);
    textSize(20);
    text("Hours Worked", 50, 50);
    text("Dollars Earned", 250, 50);
    
    //for( let i=0;       ;  i++ ){


   // }//end of for
  
//How to figure out the Total Algorithm 
    let total = 0;
   // for( let i = 0;                ; i++  ){


   // }// end of for
    text("Total Earned $" + (total*wage), 400, 200   );
   
}//end draw


function mousePressed() {
    //let tempHours = 1.0*window.prompt("How many hours did you work?")
    //allShifts.push(tempHours);
}//end mousePressed
```
