remix 

## todo
1. Go through each block of code and explain what it does. Be specific with the arrays.
2. Make it your own:
    - Change the number of lines, or their colors.
    - Give each line a random color.
    - Make the animation look more like a mountain, or a city


```javascript
const lines = 100;
let lineHeights = [];
let lineSpeeds = [];

function setup() {
  createCanvas(400, 400);

  for(let x = 0; x < lines; x++){
    const lineHeight = random(height);
    lineHeights[x] = lineHeight;
    lineSpeeds[x] = random(-10, 10);
  }
}

function draw() {
  background(32);

  for(let i = 0; i < lines; i++){
    lineHeights[i] += lineSpeeds[i];

    if(lineHeights[i] < 0 || lineHeights[i] > height) {
      lineSpeeds[i] *= -1;
    }

    const x = width * (i / lines);
    const lineWidth = width / lines;

    fill(0, 100, 255);
    stroke(0, 100, 255);
    rect(x, height / 2 - lineHeights[i] / 2,
         lineWidth, lineHeights[i] / 2);

    fill(100, 0, 255);
    stroke(100, 0, 255);
    rect(x, height / 2,
         lineWidth, lineHeights[i] / 2);
  }
}
```
