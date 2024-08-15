## Minimal example of a custom scittle build using datascript as a plugin

### Setup
- go to the [plugins/demo](https://github.com/babashka/scittle/tree/main/plugins/demo) section of scittle
- uncomment datascript plugin in `plugins/demo/bb.edn` + remove hoplon/javelin (since I didn't need these)
- run `bb release` to generate the output `.js` artifacts
- copy the contents of `plugins/demo/resources` over to this repo
- add in an index.html inside `resources/public`, adding script tags to the appropriate `.js` files that you want to use. at a minimum, this will be `scittle.js` and `scittle.nrepl.js` (and in my case, `scittle.datascript.js`). 
- add a quick `.clj` file in to test to make the imports/code runs


### Development
- run `bb dev`
- go `localhost:1341` + refresh the page
- jack in to nrepl server @ `localhost:1339` + start coding!
    - for calva users like me, use the `Connect to a running REPL server, not in your project` + select `Generic`. This will allow you to directly enter the port on localhost that you want to connect to.