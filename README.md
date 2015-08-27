# jsonToSass loader for webpack

## Usage

Forked from gist: [jsonToSassVars](https://gist.github.com/Kasu/ea4f4861a81e626ea308) and [prepend-loader](https://gist.github.com/Kasu/29452051023ff5337bd7)

In your webpack.config.js add the following;

``` javascript
var sassGlobals = require('[vars].json');
var sass = JSON.stringify(sassGlobals);
// => returns [vars].json content as string
var webpackConfig = {
    module: {
        loaders:[
            {test: /.scss$/, loader: "style!css!sass!jsontosass?" + sass}
        ]
    },
}

```





## License

MIT (http://www.opensource.org/licenses/mit-license.php)