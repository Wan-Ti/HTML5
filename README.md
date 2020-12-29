# HTML5

## 有话说

前端的核心：URL+HTTP+HTML；MDN查询HTML相关资料；

```
HTML5技术集合 

· 新标签、新属性；
· 新的通信技术：WebSockets、WebRTC等；
· 离线存储技术：LocalStorage、断网检测；
· 多媒体技术：视频、音频；
· 图像技术：Canvas、SVG、WebGl;
· Web增强技术：HistoryAPI、全屏；
· 设备相关技术：摄像头，触摸屏；
· 新的样式技术：CSS3新的Flex、Grid布局方式
``` 

## 章节标签
```
<h5>标题标签h1~h6 </h5>  
<section>章节标签section</section> 
<article>文章标签article</article> 
<p>段落标签p</p>  
<header>头部标签header</header>  
<footer>脚部标签footer</footer>  
<main>主要内容main</main>
<aside>旁支内容aside</aside>
<div>划分部分div</div>
```
所有标签都有的属性称为全局属性。
```
class
contenteditable:将styel设置为contenteditable;display:block;可以实时更改样式
hidden
id:不到万不得已不要用id为标签命名；即便id重复也不会报错。
style
tabindex：特殊值：-1，0，1；
title:鼠标浮动显示省略内容
```

## 内容标签
```
ol+li
ul+li
dl+dt+dd
pre：用户保留多个空格以及回车
hr：水平分割线
br：换行
a：超链接
em：
strong：2
code：code标签包含的内容是等宽的。                                                                                                                                                 *                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       
quote
blockquote
```

1. 控制文本自动换行，超出内容省略
```
white-space:nowrap;
text-overflow:ellipsis;
overflow:hidden;
```

2.如何查看或取消默认样式</br>
  查看：Chrome开发工具-Elements-Styles-user agent stylesheet</br>
  取消：进入大厂首页->Chrome开发者工具，找到类似代码->复制到自己项目中->命名为reset.css
  ```
 * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
*::before,
*::after {
  box-sizing: border-box;
}
a {
  color: inherit;
  text-decoration: none;
}
input,
button {
  font-family: inherit;
}
ol,
ul {
  list-style: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
  ```
  
# 部分标签常用属性

## a标签的属性取值
   作用：{
       跳转外部页面；
       跳转内部锚点；
       跳转到邮箱或电话等；
        }

### href取值

```
· 网址：
  <a href="https://google.com">谷歌</a>
  <a href="http://google.com">谷歌</a>
  <a href="//google.com">谷歌</a>
 
 · 路径：
   <a href="/a/b/c"></a>
   <a href="a/b/c"></a>
   <a href="index.html"></a>
   
  . 伪协议
     <a href="javacrtipt:alert(a)">执行JavaScript</a>
     <a href="mailto:邮箱">点击发送邮件</a>
     <a href="tel:123456">点击拨打电话</a>
     
   · id
     <a href="#xxx">跳转ID为XXX的部分</a>
  
```

### target取值

```
内置名字：
<a target="_blank">在一个新的页面打开链接</a>；
<a target="_top">在最顶层页面打开链接</a>；
<a target="_parent">在父页面打开链接</a>；
<a target="_self">在当前页面打开</a>；
```

## table标签常用属性

### table关联标签
```
<table>
  <thead>
    <tr>
      <th></th>
       <th>A</th>
       <th>B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
       <th>数学</th>
       <td>1</td>
       <td>2</td>
    </tr>
    <tr>
       <th>语文</th>
       <td>1</td>
       <td>2</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
       <th>总分</th>
       <td>3</td>
       <td>3</td>
    </tr>
  </tfoot>
</table>
```
<table>
  <thead>
    <tr>
      <th></th>
       <th>A</th>
       <th>B</th>
    </tr>
  </thead>
  <tbody>
    <tr>
       <th>数学</th>
       <td>1</td>
       <td>2</td>
    </tr>
    <tr>
       <th>语文</th>
       <td>1</td>
       <td>2</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
       <th>总分</th>
       <td>2</td>
       <td>4</td>
    </tr>
  </tfoot>
</table>

### table相关的样式属性

```
table{
    table-layout:auto/fixed;
    border-collapse:collapse(相邻单元格具有共享边框，常用)/parate(相邻单元格具有不同的边界)
    border-spacing:控制border和border之间的距离
}

```

## img标签常用属性

```
作用：发出get请求，展示图片；
属性：alt/height/width/src;(为了防止图片变形，一般只设置宽度或者只设置高度)
时间：onload(图片加载成功)/onerror(图片加载失败);
响应式：max-width:100%;
```

## 可替换元素
```
可替换元素的外观渲染是独立于CSS的。CSS 可以影响可替换元素的位置，但不会影响到可替换元素自身的内容。
典型的可替换元素有：
<iframe>
<video>
<embed>
<img>

有些元素仅在特定情况下被作为可替换元素处理，例如：

<option>
<audio>
<canvas>
<object>
<applet>

```

## from标签常用属性
```
作用：发送get或post请求，然后刷新页面；//涉及到的知识点：get和post的区别
属性：action/autocomplete(是否自动填充)/method/target(类似于a标签的target属性，在哪个页面刷新);
时间：onsubmit;//input与button的submit的区别：input中间不能再有其他内容，但是button可以，可以添加其他标签
```

## input标签常用属性

```
作用：让用户输入内容
属性：
    类型type:button/checkbox/email/file/hidden/number/password/radio/search/submit/tel/text;
    其他：name/autofocus/checked/disabled/maxlength/pattern/value/placeholder;
事件：onchange/onfocus/onblur;
验证器：HTML5新增功能；
```

## 其他输入标签
```
标签：
   select+option；textarea;label
注意事项：
   一般不监听input的click时间；
   form里面的input要有name；
   form里面放一个type=submit才能出发submit事件
```
