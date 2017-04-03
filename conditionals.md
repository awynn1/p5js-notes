# Conditionals

Conditionals allows our programs to "think." It's allows our programs to behave and do things differently based on a given situation. All conditions evaluate to `true` or `false` and then will proceed to execute (or not execute).

```
    if(the condition){
        this executes if the condition is true
    }
    else{
        this executes if the condition is false
    }
```

**For example:** Below we have an ellipse on top of a black background. *If* the x-coordinate of the mouse (`mouseX`), moves beyond the 300-pixel mark (that's halfway across the canvas), then the background will change to red *else* it will remain black.
```javascript
    function setup(){
        createCanvas(600,400);
        background(0);
    }
    function draw(){
        ellipse(300, 200, 50, 50);
        
        if(mouseX > 300){
            background(255,0,0);
        }
        else{
            background(0);
        }
    }
```

## Comparison Operators

Operator | Description 
---------| ----------- 
`>`      | Greater than 
`>=`     | Greater than or equal to 
`<`      | Less than 
`<=`     | Less than or equal to 
`==`     | Equal to 
`!=`     | Not Equal to 
`&&`     | **AND** 
ll    | **OR** 

## AND and OR

The **AND** and **OR** operators allow you to check for multiple conditions at once.

An example of using **AND** (&&) might be:

```javascript
    if( gpa > 3.5 && conduct == "positive"){
        alert("parents buy me car");
    }
    else{
        alert("continue taking the bus.");
    }
    
    //both conditions must be true in order for your parents to buy you a car.
```

An example of using **OR** (`||`) might be:

```javascript
    if( salary > 1000000 || winLottery == true){
        alert("buy myself a yacht");
    }
    else{
        alert("continue dreaming about that yacht life #foreverBroke");
    }
    
    //only ONE of the two conditions has to be true.
```

Another example take from a class assignment:

```javascript
    var x = 300;
    var y = 200;
    var speed = 3;
    
    function setup(){
        createCanvas(600,400);
        background(0);
    }
    function draw(){
        ellipse(x, y, 50, 50);
        
        //this if statement changes the direction the cirlcle moves
        if(x > 600 || x < 0){
            speed = -speed;
        }
        
        //this changes the x-coordinate of the ball 3 pixels to the right.
        //but when the if statement gets triggered, it will be x = x + -speed moving it in the opposite direction
        x = x + speed;
    }
```