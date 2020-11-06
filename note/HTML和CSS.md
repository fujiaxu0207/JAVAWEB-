在javase中的软件结构是 C/S结构  client server  
在javaweb中的软件结构式 B/S结构  browse server
### 网页由三部分组成
> 分别是：内容（结构）、表现、行为  
> 内容：一般是指我们可以看见的数据，一班用html实现  
> 表现：一般指的是在网页上展现的形式。比如颜色。。。一般使用css实现  
> 行为：指的是页面上的元素与输入设备交互的响应。一般使用javascript。  
 
## html的结构
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
```html
<!DOCTYPE html>
<html lang="zh_CN">
<head>
    <meta charset="UTF-8">
    <title>表格标签</title>
</head>
<body>
<!--
    需求1：做一个带代表头的，三行，三列的表格，并显示边框
    需求2：修改表格的宽度。高度，表格的对对齐方式，单元格间距
    cellspacing 设置单元格间距

-->
    <table border = "1" width = "300" height = '300' align="center" cellspacing="0">
        <tr>
            <th >1.1</th>
            <th>1.2</th> <!--表头标签-->
            <th>1.3</th>
        </tr>
        <tr>
            <td>2.1</td>
            <td>2.2</td>
            <td>2.3</td>
        </tr>
        <tr>
            <td>3.1</td>
            <td>3.2</td>
            <td>3.3</td>
        </tr>
    </table>
</body>
</html>
```
### 表格的跨行、列
```html
<!DOCTYPE html>
<html lang="zh_CN">
<head>
    <meta charset="UTF-8">
    <title>表格的跨行跨列</title>
</head>
<body>
    <!--
        需求1：
            新建一个五行，五列的表格，
            第一行，第一列的单元格要跨两列
            第二行第一列的单元格要跨两行
            第四行第四列的单元格跨两列两行
         colpan 属性设置跨列
         rowspan 属性设置跨行
    -->
    <table width="500" height = '500' cellspacing="0" border="1">
        <tr>
            <td colspan="2">1.1</td>
            <td>1.3</td>
            <td>1.4</td>
            <td>1.5</td>
        </tr>
        <tr>
            <td rowspan="2">2.1</td>
            <td>2.2</td>
            <td>2.3</td>
            <td>2.4</td>
            <td>2.5</td>
        </tr>
        <tr>
            <td>3.2</td>
            <td>3.3</td>
            <td>3.4</td>
            <td>3.5</td>
        </tr>
        <tr>
            <td>4.1</td>
            <td>4.2</td>
            <td>4.3</td>
            <td colspan="2" rowspan="2">4.4</td>

        </tr>
        <tr>
            <td>5.1</td>
            <td>5.2</td>
            <td>5.3</td>
           
        </tr>

    </table>
</body>
</html>
```
### iframe(内嵌窗口)
```html
<!DOCTYPE html>
<html lang="zh_CN">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    我是一个单独的完整的页面<br/><br/>
    <!--开辟一个小区域，显示一个单独页面-->
    <!--
        iframe与a标签的配合使用
            1.在iframe标签中使用name属性定义一个名称
            2 在a标签中target属性设置iframe的name值
    -->
    <iframe src="表格的跨行、列.html" width="700" height="600" name="i">
        <br/>
        <br/>

    </iframe>
    <ul>
        <li><a href="Hello.html" target="i">Hello</a></li>
    </ul>
</body>
</html>
```

