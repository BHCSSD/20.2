EDIT so it uses roation instead of sin cos


///javascript
let earthSize = 150;
let moonSize = 75;

let angle = 0;
let distance = 150;

let moons = ['🌕','🌖', '🌗', '🌘', '🌑', '🌒', '🌓', '🌔'];
let moonIndex = 0;

let earths = ['🌎', '🌍', '🌏'];
let earthIndex = 0;

function setup() {
  createCanvas(400, 400);
  textAlign(CENTER, CENTER);
}

function draw() {
  background(32);

  angle++;

  if(angle % 45 == 0){
    moonIndex++;
    if (moonIndex >= moons.length) {
      moonIndex = 0;
    }
  }

  // if(angle % 120 == 0){
  //   earthIndex++;
  //   if (earthIndex >= earths.length) {
  //     earthIndex = 0;
  //   }
  // }

  let moonX = width / 2 + cos(radians(angle)) * distance;
  let moonY = height / 2 + sin(radians(angle)) * distance;

  textSize(earthSize);
  text(earths[earthIndex], width / 2, height / 2);

  textSize(moonSize);
  text(moons[moonIndex], moonX, moonY);  
}
```
