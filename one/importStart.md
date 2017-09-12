### 初始结构
***
#### 作用域包裹 
undersource也是通过一个闭包来完成和外界防止冲突的立即执行函数
> js 里函数调用有 4 种模式:方法调用、正常函数调用、构造器函数调用、apply/call 调用。
前面两种应该都很熟悉了。
这里用的是call立即调用。
没有采用apply多半是因为操作的步骤比call多所以这里就选用了call了吧
这是从其他地方搜的答案
http://blog.csdn.net/zhengyinhui100/article/details/7837127
```
function(){}.call(this);
```

函数里 首先将this赋值给局部变量的 root
这里root的值在客户端里面是`window`,服务端一般是指node模块中的`exports`
> ```
  var root = this;
  ```
  
把刚挂载到全局的root身上的root._ 赋值给previousUnderscore
>```
var previousUnderscore = root._ ;
```











