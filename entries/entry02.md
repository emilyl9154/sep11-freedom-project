# Entry 2
##### 12/12/22

My tool is melonJS and I tinkered with it by adding some code in the player.js file from the [platformer game example on GitHub](https://github.com/melonjs/examples/tree/master/platformer). Using the documentation, I changed it so pressing G will turn the gravity off, pressing Q will make the player move up, pressing E will move the player down, and pressing B will make the player bounce when it touches the ground.

I first made/binded new keys:
```js
me.input.bindKey(me.input.KEY.Q,  "up");
me.input.bindKey(me.input.KEY.E,  "down");
me.input.bindKey(me.input.KEY.G,  "gravity");
me.input.bindKey(me.input.KEY.B,  "bounce");
```

#### Turn off gravity using G key
To turn off the gravity I used the [`ignoreGravity`](https://melonjs.github.io/melonJS/docs/melonjs/Body.html#ignoreGravity) property of the `body` class.
```js
if (me.input.isKeyPressed("gravity")){
    this.body.ignoreGravity = true;
}
```
This causes the player to stick to the object above it and stay there even if there is no object above it.

#### Bounce using B key
To make the player bounce, I used the [`bounce`](https://melonjs.github.io/melonJS/docs/melonjs/Body.html#bounce) property of the `body` class.
```js
if (me.input.isKeyPressed("bounce")){
    this.body.bounce = 1;
}
```

#### Move up and down using Q and E keys
To make the player move up/down when Q/E is pressed, I used the already existing code to change the direction from left/right to up/down. I did this by changing `this.body.force.x` to `this.body.force.y` and `this.body.maxVel.x` to `this.body.maxVel.y`.
```js
if (me.input.isKeyPressed("down")){
    this.body.force.y = this.body.maxVel.y;
}

if (me.input.isKeyPressed("up")){
    this.body.force.y = -this.body.maxVel.y;
}
```
This causes the player to move up and down along the y axis.

My goal for winter break is to do any missing assignments that I have for other classes.
I am on stage 2 of the Engineering Design Process, "Researching the problem" because I am using the MelonJS docs to tinker with my tool.
The skills I grew in are "How to read" and "How to learn" because I had to read the documentation so I could tinker with MelonJS.
[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)