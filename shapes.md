# Creating Shapes & Other Basics

## Ellipses
* `ellipse(x-coordinate, y-coordinate, width, height)`
* ellipses that have the same width and height make a circle.

**Example:** The ellipse below is a circle in the middle of the screen.

```javascript
	function setup(){
		createCanvas(600,400);
	}

	function draw(){
		ellipse(300,200,50,50);
	}
```

## Rectangles
* `rect(x-coordinate, y-coordinate, width, height)`
* rectangles that have the same width and height make a square.
* the x and y coordinates of the rectangel represent the TOP-LEFT of the rectangle.

**Example:** The rectangle below is a square in the middle of the screen.

```javascript
	function setup(){
		createCanvas(600,400);
	}

	function draw(){
		rect(275,175,50,50);
	}
```

## Lines
* `line(x-coordinate-1, y-coordinate-1, x-coordinate-2, y-coordinate-2)`
* Lines are made up of two points: a starting point (x1, y1) and an ending point (x2, y2).
* A line that goes straight up and down has x1 equal to x2.
* A line that goes straight left to right has y1 equal to y2.

**Example:** There are 3 lines code here. Look at the comments.

```javascript
	function setup(){
		createCanvas(600,400);
	}

	function draw(){
		//a line that goes from bottom left to top right
		line(100,300,400,200);
		
		//a line that goes straight up and down
		line(200,150,200,250);
			
		//a line that goes straight left to right
		line(300,300,400,200);
	}
```

# Other Basics

### Colors
* Colors can be written in two formats:
    * `(r, g, b)`: 3 arguments that represent red, green, and blue; with each value ranging from 0 to 255. 
    * `(r, g, b, a)`: the same as `(r, g, b)` excpet the 4th argument (the a value), represents *alpha* which is a fancy computer word for transparency. In p5js, the alpha value also ranges from 0 to 255. 

### Fill
* `fill(color)`: the fill function sets the p5 drawing to a specific color to fill all shapes with. Once a `fill()` is selected, all shapes after will be that color until a new `fill()` is declared.
* `noFill()` : this allows shapes to be empyt (no-color in them and therefore transparent).

### Stroke
* *stroke* is the outline of shapes.
* `stroke(color)` sets the outline of a shape to a specfic color.
* `noStroke()` means that when shapes are drawn they will not have any outline on them. 
* `stokeWeight(value)` sets the thickness of the outline to a specfic value.