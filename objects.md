# Objects

Objects are a collection of properties and behaviors. I like to think of Objects as cookie cutter template. A Cookie Cutter has a set of charactersitics that allow me create multiple cookies (lets say a gingerbread man) that are almost identical. I can change the properties of the gingerbread man (adding different color frosting, etc), but each cookie is still fundamentally similar to each one before it.

**Example**: The Object below is an example of a blood cell object. It is a collection of properties (x and y coordinates, and color) and behaviors (display and move).

```javascript
    function setup(){
        createCanvas(600, 400);
        c1 = new Cell(100, 100);
        c2 = new Cell(300, 100);
        c3 = new Cell(100, 500);
        c4 = new Cell(300, 500);
    }

    function draw(){
        background(0);
        c1.display();
        c1.move();
        c2.display();
        c2.move();
        c3.display();
        c3.move();
        c4.display();
        c4.move();
    }
    
    function Cell(x,y){
    this.x = x;
    this.y = y;
    fill(255, 0, 50, 125);
    this.display = function(){
        stroke(255);
        ellipse(this.x, this.y, 50, 50);
    }
    this.move = function(){
        this.x = this.x + random(-1, 1);
        this.y = this.y + random(-1, 1);
    }
}
```