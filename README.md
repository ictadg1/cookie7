
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

Let's add a **green** `||scene:set background color to (color)||` block to make our game look nice.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-background.png)

- Choose the color as shown in the blocks below

```blocks
// @highlight
scene.setBackgroundColor(6)
```

## Step 3: Create a cookie @fullscreen


Now let's add a cookie that our player can collect. Find the **red** `||sprites:set mysprite to sprite[] of kind Player||` block and change the sprite name to "Cookie".

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie-7-set-sprite.png)

```blocks
scene.setBackgroundColor(6)
// @highlight
let Cookie = sprites.create(img`
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
```

## Step 4: Set up the score @fullscreen

We need to keep track of how many cookies we collect. Add the **red** `set score to` block from the Info category.

```blocks
scene.setBackgroundColor(6)
let Cookie = sprites.create(img`
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
// @highlight
info.setScore(0)
```

## Step 5: Create the player @fullscreen

Now we need to create a player that we can control. Add another **red** `set sprite to` block and change the sprite name to "player1".

```blocks
scene.setBackgroundColor(6)
let Cookie = sprites.create(img`
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
// @highlight
let player1 = sprites.create(img`
    f 
    `, SpriteKind.Player)
```

## Step 6: Add mouse movement @fullscreen

We want our player to follow the mouse. Find the **purple** `on mouse move` block from the Browser category.

```blocks
// @highlight
browserEvents.onMouseMove(function (x, y) {
    
})
```

## Step 7: Control the player @fullscreen

Now make the player follow your mouse cursor. Inside the `on mouse move` block, add the **red** `set sprite position to` block.

```blocks
let player1: Sprite = null
// @highlight
browserEvents.onMouseMove(function (x, y) {
    player1.setPosition(x, y)
})
```

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