# tween.js  

JavaScript tweening engine for easy animations, incorporating optimised Robert Penner's equations.

```javascript
var coords = { x: 0, y: 0 };
var tween = new TWEEN.Tween(coords)
	.to({ x: 100, y: 100 }, 1000)
	.onUpdate(function() {
		console.log(this.x, this.y);
	})
	.start();

requestAnimationFrame(animate);

function animate(time) {
	requestAnimationFrame(animate);
	TWEEN.update(time);
}
```

## Installation

Download the [library](https://raw.githubusercontent.com/tweenjs/tween.js/master/src/Tween.js) and include it in your code:

```html
<script src="js/Tween.js"></script>
```

### More advanced users might want to...

#### Use `npm`

```bash
npm install tween-play-pause
```
