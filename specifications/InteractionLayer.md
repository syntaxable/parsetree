# Specification for the ParseTree Interaction Layer

> A standard wrapper for the raw parsed code tree

## Example Usage

```js
let $ = new ParseTree(code);
$('#foo').rename('bar');
console.log($.generate());
```

## Parsing
    A wrapped tree can only be created with `new ParseTree(code)`
    If `code` is a String it will be parsed
    If `code` is an Object that matches the accepted format it will be used as the raw tree
    If `code` is an Object that does not match the accepted format it will be adapted for use if possible

## Tree Controls
    getTree
    generate
    minify
    parse
    toString
    walk

## Node Selection
    add
    children
    closest
    concat
    eq (maybe this should be `at`?)
    find
    first
    last
    next
    parent
    siblings
    zero

## Node Modification
    after
    append
    attr
    before
    empty
    prepend
    remove
    removeAttr
    rename
    replace
    wrap

## Node Utils
    each
    has
    is
    not

## Array-like behavior
    length
    indexOf
    push
    pop
    shift
    unshift
    reverse
    slice
    splice
    forEach
    map
    filter
