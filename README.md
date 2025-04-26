# Cookie Clicker Arcade Game

## Introduction 4 @showdialog

Let's build a simple Cookie Clicker game! In this game, you'll click on a cookie sprite to earn points. The more you click, the more cookies you collect!

![Cookie clicker game](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie.png)

## Step 1: Create a cookie sprite @fullscreen

First, let's create a cookie sprite that players will click on.

```blocks
let cookie = sprites.create(img`
    . . . . . . e e e e . . . . . .
    . . . . e e 4 5 5 5 e e . . . .
    . . . e 4 5 6 2 2 7 6 5 e . . .
    . . e 5 6 6 7 2 2 6 7 7 6 e . .
    . e 5 5 7 7 7 6 6 7 7 7 5 5 e .
    . e 5 6 7 7 8 8 8 8 7 7 7 5 e .
    . e 5 5 7 7 8 8 8 8 7 8 7 5 e .
    e 4 5 5 6 7 8 7 7 8 7 8 6 5 4 e
    e 5 5 5 6 7 8 7 7 8 8 6 5 5 5 e
    e 5 5 5 6 6 8 8 8 8 7 6 5 5 5 e
    e 5 5 5 e 7 7 7 7 7 7 e 5 5 5 e
    e 5 5 e d 7 7 7 7 7 7 d e 5 5 e
    . e e d d d e e e e d d d e e .
    . . e d d e 5 5 5 5 e d d e . .
    . . . e e 5 5 5 5 5 5 e e . . .
    . . . . e 5 5 5 5 5 5 e . . . .
`, SpriteKind.Player)
cookie.setPosition(80, 60)
```

## Step 2: Create a score variable @fullscreen

Next, let's create a score variable to keep track of how many cookies we've clicked.

```blocks
let cookie: Sprite = null
let score = 0
info.setScore(0)
cookie = sprites.create(img`
    . . . . . . e e e e . . . . . .
    . . . . e e 4 5 5 5 e e . . . .
    . . . e 4 5 6 2 2 7 6 5 e . . .
    . . e 5 6 6 7 2 2 6 7 7 6 e . .
    . e 5 5 7 7 7 6 6 7 7 7 5 5 e .
    . e 5 6 7 7 8 8 8 8 7 7 7 5 e .
    . e 5 5 7 7 8 8 8 8 7 8 7 5 e .
    e 4 5 5 6 7 8 7 7 8 7 8 6 5 4 e
    e 5 5 5 6 7 8 7 7 8 8 6 5 5 5 e
    e 5 5 5 6 6 8 8 8 8 7 6 5 5 5 e
    e 5 5 5 e 7 7 7 7 7 7 e 5 5 5 e
    e 5 5 e d 7 7 7 7 7 7 d e 5 5 e
    . e e d d d e e e e d d d e e .
    . . e d d e 5 5 5 5 e d d e . .
    . . . e e 5 5 5 5 5 5 e e . . .
    . . . . e 5 5 5 5 5 5 e . . . .
`, SpriteKind.Player)
cookie.setPosition(80, 60)
```

## Step 3: Add click functionality @fullscreen

Now, let's make something happen when we click on the cookie!

```blocks
let cookie: Sprite = null
let score = 0
info.setScore(0)
cookie = sprites.create(img`
    . . . . . . e e e e . . . . . .
    . . . . e e 4 5 5 5 e e . . . .
    . . . e 4 5 6 2 2 7 6 5 e . . .
    . . e 5 6 6 7 2 2 6 7 7 6 e . .
    . e 5 5 7 7 7 6 6 7 7 7 5 5 e .
    . e 5 6 7 7 8 8 8 8 7 7 7 5 e .
    . e 5 5 7 7 8 8 8 8 7 8 7 5 e .
    e 4 5 5 6 7 8 7 7 8 7 8 6 5 4 e
    e 5 5 5 6 7 8 7 7 8 8 6 5 5 5 e
    e 5 5 5 6 6 8 8 8 8 7 6 5 5 5 e
    e 5 5 5 e 7 7 7 7 7 7 e 5 5 5 e
    e 5 5 e d 7 7 7 7 7 7 d e 5 5 e
    . e e d d d e e e e d d d e e .
    . . e d d e 5 5 5 5 e d d e . .
    . . . e e 5 5 5 5 5 5 e e . . .
    . . . . e 5 5 5 5 5 5 e . . . .
