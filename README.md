# Webpack config

This config was designed for to make development a bit easier and more convenient. It supports out of the box such features as:

- Synchronization with browser (i.e. updating on every change in code)
- Source maps (dev mode)
- Files minimization (prod mode)
- Modern JS syntax (ES6+)
- Template engine (Handlebars)
- Typescript
- Sass / SCSS
- Local fonts

## Installation:

Clone repository:

```bash
git clone https://github.com/belyaevphil/webpack_config
```

or download archive [right here](https://github.com/belyaevphil/webpack_config/archive/master.zip).

## Usage:

Install packages:

```bash
npm i
```

and run the command down below to start to code:

```bash
npm run start
```

or run the command to build project:

```bash
npm run build
```

## Build and deployment (GitHub Pages):

Go to `webpack.prod.js` config file and change the value of this const to the name of your repo:

```js
const publicPath = '/webpack_config/';
```

Make sure you commit all changes before you go any further:

```bash
git add . && git commit -m "created last commit before build" && git push -u origin master
```

Run the command down below to build project (there will appear `dist` folder):

```bash
npm run build
```

Run the command to commit our built project:

```bash
git add dist && git commit -m "created last commit before deploy"
```

Run the command to push our project to GitHub Pages:

```bash
git subtree push --prefix dist origin gh-pages
```

Now you can go to repo `Settings`, scroll down to `GitHub Pages` section and enjoy your project on the Internet :).
