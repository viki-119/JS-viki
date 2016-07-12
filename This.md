全局的this
console.log(this.document === document);  
console.log(this===window);  
this.a = 312; 
console.log(window.a);
一般函数的this
```js
  function f1() {
    return this;
  };
  console.log(f1() === window);
  function f2() {
    "use strict"; //see strict mode
    return this;
  }
  console.log(f2() === undefined);
```
作为对象方法的函数的this
```js
var o={
  prop:37,
  f:function() {
    return this.prop;
  }
}
console.log(o.f());
```

```js
var o={prop:37};
function independent() {
  return this.prop;
}
o.f=independent;
console.log(o.f());
```
