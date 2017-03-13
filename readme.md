# requirejs 简单用法

### define 在不依赖其他模块的时候 可以使用
  define({
      a:'a',
      age:12
    })
    或者
    define(function(){
     return {
       a:"a",
       age:12
     }

### 当存在依赖的时候
`define(['a'],function(a){
     return {
       name:a.name
     }
  })`


当我们引入的时候
     main.js
    ` require(['./a','./b'],function(a,b){
    然后在我们的require里面可以使用对应的a,b里面的方法

       })`

### 在main.js里面我们引入顺序
'script src='./require.js'
script src='./main.js''
