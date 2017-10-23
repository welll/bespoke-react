# bespoke-react

> Bootstrap project for easily generate Bespoke presentations using React

## I want to create my own presentation
Great! That's pretty easy. All you have to do is:

```sh
# First, clone this repo
git clone git@github.com:diegomura/bespoke-react.git

# Navigate to the project and delete the git history
cd bespoke-react
rm -rf .git

# Install the dependencies
npm install

# Initialize the development server
npm start
```
<p align="right">* you can use Yarn instead of npm if you prefer</p>

## Creating a new slide
All you need to do is creating a new `SlideXX.js` (being `XX` consecutive ascending numbers) file into the `slides` directory and leave the rest to bespoke-react. Your slide will be _automagically_ added to the presentation in the order you specified. Remember that to make it work, each file should export a valid React component.

## Setup Bespoke
This project tries to be the more _unopinionated_ as possible. This means letting you define what Bespoke plugins you want to use. To add a new plugin, just go to your `src/index.js` and add one more element to the `plugins` array:

```js
import somePlugin from 'some-plugin';

const plugins = [
  // ... more plugins
  somePlugin(),
];
```

## Building
To build the project, just run:

```sh
npm run build
# or
yarn build
```

You will see the output in the `dist` folder of your project.

## Publishing to Github pages
_TODO_

## License
MIT © [Diego Muracciole](http://github.com/diegomura)
