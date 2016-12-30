# Array-String
Javascript数组去重:http://www.tuicool.com/articles/uQ7ZjiY  
https://segmentfault.com/a/1190000000513057    
数组赋值：  
必须要相同的数组名才能够赋值，例如   
var data=[];  
data = data.push(obj);   
这样可以赋值  

const data = ['name','damage','haha','wuyu'];
data.map((key,index)=>{
  return key+index;
});

## delete它既删除其值,也删除其位置   
const data = ['name','damage','haha','wuyu'];  
const data = [0: 'name',1:'damage',2: 'haha',3: 'wuyu'];   
delete data[0];    
console.log(data);   // 返回值  [1:'damage',2: 'haha',3: 'wuyu'];   
console.log(data.length);  // 返回值4  

for (key in data) {
	console.log(key);  
	console.log(data[key]);  
}

## splice删除之后会重新排序
const data = ['name','damage','haha','wuyu'];  
const data = [0: 'name',1:'damage',2: 'haha',3: 'wuyu'];  
data.splice(0, 1);  
console.log(data);  
console.log(data.length);  // 返回值3  

小结  
[delete 操作符用来删除一个对象的属性。](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/delete)  
语法  
delete expression  
 expression 应该是一个对象的属性引用，例如：  
delete object.property   
delete object['property']  
eg:  
const data = {name:'zhangsan',age:23};  
delete data.name;  
console.log(data);  
如果 expression 的计算结果不是一个对象的属性引用，那么，delete不会起任何作用。  

splice常用于操作数组里的值  

# 数组concat() and push() unshift()
concat()方法操作后返回一个新的数组，原来的数组没有变化；push()操作之后相当于修改了原来的数组；

	<script>
		var parents=[{id:"1",name:"Tove"},{id:"2",name:"jani"}];
		var brothers=["stale","Kai","jim"];
		var children=[{id:"3",name:"clone"}];
		var xx=["tom"];
		var family=parents.concat(brothers,children,xx);
		console.log(family);
		var obj={id:'4',name:"dada"};
		family.push(obj);
		console.log(family);
	</script>
