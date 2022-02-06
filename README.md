# purescript-codegen
All relevant code to reading and generating purescript. Also contains stuff related to typescript. This readme also links to repositories that do not fall under the organization but are still relevant to codegen.

## Purescript

### Parsing
[language-cst-parser](https://github.com/natefaubion/purescript-language-cst-parser)

### Printing
[language-cst-parser](https://github.com/natefaubion/purescript-language-cst-parser) can also print. But [tidy-codegen](https://github.com/natefaubion/purescript-tidy-codegen) is recommended as it is more convenient to use (uses language-cst-parser under the hood)

## TypeScript

### Purescript to DTS
[tsd-gen](https://github.com/minoki/purescript-tsd-gen) (haskell)

### DTS to Purescript
[read-dts](https://github.com/purescript-codegen/purescript-read-dts) contains the following parts:

* ts-compiler extensive bindings to the [typescript compiler](https://github.com/purescript-codegen/purescript-read-dts/tree/master/src/TypeScript/Compiler)
* ts-repr is an intermediate representation (IR) that simplifies the types found in the typescript compiler. Currently only typescript types to ts-repr is possible. ts-repr back into typescript types is planned for the future.
* ts-codegen convert ts-repr IR into purescript using various strategies. Purescript back into ts-repr might be added in the far future.

### related projects to typescript codegen
* [Typescript compiler API - using the type checker](https://github.com/microsoft/TypeScript/wiki/Using-the-Compiler-API#using-the-type-checker)
* Generate json-schema from your Typescript sources: [typescript-json-schema](https://github.com/YousefED/typescript-json-schema). This is useful to see how the typescript compiler works and which information can be extracted from it.
* [auth0](https://auth0.github.io/auth0-spa-js/index.html) uses [typedoc](https://typedoc.org/) for docs generation.
* TypeScript d.ts file generate from JSON Schema file: [dtsgenerator](https://github.com/horiuchi/dtsgenerator) and [ts-json-schema-generator](https://github.com/vega/ts-json-schema-generator).

## old repositories
* [ps-cst](https://github.com/purescript-codegen/purescript-ps-cst) good working repository with purescript parser and printer
* [cst-simple](https://github.com/purescript-codegen/purescript-cst-simple) printer for ps-cst
* [js-ast](https://github.com/purescript-codegen/purescript-js-ast) proof of concept
* [ps-past](https://github.com/purescript-codegen/purescript-ps-past) extracted from purescript-in-purescript
* [purescript-in-purescript](https://github.com/purescript/purescript-in-purescript) abandoned rewrite of purescript compiler in purescript making it self-hosting
* [purty](https://github.com/joneshf/purty) - purescript formatter written in haskell. Abandoned since it didn't keep up with the later purescript features. Served as good inspiration for pretty printing purescript code. The official purescript compiler in haskell has only the parser part.
