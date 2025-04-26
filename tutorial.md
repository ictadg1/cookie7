# Cookie Clicker Game Tutorial

In this tutorial, we'll create a simple Cookie Clicker game where players click a cookie to earn points!

## Step 1: Create a cookie sprite

First, let's create a cookie sprite that players will click.

- Click on the **Sprites** toolbox category
- Find and use `sprites.create` to make a new sprite
- Draw a cookie or use `assets.image` with a built-in image
- Position your cookie in the center of the screen

```blocks
let myCookie = sprites.create(assets.image`cookie`, SpriteKind.Player)
myCookie.setPosition(80, 60)
```

## Step 2: Add a score variable

Next, we'll create a variable to keep track of how many cookies we've clicked.

- Click on the **Variables** toolbox category
- Create a new variable called `score`
- Set its starting value to 0
- Use `info.setScore(0)` to display it on screen

```blocks
let score = 0
info.setScore(score)
```

## Step 3: Make the cookie clickable

Now let's make the cookie respond when we click it.

- Find the `on sprite pressed` block in the **Sprites** category
- Select your cookie sprite
- Inside this block, we'll add code to increase the score

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    score += 1
    info.setScore(score)
})
```

## Step 4: Add animation when clicked

Let's make the cookie grow slightly when clicked and then return to normal size.

- Inside the `on sprite pressed` block
- Use `scale` to make the cookie bigger briefly
- Then use `scale` again to return it to normal size

```blocks
let myCookie: Sprite = null
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    score += 1
    info.setScore(score)
    myCookie.scale = 1.2
    pause(100)
    myCookie.scale = 1
})
```

## Step 5: Add cookie upgrades

Let's add a feature to make each click worth more after reaching certain scores.

- Add a new variable called `clickValue`
- Set its starting value to 1
- Create a `forever` loop that checks your score
- Increase `clickValue` at certain score milestones

```blocks
let clickValue = 1
forever(function () {
    if (score == 10) {
        game.showLongText("Upgrade! Clicks now worth 2 points!", DialogLayout.Bottom)
        clickValue = 2
    }
    if (score == 30) {
        game.showLongText("Upgrade! Clicks now worth 5 points!", DialogLayout.Bottom)
        clickValue = 5
    }
})
```

## Step 6: Use the click value

Update the score increase to use our `clickValue` variable:

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    score += clickValue
    info.setScore(score)
    myCookie.scale = 1.2
    pause(100)
    myCookie.scale = 1
})
```

## Step 7: Add sound effects

Add sounds when clicking the cookie or getting an upgrade.

- Find the `play sound` block in the **Music** category
- Add it inside your sprite pressed event
- Add different sounds for upgrades

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
    score += clickValue
    info.setScore(score)
    myCookie.scale = 1.2
    music.baDing.play()
    pause(100)
    myCookie.scale = 1
})
```

## Step 8: Create a game goal

Finally, let's add a win condition when the player reaches 100 cookies.

- Use an `if` statement to check the score
- Show a win message and effects when the goal is reached

```blocks
forever(function () {
    if (score >= 100) {
        game.over(true)
        game.showLongText("You are a master cookie clicker!", DialogLayout.Center)
    }
})
```

That's it! You've now created a basic Cookie Clicker game. Try adding more upgrades or custom graphics to make the game your own!