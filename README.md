# Mashup Template

This starter kit comes with:
- [Yarn](https://yarnpkg.com/): A fast dependency manager
- [Webpack](https://webpack.js.org) setup for [production](./config/webpack.prod.js) and [development](./config/webpack.dev.js) environments
- Live reload with [webpack-dev-server](https://github.com/webpack/webpack-dev-server)
- [Babeljs](https://babeljs.io/) to compile next generation JavaScript
- [HTML Webpack Plugin](https://github.com/ampedandwired/html-webpack-plugin): Especially useful for webpack bundles that include a hash in the filename which changes every compilation. With this plugin you write a [HTML template](./src/index.html) and the plugin takes care of inserting the `.js` and `.css` script for you whenever your code changes and gets compiled.
- [css-loader](https://github.com/webpack/css-loader) and [style-loader](https://github.com/webpack/style-loader) to loader your css and put into your `.js` bundle when in dev mode or load the css and put it in a separate folder when in production mode with [extract-text-webpack-plugin](https://github.com/webpack/extract-text-webpack-plugin)
- [url-loader](https://github.com/webpack/url-loader) used to load your images into your bundle. This plugin can return a Data Url if the file is smaller than a byte limit. That means if you have an image file which is less than a size lime you have specified on your webpack config that assets gets bundled inline, otherwise it is copied to to your dist folder with [file-loader](https://github.com/webpack/file-loader). Hence, when you add `url-loader` to your `devDependencies` you also have to add `file-loader` cuz it's a peer dependencie.

### Getting Started

To get started, clone the repo and run `yarn install`, or `npm install` if you are using `npm`. I recommend [Yarn](https://yarnpkg.com/) because it's fast than npm and also enables you to have a cache on your machine so you don't waste your bandwidth having to download everything whenever your run `npm install`.

```sh
git clone --depth=1 <git url> project-name
cd project-name
yarn install
# or
npm install
```

> You have to have Node (version >= 6) installed on your machine. 

### Running in development mode
```sh
yarn start
# or
npm start # I haven't tested it with npm though
```

The app is available on [localhost:5000](http://localhost:5000)

### Building for production
```sh
yarn run build
# or
npm run build
```

### Linting

```sh
yarn run lint
# or to autofix
yarn run lint:fix
# or 
npm run lint
# or to autofix
npm run lint:fix
```

### Very Helpful resources

[webpack](https://webpack.js.org/)
[The PRPL Pattern](https://developers.google.com/web/fundamentals/performance/prpl-pattern/)
[Webpack 3 + React — Production build tips](https://medium.com/netscape/webpack-3-react-production-build-tips-d20507dba99a)
[nwb](https://github.com/insin/nwb)
[On Webpack and Source Map integration](https://lorefnon.me/2016/12/03/on-webpack-and-source-map-integration.html)
[Conditional compilation and dead code elimination with webpack](https://www.thomann.io/blog/post/webpack_conditional_compilation_dead_code_elimination)
