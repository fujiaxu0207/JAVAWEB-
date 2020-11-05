在javase中的软件结构是 C/S结构  client server  
在javaweb中的软件结构式 B/S结构  browse server
### 网页由三部分组成
> 分别是：内容（结构）、表现、行为  
> 内容：一般是指我们可以看见的数据，一班用html实现  
> 表现：一般指的是在网页上展现的形式。比如颜色。。。一般使用css实现  
> 行为：指的是页面上的元素与输入设备交互的响应。一般使用javascript。  
 
### html的结构
``` html
<!DOCTYPE html><!-- 约束，声明-->
<html lang="zh_CN"><!--html标签，表示html的开始-->
<head> <!--表示头部信息，一一般包含三部分内容：title标签，css样式，js代码-->
    <meta charset="UTF-8">
    <title>标题</title>
</head>
<body><!--整个html的主体，表示当前页面的主体内容-->
    hello
</body>
</html>  
```
### html的标签 
>* 标签的格式 <标签名>封装的数据</标签名>  
>* 标签大小写不敏感  
>* 标签拥有自己的属性  
>   -   基本属性：bgcolor = “red” 改变背景颜色
>   -   事件属性：onclick = "alert('你好！')"   
>* 标签分为单标签和双标签  
>   -   <   p> <    /p>  
>   -   < br />

### 标签的语法
> 标签不能嵌套
> 双标签要有结束符
> 单标签要有 /
> 属性要有引号。。。。。

### 常用标签
>文档在[这里](w3cschool.CHM)
### 特殊字符
>   &lt ;   -->  <  
> &rt;  ->> <
### 标题标签
> h1到h6  
> < h1 align = "center">这是标题1，并且居中 </>
> align 属性是对齐属性 left 、right、 center
### **超链接（重点）**
>< a href = "http://www.baidu.com" target = 'self'>百度< / a >
### 列表标签
>* 无序列表、有序列表、定义列表
>* 无序列表
>      -  < ul> < li>< /li></ ul> unorder lsit
> * 有序列表
>      -    < ol></ ol> 
### img标签

### **表格tab（重点）**


    