 - prompt - 返回值是字符串，或 null，想要数字时，利用一元运算 "+" 转为number类型
 - in - 查询对象中是否含有某个属性名 `name in obj`
 - for in - 遍历对象中每一个属性
   ```
   for(propName in obj){
       console.log(proName, obj[propName])
   }
   ```
  - 箭头函数只有一个 `return` 语句时，可省略大括号和return;只有一个参数时，可以省略小括号
  - let声明的变量不会存储在window对象
    ```
    let c = 30
    window.c = 40
    console.log (c===window.c) //false
    ```
 - 局部作用域中，没有使用var或let声明变量，则变量会自动成为window对象的属性 也就是全局变量
   ```
   function fn(){
     b=10
   }
   console.log{b}
   console.log{window.b}
   ```
 - 全局定义变量 a，函数形参不是a，函数内也没有定义a，则函数内对a就是对全局变量a。
   ```
   var a = 10
   function fn(){
     a = 20
     console.log(a) //20
   }
   fn()
   console.log(a) //20

   // a 为形参
   function fn2(a){
     console.log(a) //undefined
     a=20
     console.log(a) // 20
   }
   console.log(a) // 10
   ```
 


