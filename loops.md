# Loops

Loops allows us to efficiently repeat code. When we use them in conjuction with variables, we can acheive a large number of different outputs with just a few lines of codes.

In the context of this course, the two types of loops are **while loops** and **for loops.**

These loops have 4 parts:
1. an initialized variable
2. an exit condition
3. the code that will be looped
4. an icrementing/decrementingn of that variable

## While Loops

In a while loop, we use a condition as reference to check if we should keep looping code. 

**Note**: When using while loops, you should always think about what condition will get the loop to stop. If you don't, then you could easily enter an ***infinite loop*** (a loop that goes on forever) and crash your program.
```
   while(something is true){
        //if that something is not true the loop will not exectue
        keep doing this code.
   }
```

**Example:** The code below will make a series of circles 50 pixels apart from each other halfway down the screen.

```javascript
    var x = 0; //initalize variable
    
    function setup(){
        createCanvas(600,400);
        background(0);
    }
    function draw(){
        while(x <= 600){ //exit condition
          //my code to be looped
          ellipse(x, 200, 20, 20);
          x = x + 50; //incrementing x by 50 so when it is greater that 600 we exit the loop.
        }
    }
```

## For Loops

Just like *while loops*, *for loops* contain the same 4 basic parts except it is much more condensed than a while loop.

```
    for(initialize variable; exit condition; increment){
        code to loop
    }
```

**Example:** Just like in the *while loop* example above, the code below will make a series of circles 50 pixels apart from each other halfway down the screen.

```javascript
    function setup(){
        createCanvas(600,400);
        background(0);
    }
    function draw(){
        for(var x = 0; x <= 600; x = x + 50){ 
          ellipse(x, 200, 20, 20);
        }
    }
```