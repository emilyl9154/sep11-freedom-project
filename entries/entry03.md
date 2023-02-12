# Entry 3
##### 2/3/23

My tool is melonJS and I tinkered with it by making the player sprint when they hold Shift on their keyboard.
Like the previous blog entry, I [binded a new key](https://melonjs.github.io/melonJS/docs/melonjs/input/bindKey.html) by doing `me.input.bindKey(me.input.KEY.SHIFT, "sprint");` in the player.js file.
Then I did:
```js
if (me.input.isKeyPressed("sprint")){ // SHIFT
    this.body.setMaxVelocity(10, 15);
}
else {
    this.body.setMaxVelocity(3, 15);
}
```
The player's speed (`maxVelocity`) is being set to 10 when the game detects Shift is being pressed, and it resets to 3 when Shift is released.
I also decreased the audio's volume to 0.5 in index.js by using [audio.setVolume](https://melonjs.github.io/melonJS/docs/melonjs/audio/setVolume.html): `me.audio.setVolume(0.5);`.
I tried to make text appear on the screen using [BitmapText](https://melonjs.github.io/melonJS/docs/melonjs/BitmapText.html) but it didn't work.

I think I am still on stage 2 of the Engineering Design Process because I am learning about my tool. The skills I grew in were "how to read", "how to google" and "how to learn" because I used the documentation and Google to learn my tool.
I plan on editing the map/textures in the template next, by using Krita and Tiled.


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)