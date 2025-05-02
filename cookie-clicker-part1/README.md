
# Cookie Clicker Game

## Introduction @unplugged
Author:
D.Antrobus 2025

In this tutorial, we will make a Cookie Clicker game! You will control a black square with your mouse and try to collect cookies to score points.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie.png)

## Step 1: Start your Game
First, we need the **green** `on start` block. This is where we'll put all the code that runs when your game begins.

On start block is automatically added
We'll add code inside it in the next steps


```blocks
// On start block is automatically added
// We'll add code inside it in the next steps
```

## Step 2: Set the background color @fullscreen

Let's add a **blue** `||scene:set background color to (color)||` block to make our game look nice.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-background.png)

1. Choose the block as shown below
2. Select the color "teal"
3. Drag the block into the **green** on start block 

```blocks
// @highlight
scene.setBackgroundColor(6)
```

## Step 3: Create a cookie 
Now let's add a cookie that our player can click on. 

1. Find the **red** `||sprites:set mysprite to sprite[] of kind Player||` block.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-sprite.png)

`2`. Drag the set sprite block into the on start block as shown below

```blocks
scene.setBackgroundColor(6)
// @highlight
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player)
```

## Step 4: Draw the cookie in the Image editor

1. Click on the grey box of the Sprite

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-sprite-edit.png)

`2.` Set the canvas dimensions to 100 x 100 
`3.` Draw Cookie as shown below

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-draw-cookie.png)


## Step 5. Rename mySprite to Cookie

1. Click on mySprite down arrow as shown below

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-rename-variable.png)

`2.` Rename "mySprite" to Cookie

## Step 6: Set up the score 

We need to keep track of how many cookies we click on. Add the **pink** `||info:set score to||` block from the Info category.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-info-set-score.png)

`3.` Drag the set score to 0 block into the on start block as shown below

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-step-6.png)


## Step 7: Create the player

Now we need to create a player that we can control. 

`1.` Add another **red** `||sprites:set sprite to||` block and change the sprite name to "player1".
```block
// @highlight
let player1 = sprites.create(img`
    f 
    `, SpriteKind.Player)
```

`2.` Drag the player1 set sprite to block into the on start block as shown below 

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-step-7.png)

## Step 8: Adjust player1 sprite

Click on the grey [ ] box on the Sprite
- Set x width to 1
- Set y height to 1
- Set color to black
- Use the pencil tool to click the black pixel

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-step-8.png)


## Step 9: Add mouse movement @fullscreen

We want our player to follow the mouse. Find the **purple** `||browser events:on mouse move||` block from the Browser category.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-browser-mouse-move.png)


## Step 10: Control the player

Now make the player follow your mouse cursor. 
1. Inside the `on mouse move` block, add the **red** `||sprites:set sprite position to||` block.
2. Drag the "x" label into the sprite 0 (x) position
3. Drag the "y" label into the sprite 0 (y) position 

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/step8.mov.gif)


## Step 11: Detect mouse clicks @fullscreen

We want to check if we've clicked a cookie when we click. 

`1.` Find the **purple** `on left mouse button Pressed` block from the Browser category.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-browser-click.png)

`2.` Go to **light blue** logic library and select `||logic:if true then||`

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-logic-if.png)

`3.` Drag `||logic:if true then||` into the on mouse button pressed block

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-step-11-1.png)

`4.` Go to **blue** sprites library, scroll down to find `||sprites:mySprite overlaps with otherSprite||`
![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-sprite-overlaps.png)

`5.` Drag `||sprites:mySprite overlaps with otherSprite||` into the if block as shown below

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-step-11.png)

`6.` Click on mySprite and choose "player1"

`7.` Click on otherSprite and choose "cookie"

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-step-11-2.png)


## Step 12: Check for cookie collection @fullscreen

Last step! Let's now add one to the score if player clicks on cookie

`1.` Select **pink** Info `||info:change score by 1||` block

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-info-change-score.png)

`2.` Drag `||info:change score by 1||` block into the `||logic:if then||` block as shown below

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-step-12.png)

# Congratulations!

Did you finish all of the steps?

Here is the final code to check your progress.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-finished.png)

** What mods can you add to your code to make your game even better?**

- Sound effects?
- Timer?

Remember:
* **Green** blocks tell when things happen
* **Purple** blocks work with the mouse
* **Blue** blocks make decisions
* **Red** blocks control sprites and score