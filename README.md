## Download Bootstrap via NPM

`npm install -S bootstrap`  
Documentation: https://getbootstrap.com/docs/4.3/getting-started/download/#npm

## File structure

Documentation: https://getbootstrap.com/docs/4.3/getting-started/theming/#file-structure

## Build tools

`npm install -D node-sass concat postcss-cli autoprefixer`

npm scripts:

```
    "watch:sass": "node-sass sass/custom.scss css/style.css -w",
    "compile:sass": "node-sass sass/custom.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b \"last 10 versions \" css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build": "npm-run-all compile:sass concat:css prefix:css compress:css",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass"
```
