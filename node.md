# Bootstrap 响应式原理

## 响应式具有的特点

- 1.网页的宽度自动调整
- 2.尽量少用绝对宽度
- 3.字体要使用 rem、em 作为单位(其中,主要使用 rem,rem 表示根节点字体的大小,在 HTML 中的根节点(:root)是 html)
- 4.布局要使用浮动或弹性布局(其中,3 版本 Bootstrap 布局使用浮动,也就是流式布局;4 版本 Bootstrap 布局使用弹性布局)
  Bootstrap 实现响应式的效果主要依靠媒体查询

## 媒体查询

- 定义：根据一个或多个基于设备类型、具体特点和环境来应用样式
- css 中的@规则
  - @charset 定义编码
  - @import 引入 css 文件(css 模块化)
  - @font-face 自定义字体
  - @keyframes animation 关键字
  - @media 媒体查询

## 媒体查询的使用

* 在 css 文件中使用@media 媒体类型、媒体功能
```
@media screen and (max-width: 300px) {
    body {
        background-color: lightblue;
    }
}
```
* 在 @import 中使用@media
```
@import url('css/index.js')(min-width: 200px);
```
* 在link标签中使用@media
```
<link rel="stylesheet" href="css/bootstrap.css" media="all">
```

## 媒体查询的内容
* w3c官方网站：https://drafts.csswg.org/mediaqueries

### 媒体类型
- all：表示所有设备
- print：表示打印机设备
- screen：表示彩色的电脑屏幕
- speech：表示听觉设备(针对有视力障碍的人士,可以把页面的内容以语音的方式呈现的设备)
**注意：tty、tv、projection、handheld、braille、embossed、aural等几种类型在媒体查询4中已经废弃**
```
<style>
div{
    width: 200px;
    height: 200px;
    background-color: aqua;
}
@media screen{
    div{
        background-color: #f40;
    }
}
</style>

<div>媒体类型</div>
```
### 常用媒体特性
* width 宽度
  - min-width 最小宽度、宽度只能比这个大
  - max-width 最大宽度、宽度只能比这个小
* height 高度
  - min-height 最小高度、高度只能比这个大
  - max-height 最大高度、高度只能比这个小
* orientation 方向
  - landscape 横屏(宽度大于高度)
  - portrait 竖屏(高度大于宽度)
* aspect-ratio 宽度比
  - -webkit-device-pixel-ratio 像素比(webkit内核的私有属性)
```
<div>媒体类型</div>

<style>
    div{
        width: 200px;
        height: 200px;
        background-color: aqua;
    }
    @media (max-width: 500px) {
        div{
            background-color: #f40;
        }
    }
    <!-- 宽高比例为4:3的是否满足,例如800*600 -->
    @media (aspect-ratio: 4/3){
        div{
            border: 10px solid #000;
        }
    }
</style>
```

### 逻辑运算符(用来做条件判断)
* and 合并多个媒体类型(并且的意思)
* , 匹配某个媒体查询(或者的意思)
* not 对媒体查询结果取反,not运算符必须要两个条件以上才能使用
* only 仅在媒体查询匹配成功后应用样式(防范老旧浏览器,旧的浏览器可能不支持媒体查询,如果设置了媒体查询会导致没有满足媒体查询同样使用样式,为了防止此种情况可以加上only,仅在媒体查询匹配成功后应用样式)
```
<div>媒体类型</div>

<style>
    div{
        width: 200px;
        height: 200px;
        background-color: aqua;
    }
    @media all and (min-width: 500px) and (orientation: landscape) {
        div{
            background-color: #f40;
        }
    }
    @media (max-width: 800px), (orientation: landscape){
        div{
            background-color: pink;
        }
    }
    @media not all and (max-widht: 800px){
        div{
            background-color: springgreen;
        }
    }
    @media only screen and (min-width: 1000px){
        div{
           background-color: silver;
        }
    }
</style>
```

## 响应式的应用
```
<div>1</div>
<div>2</div>
<div>3</div>
<div>4</div>
<div>5</div>

<style>
    body {
        margin: 0;
    }
    div {
        width: 100px;
        height: 100px;
        background-color: aqua;
        float: left;
        border: 1px solid #000;
        box-sizing: border-box;
        text-align: center;
        line-height: 100px;
    }
    body::after {
        content: "";
        display: block;
        clear: both;
    }
    @media screen and (max-width: 500px) {
        div {
          width: 100%;
        }
    }
    @media screen and (min-width: 500px) {
        div {
          width: 50%;
        }
    }
    @media screen and (min-width: 700px) {
        div {
          width: 33.33%;
        }
    }
    @media screen and (min-width: 900px) {
        div {
          width: 25%;
        }
    }
    @media screen and (min-width: 1100px) {
        div {
          width: 20%;
        }
    }
</style>
```