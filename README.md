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
 


