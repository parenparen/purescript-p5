# purescript-p5

p5.js bindings for PureScript

*Disclaimer: This project has just been started and the API is still very unstable.*

* [Module documentation](generated-docs/P5.md)

There are still a large percentage of p5.js functions that have not yet been implemented (see [unsupported.md](unsupported.md)).

## Installation

This library depends on p5.js. This dependency may be satisfied by installing the NPM [p5.js package](https://www.npmjs.com/package/p5).

```
npm install p5 --save
```

## Running the examples

The examples use the webpack DLLPlugin to improve build performance. To run the examples, first build the dll bundle with:

```
npm run webpack:dll
```

This creates a separate webpack bundle for dependencies so that they don't need to be regenerated each time the app is changed.

To start webpack dev server, run:

```
npm run webpack:server
```

With webpack dev server running, examples can be viewed in a browser by visiting ```localhost:4008/examples/path-to-example```.

## Project Status

Most of the FFI as been auto-generated from the p5.js YUIDoc. There are still a large number of functions that couldn't be auto-generated, sometimes because of missing type information in the YUIDoc (see [unsupported.md](unsupported.md)). These might have to be written by hand.

Completed:
  * generate FFI PureScript functions for basic p5.js types (e.g. Number, String, Boolean)

TODO:
  * generate FFI for more complicated p5.js types (e.g. p5.Color, p5.Vector)
  * support functions with greater than 10 arguments (the library uses runFn, which is only defined for functions of at most 10 arguments) 
  * generate comments for FFI functions so that purescript-p5 documentation can be auto-generated by pulp
  * support functions that accept product types
  * complete hello-p5-simple-shapes example

## References

Many of the examples are based on the p5.js examples on the [p5.js reference site](https://p5js.org/examples/), and are licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

