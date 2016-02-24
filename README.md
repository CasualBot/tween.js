# Tween-Play-Pause

This is a derivative of the [Tween.JS](https://github.com/tweenjs/tween.js) library by [Sole](https://github.com/sole) on [Github.com](https://github.com/tweenjs/tween.js).
For more documentation head over to their repository.

JavaScript tweening engine for easy animations, incorporating optimised Robert Penner's equations.

```javascript
// Start position coordinates
var coords = { x: 0, y: 0 };

//Time tween will animate from start point to end point in milliseconds 
var duration = 1000; 

// End coordinates 
// End Position coords can also be an array of positions 
// var endX = [0, 100, 200, 300]; var endY = [0, 100, 200, 300];
// Ex:  .to({ x: endX, y: endY }, duration) ...

var endCoords = { x: 100, y: 100 };

var tween = new TWEEN.Tween(coords)
	.to(endCoords, duration)
	.onUpdate(function() {
	    //Show position of Tween
		console.log(this.x, this.y);
		//Animate the coords using x and y passed through
		coords.x = this.x;
		coords.y = this.y;
	})
	.start();

requestAnimationFrame(animate);

function animate(time) {
	requestAnimationFrame(animate);
	TWEEN.update(time);
}

//Play Tween
tween.play();

//Pause Tween
tween.pause();

```

## Installation

Download the [library](https://raw.githubusercontent.com/CasualBot/tween.js/master/src/Tween.js) and include it in your code:

```html
<script src="js/Tween.js"></script>
```

### More advanced users might want to...

#### Use `npm`

```bash
npm install tween-play-pause
```
