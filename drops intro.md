

```javascript
const drops = [];

function setup() {
  createCanvas(300, 300);
  for(let x = 0; x < width; x++) {
    drops[x] = random(height);
  }

  stroke(255);
}

function draw() {
  background(32);

  for(let x = 0; x < drops.length; x++) {
    drops[x] += random(5);
    if(drops[x] > height){
      drops[x] = 0;
    }

    point(x, drops[x]);
  }
}
```
