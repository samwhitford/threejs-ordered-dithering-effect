# threejs-ordered-dithering-effect
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
const orderedDitherEffect = new OrderedDitherPass(4);
composer.addPass( orderedDitherEffect );
```

The allowed values at this point are `4` and `8`.
These relate to the Bayer matrix threshold map size (i.e. 4x4 or 8x8).

## :pencil: License

This project is licensed under [MIT](https://opensource.org/licenses/MIT) license.
