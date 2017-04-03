# Variables

Think of variables like you would in math. They are placeholders for values that can change or vary. One big difference between variables in programming and in math is that in programming variables can be words while in math variables are single letters.

## Creating Variables in 3 Steps
1. **Declare**: you have to tell your program when you are creating a variable. If you don't, then your program won't know what to do with the word/letter you used.
2. **Initialize**: Once you've created your variable, you have to set it to a value. 
3. **Use**: Variables are kind of useless unless you actually use them somewhere in your program.

    ### Example:
    
    ```javascript
    //this is me declaring two variables x and y
    var x;
    var y;
    
    //I initialize them by assigning them values
    x = 300;
    y = 200;
    
    /*I can use them in a variety of ways, 
    in this case I'll create an ellipse in the center of the screen.*/
    function setup(){
        createCanvas(600,400);
    }
    function draw(){
        background(0);
        ellipse(x, y, 50, 50); //I'm using x and y here
    }
    ```
    
    ### Note:
    You can *declare* and *initialize* variables on the same line. Thus, the above example can be written like so:
    ```javascript
    //this is me declaring two variables x and y
    var x = 300;
    var y = 200;
    
    function setup(){
        createCanvas(600,400);
    }
    function draw(){
        background(0);
        ellipse(x, y, 50, 50);
    }
    ```
## Changing the values of variables

Because variables by nature change in value, there are a couple of different ways we can re-assign values to variables.

#### Simply Re-assigning the value
```javascript
    var x = 10;
    var y = 50;
    
    alert(x + y); //this outputs 60
    
    var x = 50; //this replaces the 10 with 50
    alert(x + y); //this outputs 100
```

#### Incrementing/Decrementing
We can increase/decrase a variable's value by a specfic number (this is helpful in looping or moving things across the screen). The following 3 methods are equivalent:
* `x = x + 1`
* `x += 1`
* `x ++`

    **Note:** `x = x + 1` and `x += 1` are advantageous because you can swap the 1 for any number. If you want something to increase by 5 each time then just write `x = x + 5` or `x += 5`. 
    
    `x++` is advantageous when you only need to increment by 1 since this is the shortest. 
    
    If you need to decrease variables, then just swap the `+` for `-`