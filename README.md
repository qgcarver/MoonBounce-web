# MoonBounce
## Demo
https://qgcarver.github.io/MoonBounce-web (Only works with touchscreens)
### Miller Column object viewer
![demo](https://github.com/qgcarver/MoonBounce-web/blob/main/Screenshot_20240915_050341_Chrome.jpg)
### WebGL graphics with HTML5 Canvas
![graphics demo](https://github.com/user-attachments/assets/0c7f1458-cec1-4ef2-b033-dc5bb1dc4cfa)
### Hot Reloading
<video src='https://github.com/user-attachments/assets/b0516355-a415-43b8-8169-9899cb9184d5' width=180></video>

## What is this?
MoonBounce is an inspector-based Jupyter Notebook-style IDE project.
Most of the work I've done with this project exists in a private dev image, but
you can use the base-line image to do your own stuff. It's all done client-side,
in fact you could grab the bundle and html from the a github pages action to 
just host yourself with `python http.server` or whatever you like.

## Some information on built-in stuff.
The `DOM` object has a reference to `document` and `window` which should give
you full control over the browser environment.

The `prsv` variable will act as local storage, which you can save or download
with `save-prsv` and `download-prsv` respectively. And you can download or
upload general text with `DOM.dlstr` and `DOM.upstr`. If the function returns
a Javascript promise, you'll need to call `<prom>:await()`.

Using localStorage you can patch the `boot` variable on reload to update the
initial environment. This is really only useful for extending the console.

## Building
`npm run build` builds the application to `public/bundle.js`, along with a sourcemap file for debugging.
`npm run dev` will run `npm start` and `npm run watch` in parallel.

## Dependencies (informal list)
- rollup
- wasmoon (Wasm implementation of Lua)
- fennel

## License
[AGPL3](LICENSE).
