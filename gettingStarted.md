## Getting Started

At minimum, you need an **index.html** file and a **sketch.js** file, but for purposes of getting in the habit of building full sites/webapps, you should get into the habit of creating a **style.css** and a **script.js** file.

In your **index.html** file:

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="//cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.7/p5.js"></script>
    <script src="sketch.js"></script>
  </head>
  <body>
  
  </body>
</html>
```

**Note:** In the above example, we are importing the p5 javascript library using what's called a Content Delivery Network or CDN. There are other ways to do this, but as beginners and for simplicity's sake this is a nice and easy method.


If you create all 4 files (`index.html`, `style.css`, `script.js`, and `sketch.js`), your `index.html` file should look like this:

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="style.css" type="text/css" />
        <script src="//cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.7/p5.js"></script>
        <script type="text/javascript" src="sketch.js"></script>
    </head>
    <body>
        
    </body>
    <script type="text/javascript" src="script.js"></script>
</html>
```
The above example will allow you the most flexibility when designing future web applications, so it would be best to get into the habit of using this structure even if you don't write any code into all the files.


In your **sketch.js** file:

```javascript
	function setup(){
		createCanvas(width,height);
	}
	function draw(){
	
	}

```
**Note:** In the above example for `createCavas(width,height)` you can use any dimenstions for a width and height such as `createCanvas(600,400)` or even `createCanvas(width/2,height/2)` which would take up half of the width of the browser's window and half of the height of the browser's window.

## function setup( ) vs. function draw( )

These two functions are automatically executed by p5js. The main difference is that `function setup( )` is called only once, while `function draw( )` is called repeatedly. Therefore, your p5js project will behave differently depending on where you put the `background( )` function.

**Note:** `background( )` by default takes color in a red, green, blue (r,g,b) format. If you use the same number across all three values, then only one number is needed. For example: `background(50,50,50)` is the same as `background(50)`


Play around with the two example structures in your `sketch.js` file.

#### Example 1: `background( )` is in `function setup( )`.

```javascript
	function setup(){
		createCanvas(width,height);
		background(50,50,50);
	}
	function draw(){
		
	}

```

#### Example 2: `background( )` is in `function draw( )`.

```javascript
	function setup(){
		createCanvas(width,height);
		background(50,50,50);
	}
	function draw(){
		
	}

```