# Object building practice
MDN Web Docs: [bouncing balls demo](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_building_practice)

**See this live:** https://bideinsilence.github.io/objectBuildingPractice


## How it's made:
HTML, CSS, Javascript, and the Canvas and requestAnimationFrame APIs


## Optimizations:
I commented much of the code and in one place added the exponentation operator
to make it easier to understand, for example:

```
// Collision detection
collisionDetect() {
    for (const ball of balls) {
        // Check to make sure that current ball being looped through is not
        // the same ball as the one being checked
        // Code only runs if not the same
        if (!(this === ball)) {
            // Distance (hypotenuse of a right triangle) is equal to the
            // square root of the squared x and y distances (legs) added
            // togther; Pythagorean Theorem c = √(x^2 + y^2)
            const dx = this.x - ball.x;
            const dy = this.y - ball.y;
            const distance = Math.sqrt(dx ** 2  + dy ** 2);

            // If balls collide (whether any of the two circles'
            // areas overlap), assign both the same new random color
            if (distance < this.size + ball.size) {
                ball.color = this.color = randomRGB();
            }
        }
    }
}

```

## Lessons Learned:
This was an exciting and visually dynamic opportunity to practice working with
JavaScript classes and some of the browser APIs to build a simple web
application.

