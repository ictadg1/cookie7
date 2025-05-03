# Cookie Clicker Game - Part 2

## Introduction
Author:
D.Antrobus 2025

Welcome to Part 2 of the Cookie Clicker game! In this tutorial, we'll enhance our game with:
- Cookie movement and bounce effects
- Special effects when clicking cookies
- Sound effects
- A shrinking cookie for more challenge
- Game over conditions


<!-- 

dev: http://localhost:8004/common

dev: http://localhost:8004/clicker

https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/

 -->
![Cookie clicker game enhanced](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-part2-preview.png)

## Important:
Have you coded part 1?

![Part 1](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-part1-final.png)

**Go back and complete Cookie Clicker Part 1 Tutorial if you have not done this yet.**


## Step 1: Make your cookie move

First, let's make our cookie bounce around the screen for a more challenging game!

1. Find the **red** `||sprites:set mySprite bounce on wall on||` block from the Sprites category

![Cookie bounce block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/bounce-walls.png)

2. Add it to your program after creating the cookie sprite
3. Change "mySprite" to "cookie" in the dropdown

![Setting cookie bounce](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-set-bounce.png)

## Step 2: Set cookie velocity

Now let's set the speed and direction of the cookie's movement.

1. Find the **red** `||sprites:set mySprite velocity to vx: 0 vy: 0||` block

![Velocity block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/cookie-velocity-block.png)

2. Add it to your program after the bounce on wall block
3. Change "mySprite" to "cookie" in the dropdown
4. Set the vx to 60 and vy to 50

![Setting cookie velocity](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-set-velocity.png)

## Step 3: Add effects when clicking

Let's add a visual effect when we click the cookie!

1. Find the **red** `||sprites:start effect on sprite||` block

![Start effect block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/cookie-start-effect.png)

2. Add this block at the beginning of your if-statement in the mouse button pressed event (before the change score block)
3. Change the sprite to "cookie"
4. Select "ashes" for the effect
5. Set the duration to 100 ms

![Adding effect to cookie](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-add-effect.png)

## Step 4: Add sound effects

Next, let's add sound when we click the cookie!

1. Find the **pink** `||music:play sound||` block

![Play sound block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/cookie-play-sound.png)

2. Add this block after the change score block in the if-statement
3. Click on the dropdown and select "create sound effect"
4. Configure your sound with these settings:
   - Wave shape: Noise
   - Starting frequency: 670
   - Effects: None
   - Duration: 10 ms

![Sound effect settings](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-sound-settings.png)

## Step 5: Add camera shake

Let's make the screen shake when we click the cookie!

1. Find the **blue** `||scene:camera shake||` block

![Camera shake block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/cookie-camera-shake.png)

2. Add this block after the play sound block
3. Set the intensity to 4 and the duration to 100 ms

![Adding camera shake](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-add-shake.png)

## Step 6: Add a size variable

Now let's make our game more challenging by making the cookie shrink over time!

First, we need to create a variable to track the cookie's size.
1. Select `||variables:Make a Variable||"

![Make a variable](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/make-variable.png)

2. Name the variable "size"

![Name variable](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/name-variable-size.png)


3. Find the **red** `||variables:set size to||` block

![Set variable block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/cookie-size-variable.png)

3. Add this to the beginning of your on start section (before creating the cookie)
4. Set the value to 1

![Adding size variable](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-add-size.png)

## Step 7: Add game update interval

Now we'll set up the code that runs repeatedly to shrink the cookie.

1. Find the **purple** `||game:on game update every||` block

![Game update block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/game-update.png)

2. Set the interval to 1000 milliseconds (1 second)

![Setting update interval](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/set-update.png)

## Step 8: Shrink the cookie

Inside the game update block, we need to:
1. Decrease the size variable
2. Update the cookie's scale

1. Add a **red** `||variables:change size by||` block into the game update section

![Change size block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/cookie-change-size.png)

2. Set the size value to -0.02

![Set scale value](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/set-scale-value.png)

3. Add a **red** `||sprites:set sprite scale to||` block after the change size block

![Set scale block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/cookie-set-scale.png)

![Select size variable](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-select-size.png)

4. Change "mySprite" to "cookie" and set the scale to "size"

5. Keep the anchor as "middle"

![Scaling the cookie](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-scaling.png)

## Step 9: Add game over condition

Finally, let's end the game when the cookie gets too small!

1. Add a **light blue** `||logic:if then||` block after the set scale block

![If block for game over](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/logic-if.png)

![if block for game over](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/game-over-if.png)

2. Add a **light blue** `||logic:0 <= 0||` block for the condition

![logic condition](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/logic-condition.png)

3. Change the first value to "size" (select "size" from variables) and the condition to "<="
4. Keep the second value as 0

![Setting game over condition](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-game-over-condition.png)

5. Inside the if block, add a **purple** `||game:game over||` block

![Game over block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/common/game-over.png)

6. Add a **purple** `||game:set game over message||` block after the game over block

![Game over set](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-game-over.png)

## Congratulations!

You've enhanced your Cookie Clicker game with:
- A moving cookie that bounces around the screen
- Cool visual effects when clicking the cookie
- Sound effects and camera shake for extra feedback
- A shrinking cookie that creates a time challenge
- A game over condition when the cookie gets too small

Here is the final code to check your progress.

![Final code](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/main/clicker/cookie-part2-final.png)

**What mods can you add to your code to make your game even better?**

- Add multiple cookies?
- Create power-ups that make the cookie grow again?
- Add different levels with faster cookies?
- Create a high score system?

Remember:
* **Green** blocks tell when things happen
* **Purple** blocks work with the mouse and game events
* **Blue** blocks control the scene and make decisions
* **Red** blocks control sprites
* **Pink** blocks handle score, music and info