### **表单标签重点**
```html
<!DOCTYPE html>
<html lang="zh_CN">
<head>
    <meta charset="UTF-8">
    <title>表单的显示</title>
</head>
<body>
    <!--表单用来收集用户信息的所有元素集合，然后把这些信息发送个服务器-->
    <!--x
        需求：
           1.创建一个个人信息注册的表单界面。包含用户名，密码，确认密码。心别（单选）
                兴趣爱好（多选），国籍（下拉列表）
                影藏域，自我评价（多行文本域）。重置，提交。

        -->
    <!--form标签就是表单
        input  type = text 是文本输入框  value是默认值
               type = password 是密码输入框 value是默认值
               type = radio 单选框  name可以分组，防止多选 checked="checked"表示默认选重
               type="checkbox" 复选框
               type = "reset" 是重置
               type="submit" 提交按钮
               type="button" 按钮
               type="file" 文件上传域
               type = hidde 隐藏域  当我们要发送某些信息，但是不需要用户参与，就可以使用它（提交的时候可以发送个服务器）
        <select> 下拉列表框 option是选项  selected="selected"默认选中

        textarea 表示多行文本输入框  （默认值在起始标签和结束标签之间）
               rows 属性表示可以显示几行的高度
               cols 属性表示显示几行的狂赌

            -->

    <form>
        <table><!--表单的格式化-->
            <tr>
                <td>用户名称：</td>
                <td><input type="text" value="默认值"/><br/></td>
            </tr>
        </table>
        用户密码：<input type="password" value="abc" maxlength="11"/><br>
        确认密码：<input type="password" value="abc"/><br>
        性别：<input type="radio" name="sex" checked="checked"/>男<input type="radio" name="sex"/>女<br>
        兴趣爱好：<input type="checkbox"/>java<input type="checkbox"/>c++<br>
        国籍：<select>
                <option>请选择你的国籍</option>
                <option selected="selected">中国</option>
                <option>每个</option>
            </select><br>
        自我评价:<textarea rows="10" cols="20">我才是默认值</textarea><br>
        <input type="reset" value="重值"><br>
        <input type="submit"><br>
        <input type="button"><br>
        <input type="file">
        <input type = hidden>
    </form>
</body>
</html>
```
### 表单的格式化
> 在表单里面使用table即课
### 表单提交个服务器
```html
  form标签的表单标签
                action属性 是设置提交的地址
                method属性设置提交的方式GET（默认值）或者POST
            表达提交的时候没有提交上去的原因：
                1.表单项没有name属性值
                2.单选、复选（下拉列表中的option标签）都需要添加value属性，以便发送给服务器
                3.表单项不在form之中。
            GET请求的特点是：
                1.浏览器地址栏中的地址是：action属性[+？+请求的参数]
                    请求参数的格式是：name = value & name = value
                2.不安全，所有信息都可见（地址栏中）
                3.他有数据的长度限制
            POST请求的特点是：
                1.浏览器地址栏中只有action属性值
                2.相对于GET请求安全
                3.理论上没有数据长度的限制
```
### 其他标签
>div span p
```html
<!DOCTYPE html>
<html lang="zh_CN">
<head>
    <meta charset="UTF-8">
    <title>其他标签</title>
</head>
<body>
    <!--
        需求：div、span、p标签的演示
    -->
    <!--
    div默认独占一行
    span他的长度是封装数据的长度
    p段落标签  默认会在段落的上方或者下方各空出一行来（如果有则不在空）
    -->
</body>
</html>
```
## CSS技术 记得看文档
>css是一种标记行语言  

### CSS语法规则
P{
    font-size:800px;
}
p是选择器，font-size是属性，80px是值
>选择器决定受CSS样式影响的HTML元素(标签)  
>属性（property）要改的样式名  
>多个属性声明是要';'分开
>**CSS的注释 /* */**
### CSS的用法
>通过style使用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <!--
        需求：分别定义两个div、span标签，分别修改每个div标签的格式：边框为1个像素，实线：红色

    -->
    <div style="border: 1px solid;border-color: #3b1010">
        div标签1
    </div>
    <div>

    </div>
    <span>

    </span>
</body>
</html>
```
>通过style使用在head标签中定义
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        div{
            border: 1px solid red;
        }
    </style>
</head> 
<body>
    <!--
        需求：分别定义两个div、span标签，分别修改每个div标签的格式：边框为1个像素，实线：红色

    -->
    <div >
        div标签1
    </div>
</body>
</html>
```
>把CSS样式写出一个单独的CSS文件，在通过Link标签引用就可以
>在1.css定义
```html
div{
    border: 1px solid red;
}
```
>在1-CSS.html中引用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <!--link标签用来引用css代码-->
    <<!--rel是关系，stylesheet是表示调用的css文件-->
    <link rel="stylesheet" type="text/css" href="1.css">
</head> 
<body>
    <!--
        需求：分别定义两个div、span标签，分别修改每个div标签的格式：边框为1个像素，实线：红色

    -->
    <div >
        div标签1
    </div>
</body>
</html>
```
### 标签名的选择器
标签名{
    属性：值
}
标签名可以选择哪些标签使用该样式
### id选择器
#id 属性值{
    属性:值
}
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        #id001{
            color: blue;
            font-size: 30px;
            border: 1px yellow solid ;
        }
        #id002{
            color: red;
            font-size: 20px;
            border: 5px blue dotted;
        }
    </style>
</head>
<body>
    <div id="id001">div1</div>
    <div id="id002">div2</div>
</body>
</html>
```
### class类型选择器
.class属性值{
    属性：值
}
```html
<!DOCTYPE html>
<html lang="zh_CN">
<head>
    <meta charset="UTF-8">
    <title>class属性</title>
    <style>
        .class01{
            color: blue;
            font-size: 30px;
            border: 1px yellow solid;
        }
        .class02{
            color: grey;
            font-size: 26px;
            border: 1px red solid
        ;
        }
    </style>
</head>
<body>
    <div class="class01">
        div标签
    </div>
    <div class="class02">
        div标签
    </div>

</body>
</html>
```
### 组合选择器
选择器1，选择器2，选择器n{

    属性：值
}
```html
<!DOCTYPE html>
<html lang="zn_CH">
<head>
    <meta charset="UTF-8">
    <title>组合选择器</title>
    <style type="text/css">
        .class01,#id01{
            color: blue;
            font-size: 20px;
            border: 1px yellow solid;
        }
    </style>
</head>
<body>
    <div class="class01">
        div
    </div>
    <span id="id01">
        span
    </span>
</body>
</html>
```
可以让多个选择器公用一个代码
### CSS常用样式
>