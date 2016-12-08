```javascript
// Declare and initiate at the beginning
var firstName = "",
    lastName = "",
    price = 0,
    discount = 0,
    fullPrice = 0,
    myArray = [],
    myObject = {};
```    

```javascript
var MyNamespace = MyNamespace || {};

MyNamespace.MyModule = function()
{
    // Your module is now in a namespace!
}
```        

```javascript
// An anonymous function that can never be referenced by name...
(function(){
    var x = 123;
    console.log(x);
})(); // Call the anonymous function once, then throw it away!

console.log(x);
```

```javascript
//Don't use !eval()
```

```javascript
//Difference == and ===
3 == "3" //true
3 == 3 //true
3 === "3" //false
3 === 3 //true
```

```javascript
//Don't use
for(var i = 0; i < someArray.length; i++) {
   var container = document.getElementById('container');
   container.innerHtml += 'my number: ' + i;
   console.log(i);
}
//Use
var container = document.getElementById('container');
for(var i = 0, len = someArray.length; i < len;  i++) {
   container.innerHtml += 'my number: ' + i;
   console.log(i);
}
```

```javascript
// {} Better new Object();
// [] Better new Array(); 
```

```javascript
//Self-Executing Functions
(function doSomething() {
   return {
      name: 'jeff',
      lastName: 'way'
   };
})();
```

```javascript
//Before
if(v){
   var x = v;
} else {
   var x =10;
}
//After
var x = v || 10;
```

```javascript
//Before
var direction;
if(x > 100){
   direction = 1;
} else {
   direction = -1;
}
//After
var direction = (x > 100) ? 1 : -1;
```

```javascript
// bad
function foo(bar,
             baz,
             quux) {
  // body
}

// good
function foo(
  bar,
  baz,
  quux,
) {
  // body
}
```

```javascript
// bad
console.log(foo,
  bar,
  baz);

// good
console.log(
  foo,
  bar,
  baz,
);
```

```javascript
// After
var Jedi = function(){};
Jedi.prototype.jump = function () {
  this.jumping = true;
  return true;
};

Jedi.prototype.setHeight = function (height) {
  this.height = height;
};

const luke = new Jedi();
luke.jump(); // => true
luke.setHeight(20); // => undefined

// After
class Jedi {
  jump() {
    this.jumping = true;
    return this;
  }
  setHeight(height) {
    this.height = height;
    return this;
  }
}

const luke = new Jedi();

luke.jump()
  .setHeight(20);
```

```javascript
// bad
if (isValid === true) {}
// good
if (isValid) {}

// bad
if (name) {}
// good
if (name !== '') {}

// bad
if (collection.length) {}
// good
if (collection.length > 0) {}
```

```javascript
// bad
const foo = a ? a : b;
const bar = c ? true : false;
const baz = c ? false : true;

// good
const foo = a || b;
const bar = !!c;
const baz = !c;
```