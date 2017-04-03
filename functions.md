# Functions

Functions in programming serve two main purposes:

1. **Modularity**: Chunking our code into functional parts
2. **Reusability**: Being able to resuse code if and when we need it.

## Modularity
Functions allow us to chunk parts of our programs so that it becomes easier to read, debug, and code.

**Example**: The two code snippets below have the exact same output which is a circle that moves across the screen horizontally. Tough the second version is a lot longer, it is much more readable. This will be especilaly true as programs get longer and more complex.

**Before implementing functions**

```javascript
var x = 300;
var speed = 8;

function setup(){
    createCanvas(600,400);
}

function draw(){
    background(0);
    //display ball
    fill(50,250,50);
    ellipse(x, 200, 50, 50);
    //make ball move
    x = x + speedx;
    //ball changes direction when it hits wall
    if(x>600 || x<0){
        speed = -speed;
    }
}
```

**After implementing functions**

```javascript
var x = 300;
var speed = 8;

function setup(){
    createCanvas(600,400);
}

function draw(){
    background(0);
    display();
    move();
    bounce();
}

function display(){
    fill(50,250,50);
    ellipse(x, 200, 50, 50);
}

function move(){
    x = x + speed;
}

function bounce(){
    if(x>600 || x<0){
        speedx = -speedx;
    }
}
```
## Reusability

Functions also allow us to wrap code into a keyword that we make so we can reuse that code when we want.

**Example**: The code below wraps the code of drawing a flower into a word called ***flower.*** I can then use the flower function anytime I want to draw a flower without having to rewrite all those lines of code.

In this particular example, the flower function is reused every time the user clicks the mouse.

```javascript
function setup(){
    createCanvas(600,400);
    background(50);
}

function draw(){
    if(mouseIsPressed){
        flower(mouseX,mouseY);
    }
}

function flower(x,y){
    //petals
    noStroke();
    fill(255,150,200);
    ellipse(x+10,y-10,35,35);
    ellipse(x+10,y+10,35,35);
    ellipse(x-10,y-10,35,35);
    ellipse(x-10,y+10,35,35);
    
    //bulb
    fill(255,200,0);
    ellipse(x,y,25,25);
}
```