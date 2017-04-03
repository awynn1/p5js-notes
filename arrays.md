# Arrays

Arrays are lists. They are essentially a collection of elements (variables, numbers, strings, etc) or objects.

The elements in arrays are numbered with an index value, however it is important to remember that the index value of the first element of an array starts with 0.

Bucket List
index | element
-- | --
0 | "Jump out of airplane"
1 | "Swim with Sharks"
2 | "Kiss Beyonce"
3 | "Shake hands with Obama"

Arrays are denoted with square brackets `[ ]` and in the context of this course, can be created in 2 ways:

1. We can create a list altogether:
```javascript
var listofnumbers = [12, 15, 17, 19, 20];
```
**OR**

2. We can assign values to an array (even an empty array), individually:
```javascript
listofnumbers[0] = 12;
listofnumbers[1] = 15;
listofnumbers[2] = 17;
listofnumbers[3] = 19;
listofnumbers[4] = 20;
```

## Using Arrays

We access the elements of the arrays by using the array's name and the index value of the element we want. 

**For Example:** If I have a list of words such as choice, voice, hustle, grit, growth, optimism, consideration,bad and boujie: I can create prompts of a specic set of those words:

```javascript
    var habits = ["choice", "voice", "hustle", "grit", "growth", "optimism", "consideration","bad and boujee"];
    
    alert(habits[2]);
    alert(habits[3]);
    alert(habits[7]);
    
    //this will create three prompts that show only "hustle", "grit", and "bad and boujee"
```

## Using Arrays with Looops
I can replace the index value of an array with a variable and loop through it.

**For example**: I am going to use our list of numbers to create ellipses of various sizes.

```javascript
    size = [10, 20, 40, 80, 160];
    
    for(var i = 0; i < size.length; i++){
        ellipse((i+1)*100, 200, size[i], size[i]);
    }
```

**Note**: The ***.length*** is a built in javascript function that returns the number of elements in myy array which in this case is 5. I could have also acheived the same result by writing the above example as:

```javascript
    size = [10, 20, 40, 80, 160];
    
    for(var i = 0; i < 5; i++){
        ellipse((i+1)*100, 200, size[i], size[i]);
    }
```