## tinysql笔记



### go语言复习

+ 一个模块导出的表变量名，第一个字母大写，否则不能导出被其他模块引用。

+ defer会将要进行的操作进行压栈，当函数返回之后进行弹栈。（不知道有没有是队列形式的defer）

+ 进行切片的复制后，实际上变量对变量进行了引用，切片实际上不会占用额外的内存。

+ 
  ```
  var m map[string]Vertex
  m = make(map[string]Vertex)//声明时是nil类型，只有make()才初始化可使用
  或
  m := make(map[string]Vertex)
  ```

+ 闭包：实际上是匿名函数的升级版。能够实现代码和数据的分离。实际上感觉是一种作用域的使用方法。

+ 在定义某个结构体中的方法函数时，如果是函数声明式，那么必须按照规定的要求来；如果是`.fun()`方式，那么指针类型或者一般类型都可以直接引用

```go
var v Vertex
ScaleFunc(v, 5)  // Compile error!
ScaleFunc(&v, 5) // OK
or
var v Vertex
v.Scale(5)  // OK
p := &v
p.Scale(10) // OK
```