`, SpriteKind.Player)
cookie.setPosition(80, 60)

sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function(sprite, otherSprite) {
    if (controller.A.isPressed()) {
        info.changeScoreBy(1)
    }
})
```

## Step 4: Add animation effects @fullscreen

Let's add some visual feedback when the player clicks the cookie.

```blocks
let cookie: Sprite = null
let score = 0
info.setScore(0)
cookie = sprites.create(img`
    . . . . . . e e e e . . . . . .
    . . . . e e 4 5 5 5 e e . . . .
    . . . e 4 5 6 2 2 7 6 5 e . . .
    . . e 5 6 6 7 2 2 6 7 7 6 e . .
    . e 5 5 7 7 7 6 6 7 7 7 5 5 e .
    . e 5 6 7 7 8 8 8 8 7 7 7 5 e .
    . e 5 5 7 7 8 8 8 8 7 8 7 5 e .
    e 4 5 5 6 7 8 7 7 8 7 8 6 5 4 e
    e 5 5 5 6 7 8 7 7 8 8 6 5 5 5 e
    e 5 5 5 6 6 8 8 8 8 7 6 5 5 5 e
    e 5 5 5 e 7 7 7 7 7 7 e 5 5 5 e
    e 5 5 e d 7 7 7 7 7 7 d e 5 5 e
    . e e d d d e e e e d d d e e .
    . . e d d e 5 5 5 5 e d d e . .
    . . . e e 5 5 5 5 5 5 e e . . .
    . . . . e 5 5 5 5 5 5 e . . . .
`, SpriteKind.Player)
cookie.setPosition(80, 60)

controller.A.onEvent(ControllerButtonEvent.Pressed, function() {
    if (cookie.overlapsWith(cookie)) {
        info.changeScoreBy(1)
        cookie.startEffect(effects.ashes, 200)
        cookie.scale -= 0.05
        cookie.scale += 0.05
    }
})
```

## Step 5: Add sound effects @fullscreen

Now, let's add some sound effects when we click the cookie!

```blocks
let cookie: Sprite = null
let score = 0
info.setScore(0)
cookie = sprites.create(img`
    . . . . . . e e e e . . . . . .
    . . . . e e 4 5 5 5 e e . . . .
    . . . e 4 5 6 2 2 7 6 5 e . . .
    . . e 5 6 6 7 2 2 6 7 7 6 e . .
    . e 5 5 7 7 7 6 6 7 7 7 5 5 e .
    . e 5 6 7 7 8 8 8 8 7 7 7 5 e .
    . e 5 5 7 7 8 8 8 8 7 8 7 5 e .
    e 4 5 5 6 7 8 7 7 8 7 8 6 5 4 e
    e 5 5 5 6 7 8 7 7 8 8 6 5 5 5 e
    e 5 5 5 6 6 8 8 8 8 7 6 5 5 5 e
    e 5 5 5 e 7 7 7 7 7 7 e 5 5 5 e
    e 5 5 e d 7 7 7 7 7 7 d e 5 5 e
    . e e d d d e e e e d d d e e .
    . . e d d e 5 5 5 5 e d d e . .
    . . . e e 5 5 5 5 5 5 e e . . .
    . . . . e 5 5 5 5 5 5 e . . . .
`, SpriteKind.Player)
cookie.setPosition(80, 60)

controller.A.onEvent(ControllerButtonEvent.Pressed, function() {
    if (cookie.overlapsWith(cookie)) {
        info.changeScoreBy(1)
        cookie.startEffect(effects.ashes, 200)
        music.baDing.play()
        cookie.scale -= 0.05
        cookie.scale += 0.05
    }
})
```

## Step 6: Add upgrades! @fullscreen

Let's add an upgrade system that increases the points per click when you reach certain milestones.

