 # Cookie Clicker Arcade Game 7

## Introduction @showdialog

Let's build a simple Cookie Clicker 7 game! In this game, you'll click on a cookie sprite to earn points. The more you click, the more cookies you collect! Cool Huh?
![Cookie clicker game 4](https://raw.githubusercontent.com/ictadg1/cookie7/refs/heads/master/images/cookie.png)

## Step 1: Create a cookie sprite @fullscreen

First, let's create a delicious cookie sprite that players will click on.

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