# 栅格系统-1

## use Grid

```
<div class="container-fluid">
  <div class="row"></div>
</div>
<div class="container">
  <div class="row"></div>
</div>
```

两个 div 的宽度不一样,设置 class="container-fluid"的元素取得的宽度是父级,通常是 body,body 是取的是 html 的宽度,而 html 取的是用户打开网页的设备;而 class="container"并不是 100%宽度,而是一个具体数值,这个数值根据用户的屏幕尺寸进行改变

## Grid options
- Bootstrap4 根据设备屏幕尺寸分为五种情况
  > 特小(< 576px), 最大容器宽度(None(auto)), 类名前缀(.col-)
  > 小(>= 576px), 最大容器宽度(540px), 类名前缀(.col-sm-)
  > 中(>= 768px), 最大容器宽度(720px), 类名前缀(.col-md-)
  > 大(>= 992px), 最大容器宽度(960px), 类名前缀(.col-lg-)
  > 特大(>= 1200px), 最大容器宽度(1140px), 类名前缀(.col-xl-)
  > 列数(12), 间距(30px(每列左右 15px)), 支持嵌套, 支持列排序
**相对于 Bootstrap3 最大容器宽度变小,增加特大的情况**
## 例子
```
<div class="container-fluid">
    <div class="row">
      <div class="col-xl-1">第1列</div>
      <div class="col-xl-1">第2列</div>
      <div class="col-xl-1">第3列</div>
      <div class="col-xl-1">第4列</div>
      <div class="col-xl-1">第5列</div>
      <div class="col-xl-1">第6列</div>
      <div class="col-xl-1">第7列</div>
      <div class="col-xl-1">第8列</div>
      <div class="col-xl-1">第9列</div>
      <div class="col-xl-1">第10列</div>
      <div class="col-xl-1">第11列</div>
      <div class="col-xl-1">第12列</div>
    </div>
    <div class="row">
      <div class="col-xl-6">占6列</div>
      <div class="col-xl-6">占6列</div>
    </div>
    <div class="row">
      <div class="col-xl-6">占6列</div>
      <div class="col-xl-8">占8列</div>
    </div>
    <div class="row">
      <div class="col-xl-15">占15列</div>
    </div>
</div>    
.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
```
**从上面的例子可以看出,栅格系统每一行最多只能分为12列,如果多列之和超过12,会导致不能被该行容纳部分换行,如果单列超过12,Bootstrap没有对应的样式导致显示原始样式**

## Grid options详解
## 例子
```
<div class="container">
    <div class="row">
        <div class="col-xl-3">xl为超大屏,屏幕宽度 >= 1200px,容器的宽度固定为1140px,一行可以设置12列;当屏幕尺寸 < 1200px的时候,一行只能设置1列</div>
        <div class="col-xl-3"></div>
        <div class="col-xl-3"></div>
        <div class="col-xl-3"></div>
    </div>
    <div class="row mt-5">
        <div class="col-lg-4">lg为大屏,屏幕宽度 >= 992px,容器的宽度固定为960px,一行可以设置12列;当屏幕尺寸 < 992px的时候,一行只能设置1列</div>
        <div class="col-lg-4"></div>
        <div class="col-lg-4"></div>
    </div>
    <div class="row mt-5">
        <div class="col-md-6">md为中等屏,屏幕宽度 >= 768px,容器的宽度固定为720px,一行可以设置12列;当屏幕尺寸 < 768px的时候,一行只能设置1列</div>
        <div class="col-md-6"></div>
    </div>
    <div class="row mt-5">
        <div class="col-sm-3">sm为小屏,屏幕宽度 >= 576px,容器的宽度固定为540px,一行可以设置12列;当屏幕尺寸 < 576px的时候,一行只能设置1列</div>
        <div class="col-sm-3"></div>
        <div class="col-sm-3"></div>
        <div class="col-sm-3"></div>
    </div>
      <div class="row mt-5">
        <div class="col-4">col为超小屏,屏幕宽度 < 576px,一行永远可以设置12列</div>
        <div class="col-4"></div>
        <div class="col-4"></div>
    </div>
    <!-- 设置等宽,平衡宽度,通过.col的class设置 -->
    <div class="row">
        <div class="col">等宽列</div>
        <div class="col">等宽列</div>
        <div class="col">等宽列</div>
        <div class="col">等宽列</div>
    </div>
    <!-- 设置多行等宽列,在希望断开的地方添加一个.w-100的class,能够让后面的列换行-->
    <div class="row">
        <div class="col">等宽列1</div>
        <div class="col">等宽列2</div>
        <!-- 因为前面统一对div设置样式了所以需要去掉 -->
        <div class="w-100" style="height: auto; border: none;"></div>
        <div class="col">等宽列3</div>
        <div class="col">等宽列4</div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
```
**误区：当屏幕满足小屏(sm)、中等屏(md)、大屏(lg)、超大屏(xl)时,容器的最大宽度不是540px、720px和960px,而是1140px;因为媒体查询跟CSS一样后面的样式覆盖前面的样式,而这里媒体查询书写是按照屏幕尺寸大写书写,所以屏幕尺寸最大的在最后,而匹配的条件都是>=没有上限,除了超小屏**