# json

https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/JSON



## json 数据格式

```
{
	"key1": "string value",
	"key2": 0,
	"key3": [0,"string",{},[]],
	"key4": {},
	"key5": true/false
}
```

json 是跨语言的数据格式，key 必须加半角双引号。



在 js 代码中，json 和其他数据一样，通过访问变量或者函数参数调用。

```
let obj = {"a": 1};
let key = "c";
obj.b = 2;
obj[key] = 3;


console.log(obj.a);		//1
console.log(obj.b);		//2
console.log(obj.c);		//3
```



## 浏览器 JSON 对象

JSON.parse()

JSON.stringify()