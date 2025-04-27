
# Cookie Clicker Game

## Introduction @unplugged

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


## Step 9: Control the player

Now make the player follow your mouse cursor. 
1. Inside the `on mouse move` block, add the **red** `||sprites:set sprite position to||` block.
2. Drag the "x" label into the sprite 0 (x) position
3. Drag the "y" label into the sprite 0 (y) position 

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/step8.mov.gif)


## Step 8: Detect mouse clicks @fullscreen

We want to check if we've collected a cookie when we click. Find the **purple** `on left mouse button Pressed` block from the Browser category.

```blocks
// @highlight
browserEvents.MouseLeft.onEvent(browserEvents.MouseButtonEvent.Pressed, function (x, y) {
    
})
```

## Step 9: Check for cookie collection @fullscreen

Let's add code to check if the player is touching the cookie. Inside the mouse click block, add the **blue** `if sprite overlaps with` block.

```blocks
let player1: Sprite = null
let Cookie: Sprite = null
// @highlight
browserEvents.MouseLeft.onEvent(browserEvents.MouseButtonEvent.Pressed, function (x, y) {
    if (player1.overlapsWith(Cookie)) {
        
    }
})
```

## Step 10: Score points @fullscreen

Finally, let's add a point to our score when we collect a cookie. Inside the if block, add the **red** `change score by` block.

```blocks
let player1: Sprite = null
let Cookie: Sprite = null
browserEvents.MouseLeft.onEvent(browserEvents.MouseButtonEvent.Pressed, function (x, y) {
    if (player1.overlapsWith(Cookie)) {
        // @highlight
        info.changeScoreBy(1)
    }
})
```

## Complete! @unplugged

Great job! You've made a Cookie Collector game!

How to play:
* Move your mouse to control the black square
* When you touch the cookie, click the left mouse button
* Each time you click when touching the cookie, you get 1 point
* Try to get as many points as you can!

Here's your complete program:

```blocks
browserEvents.MouseLeft.onEvent(browserEvents.MouseButtonEvent.Pressed, function (x, y) {
    if (player1.overlapsWith(Cookie)) {
        info.changeScoreBy(1)
    }
})
browserEvents.onMouseMove(function (x, y) {
    player1.setPosition(x, y)
})
let player1: Sprite = null
let Cookie: Sprite = null
scene.setBackgroundColor(6)
Cookie = sprites.create(img`
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . e e e e e e . . . . . 
    . . . . e e e e e e e e . . . . 
    . . . e e e d d d d e e e . . . 
    . . . e e d d d d d d e e . . . 
    . . . e e d d d d d d e e . . . 
    . . . e e d d d d d d e e . . . 
    . . . e e e d d d d e e e . . . 
    . . . . e e e e e e e e . . . . 
    . . . . . e e e e e e . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . .
`, SpriteKind.Player)
info.setScore(0)
player1 = sprites.create(img`
    f 
    `, SpriteKind.Player)
```

Remember:
* **Green** blocks tell when things happen
* **Purple** blocks work with the mouse
* **Blue** blocks make decisions
* **Red** blocks control sprites and score