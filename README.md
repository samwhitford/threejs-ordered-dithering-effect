# threejs-ordered-dithering-effect
![](pixelated_dithered_checkerboard_torus.gif)

Threejs post-processing shader to apply an ordered dithering effect

Copy provided files into your threejs project.

Ensure you're using EffectComposer and RenderPass.
[Guide here](https://threejs.org/docs/#manual/en/introduction/How-to-use-post-processing)

Import the effect like so:
```js
import { OrderedDitherPass } from './OrderedDitherPass.js'
```

Initialise like so:
```js
const orderedDitherEffect = new OrderedDitherPass(mapSize, scale);
composer.addPass( orderedDitherEffect );
```

`mapSize` refers to the Bayer matrix threshold map size.

This can be a value of `2`, `4` or `8` at this time.

`scale` refers to the scale of the effect. This is locked to increments of `0.5` (i.e. 1, 1.5, 2, 2.5 and so on). other values can be entered but the value will be sanitised by the shader.

Default values will be applied if none are provided (mapSize: 4, scale: 1)


## :pencil: License

This project is licensed under [MIT](https://opensource.org/licenses/MIT) license.

## :loudspeaker: Shout outs!

Hugh Kennedy for this repo - https://github.com/hughsk/glsl-dither