```blocks
let cookie: Sprite = null
let pointsPerClick = 1
let score = 0
info.setScore(0)
cookie = sprites.create(img`
    . . . . . . e e e e . . . . . .
    . . . . e e 4 5 5 5 e e . . . .
    . . . e 4 5 6 2 2 7 6 5 e . . .
    . . e 5 6 6 7 2 2 6 7 7 6 e . .
    . e 5 5 7 7 7 6 6 7 7 7 5 5 e .
    . e 5 6 7 7 8 8 8 8 7 7 7 5 e .
    . e 5 5 7 7 8 8 8 8 7 8 7 5 e .
    e 4 5 5 6 7 8 7 7 8 7 8 6 5 4 e
    e 5 5 5 6 7 8 7 7 8 8 6 5 5 5 e
    e 5 5 5 6 6 8 8 8 8 7 6 5 5 5 e
    e 5 5 5 e 7 7 7 7 7 7 e 5 5 5 e
    e 5 5 e d 7 7 7 7 7 7 d e 5 5 e
    . e e d d d e e e e d d d e e .
    . . e d d e 5 5 5 5 e d d e . .
    . . . e e 5 5 5 5 5 5 e e . . .
    . . . . e 5 5 5 5 5 5 e . . . .
`, SpriteKind.Player)
cookie.setPosition(80, 60)

controller.A.onEvent(ControllerButtonEvent.Pressed, function() {
    if (cookie.overlapsWith(cookie)) {
        info.changeScoreBy(pointsPerClick)
        cookie.startEffect(effects.ashes, 200)
        music.baDing.play()
        cookie.scale -= 0.05
        cookie.scale += 0.05
        
        // Check for upgrades
        if (info.score() >= 10 && pointsPerClick == 1) {
            pointsPerClick = 2
            game.showLongText("Upgrade! Now you get 2 points per click!", DialogLayout.Bottom)
        } else if (info.score() >= 30 && pointsPerClick == 2) {
            pointsPerClick = 5
            game.showLongText("Upgrade! Now you get 5 points per click!", DialogLayout.Bottom)
        }
    }
})
```

## Step 7: Add a game goal @fullscreen

Let's add a goal for players to reach to win the game.

```blocks
let cookie: Sprite = null
let pointsPerClick = 1
let score = 0
let goalScore = 100
info.setScore(0)
cookie = sprites.create(img`
    . . . . . . e e e e . . . . . .
    . . . . e e 4 5 5 5 e e . . . .
    . . . e 4 5 6 2 2 7 6 5 e . . .
    . . e 5 6 6 7 2 2 6 7 7 6 e . .
    . e 5 5 7 7 7 6 6 7 7 7 5 5 e .
    . e 5 6 7 7 8 8 8 8 7 7 7 5 e .
    . e 5 5 7 7 8 8 8 8 7 8 7 5 e .
    e 4 5 5 6 7 8 7 7 8 7 8 6 5 4 e
    e 5 5 5 6 7 8 7 7 8 8 6 5 5 5 e
    e 5 5 5 6 6 8 8 8 8 7 6 5 5 5 e
    e 5 5 5 e 7 7 7 7 7 7 e 5 5 5 e
    e 5 5 e d 7 7 7 7 7 7 d e 5 5 e
    . e e d d d e e e e d d d e e .
    . . e d d e 5 5 5 5 e d d e . .
    . . . e e 5 5 5 5 5 5 e e . . .
    . . . . e 5 5 5 5 5 5 e . . . .
`, SpriteKind.Player)
cookie.setPosition(80, 60)

game.onUpdate(function() {
    if (info.score() >= goalScore) {
        game.over(true)
    }
})

controller.A.onEvent(ControllerButtonEvent.Pressed, function() {
    if (cookie.overlapsWith(cookie)) {
        info.changeScoreBy(pointsPerClick)
        cookie.startEffect(effects.ashes, 200)
        music.baDing.play()
        cookie.scale -= 0.05
        cookie.scale += 0.05
        
        // Check for upgrades
        if (info.score() >= 10 && pointsPerClick == 1) {
            pointsPerClick = 2
            game.showLongText("Upgrade! Now you get 2 points per click!", DialogLayout.Bottom)
        } else if (info.score() >= 30 && pointsPerClick == 2) {
            pointsPerClick = 5
            game.showLongText("Upgrade! Now you get 5 points per click!", DialogLayout.Bottom)
        }
    }
})
```

## Complete! @showdialog

Congratulations! You've created a simple Cookie Clicker game! Try to reach 100 points to win!

Here are some ways to expand your game:
- Add more upgrades
- Add a timer
- Create different types of cookies that give different points
- Add automatic cookie generation over time

Happy coding!
