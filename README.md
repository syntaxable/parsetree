# ParseTree

> Because syntax trees are difficult to use.

Syntaxable's ParseTree provides a wrapper layer that makes it easy to interact with parsed code using selector patterns that are familiar and comfortable. (Think jQuery for your parsed code tree)

Available for the following languages:

Language|Package|Available Selectors
:---|:---|:---
JavaScript|[parsetree-js](https://github.com/syntaxable/parsetree-js)|[glossary](https://github.com/syntaxable/parsetree-js/blob/master/GLOSSARY.md)
HTML||
CSS||
...||

## Specification and Standards

View the Specification for the [ParseTree Interaction Layer](https://github.com/syntaxable/parsetree/blob/master/specifications/InteractionLayer.md)

Code is so much more than a String. It has form and structure that makes it possible for a machine to understand and execute precise instructions. Sadly, many of our development tools operate on source files as simple strings and we lose the ability to understand our own code during processing steps. Even when we do have access to parsed trees we avoid using them because they are deeply nested and difficult to traverse.

Our goal is to create a standard way to interact with parsed code trees in a reliable and intuitive manner that applies across all languages. Manipulating and transforming source code should be easy and approachable for developers of all levels and backgrounds.

## Examples

JavaScript
```js
let code = fs.readFileSync('./src/program.js', 'utf8');
let $ = new ParseTree(code);
let allFns = $.find('FunctionDeclaration');
allFns.each((fn) => {
    console.log(fn.name);
});
```
