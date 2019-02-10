# isObject


```js
// Populate the class2type map
$.each("Boolean Number String Function Array Date RegExp Object Error".split(" "), function(i, name) {
    class2type[ "[object " + name + "]" ] = name.toLowerCase()
})
function type(obj) {
    return obj == null ? String(obj) :
        class2type[toString.call(obj)] || "object"
}

function isObject(obj){ 
    return type(obj) == "object" 
}
```