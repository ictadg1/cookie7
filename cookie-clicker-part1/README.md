# Cookie Clicker Game - Part 1

## Introduction @unplugged
Author:
D.Antrobus 2025

In this tutorial, we will make a Cookie Clicker game! You will control a black square with your mouse and try to collect cookies to score points.

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-part1-preview.png)

## Step 1: Start your Game
First, we need the **green** `on start` block. This is where we'll put all the code that runs when your game begins.

On start block is automatically added
We'll add code inside it in the next steps

## Step 2: Set the background color @fullscreen

Let's add a **blue** `||scene:set background color to (color)||` block to make our game look nice.

![Setting background color](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-set-background.png)

1. Choose the block as shown below
2. Select the color "teal"
3. Drag the block into the **green** on start block 

![Set background color](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/clicker/cookie-background-color.png)

## Step 3: Create a cookie 
Now let's add a cookie that our player can click on. 

1. Find the **red** `||sprites:set mysprite to sprite[] of kind Player||` block.

![Set sprite block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/common/cookie-set-sprite.png)

2. Drag the set sprite block into the on start block as shown below
3. Change the kind from **Player** to **Food**

![Set sprite to Food](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/common/cookie-sprite-food.png)

## Step 4: Draw the cookie in the Image editor

1. Click on the grey box of the Sprite

![Edit sprite image](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/common/cookie-edit-sprite.png)

2. Set the canvas dimensions to 100 x 100 
3. Draw Cookie as shown below

![Draw cookie](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/common/cookie-draw-sprite.png)

## Step 5: Rename mySprite to Cookie

1. Click on mySprite down arrow as shown below

![Rename sprite variable](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-rename-variable.png)

2. Rename "mySprite" to Cookie

## Step 6: Set up the score 

We need to keep track of how many cookies we click on. Add the **pink** `||info:set score to||` block from the Info category.

![Set score block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-set-score.png)

3. Drag the set score to 0 block into the on start block as shown below

![Score added](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-score-added.png)

## Step 7: Create the player

Now we need to create a player that we can control. 

1. Add another **red** `||sprites:set sprite to||` block and change the sprite name to "player1".
```block
// @highlight
let player1 = sprites.create(img`
    f 
    `, SpriteKind.Player)
```

2. Drag the player1 set sprite to block into the on start block as shown below 

![Set player sprite](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-set-player.png)

## Step 8: Adjust player1 sprite

Click on the grey [ ] box on the Sprite
- Set x width to 1
- Set y height to 1
- Set color to black
- Use the pencil tool to click the black pixel

![Set player pixel](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-player-pixel.png)

## Step 9: Add mouse movement @fullscreen

We want our player to follow the mouse. Find the **purple** `||browser events:on mouse move||` block from the Browser category.

![Mouse move event](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-mouse-move.png)

## Step 10: Control the player

Now make the player follow your mouse cursor. 
1. Inside the `on mouse move` block, add the **red** `||sprites:set sprite position to||` block.
2. Drag the "x" label into the sprite 0 (x) position
3. Drag the "y" label into the sprite 0 (y) position 

![Set position to mouse](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-set-position.png)

## Step 11: Detect mouse clicks @fullscreen

We want to check if we've clicked a cookie when we click. 

1. Find the **purple** `||browser:on left mouse button Pressed||` block from the Browser category.

![Mouse button event](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-mouse-button.png)

2. Go to **light blue** logic library and select `||logic:if true then||`

![Logic if block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-logic-if.png)

3. Drag `||logic:if true then||` into the on mouse button pressed block

![If block added](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-if-added.png)

4. Go to **red** sprites library, scroll down to find `||sprites:is sprite overlapping with||`
![Sprite overlapping block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-sprite-overlaps.png)

5. Drag `||sprites:is sprite overlapping with||` into the if condition space

![Overlaps condition added](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-overlaps-added.png)

6. Click on mySprite and choose "player1"
7. Click on otherSprite and choose "cookie"

![Select sprites for overlap](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-select-sprites.png)

## Step 12: Check for cookie collection @fullscreen

Last step! Let's now add one to the score if player clicks on cookie

1. Select **pink** Info `||info:change score by 1||` block

![Change score block](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-change-score.png)

2. Drag `||info:change score by 1||` block into the `||logic:if then||` block as shown below

![Change score block added](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-change-score-added.png)

# Congratulations!

Did you finish all of the steps?

Here is the final code to check your progress.

![Final code](https://raw.githubusercontent.com/ictadg1/makecode-tutorial-images/refs/heads/master/images/cookie-part1-final.png)

**What mods can you add to your code to make your game even better?**

- Sound effects?
- Timer?

Remember:
* **Green** blocks tell when things happen
* **Purple** blocks work with the mouse
* **Blue** blocks make decisions
* **Red** blocks control sprites and score

Try [Part 2 of this tutorial](https://makecode.com/_part2link) to add more exciting features to your game!