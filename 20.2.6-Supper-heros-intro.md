# 20.2.6-Supper-heros-intro

```
let allHeroes = ["Thor","Ironman","Superman", "Storm", "Wonder Woman"];
let isHuman = [false, true, false, true, true];
let allPics = [];
let rand;
let angle = 0;

function preload(){ // fill our your file names
  allPics.push(  createImg( "")   );
  allPics.push(  createImg( "")   );
  allPics.push(  createImg( "")   );
  allPics.push(  createImg( "")   );
  allPics.push(  createImg( "")   );

  for(let i=0; i<allHeroes.length; i++){
      allPics[i].hide();
    }//end for
}//end preloading of images

function setup() {
	createCanvas(800, 800);
  // we need to fill out our random variable here. 
  //print(rand);
  angleMode(DEGREES)// use this or you have to deal with RADS
}//end setup



function draw() {
  background(100,92,80);

  imageMode(CORNER)//just like rectMODE
// lets add a for loop here

  noFill();
  strokeWeight(5)
  stroke(255,255,0);
  rect(50,50,400,400);
  fill(255,255,0);
  noStroke();
  textSize(20);
// text to show random hero... 

  imageMode(CENTER);
  translate(250,250) // sets x250,y250 and makes it the new 0,0
  rotate(angle)
  image(allPics[rand], 0, 0, angle, angle);
  resetMatrix(); //undoes the translate, 0,0 is back to normal
  if(angle<360){ //this is the roation bit
      angle+=3;
  }
    
}//end draw

```
