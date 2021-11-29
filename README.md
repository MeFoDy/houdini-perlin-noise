# CSS Houdini Perlin Noise

A CSS Houdini Paint Worklet that draws a Perlin Noise as a background image.

[![CSS Houdini Perlin Noise](https://github.com/mefody/houdini-perlin-noise/blob/main/assets/css-houdini-perlin.png?raw=true)](https://mefody.github.io/houdini-perlin-noise/)

Demo: [https://mefody.github.io/houdini-perlin-noise/](https://mefody.github.io/houdini-perlin-noise/)

## Installation

You can install the `houdini-perlin-noise` using NPM.

```bash
npm install houdini-perlin-noise
```

Also you can clone [the `houdini-perlin-noise` repo](https://github.com/mefody/houdini-perlin-noise/).

## Build

```bash
npm install
npm run build
```

The built file will be in the `./dist` folder.

## Usage

Load the module in the `dist/worklet.js` file and add it to the Paint Worklet.

```js
if ('paintWorklet' in CSS) {
    CSS.paintWorklet.addModule('path/to/worklet.js');
}
```

Then set the `background-image` property of some DOM-element to `paint(perlin-noise)`.

```css
.element {
    background-image: paint(perlin-noise);
}
```

## Run demo locally

```bash
npm run dev
```

## Configuration

| property | description | default value |
| -------- | ----------- | ------------- |
| --perlin-color | **Color of lines**, (color) | `#ecee81` |
| --perlin-bg-color | **Color of background**, (color) | `tomato` |
| --perlin-x | **Magic number for axis X** (number, > 1) | `5` |
| --perlin-y | **Magic number for axis Y** (number, > 1) | `5` |
| --perlin-z | **Magic number for axis Z** (number) | `0` |
| --perlin-line-width | **Stroke width**, (number) | `1` |

### Example

```css
.element {
    --perlin-color: #ecee81;
    --perlin-bg-color: tomato;
    --perlin-line-width: 1;
    --perlin-x: 5;
    --perlin-y: 5;
    --perlin-z: 0;

    background-image: paint(perlin-noise);
}
```

## License

`houdini-perlin-noise` is released under the MIT public license. See the enclosed `LICENSE` for details.