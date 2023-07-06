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
     console.log(a) //10 
     a = 20
     console.log(a) //20
   }
   fn()
   console.log(a) //20
   
   //-----------------------
   a = 10
   // a 为形参
   function fn2(a){
     console.log(a) //undefined
     console.log(a) // 20
   }
   fn2()
   console.log(a) // 10
   
   //-----------------------
   a = 10
   // 函数内定义a
   function fn3(){
      console.log(a) //undefined
      var a=20
      console.log(a) //20
   }
   fn3()
   console.log(a) //10
   ```
 - 访问一个对象的原型对象
   ```
   obj.__proto__ //不建议
   Object.getPrototypeOf(obj) //建议
   类.prototype //修改原型
   ```
 - 原型对象由两部分组成
  - 对象添加到原型的属性和方法
  - constructor 构造函数，一般是示例对象的类。即一个示例对象的原型对象，其包含的构造函数是该示例对象对应的类
 - 多态最根本的作用就是通过把过程化的条件语句转化为对象的多态性，从而消除这些条件分支语句
   ```
   function makeSound (animal) {
     if (animal.sound instanceof Function) { // 判断是否有animal.sound且该属性为函数
       animal.sound()
     }
   }
   class Cat {
     sound () {
       console.log('喵喵喵～')
     }
   }
   class Dog {
     sound () {
       console.log('汪汪汪！')
     }
   }
   class Pig {
     sound () {
       console.log('啂妮妮')
     }
   }
   makeSound(new Cat()) // '喵喵喵～'
   makeSound(new Dog()) // '汪汪汪！'
   makeSound(new Pig()) // '啂妮妮'
   ```



