# 栅格系统-2

## use Grid system
```
<div class="container">
    <!-- 设置一个列宽,剩下的自动平分,使用.col,通常.col是用来均分剩余宽度 -->
    <div class="row mt-5">
        <div class="col-sm-7">在小屏幕下占7列</div>
        <div class="col">自动平分剩余宽度</div>
        <div class="col">自动平分剩余宽度</div>
    </div>
    <!-- 设置根据内容调整列的宽度,使用.col-{breakpoint}-auto -->
    <div class="row mt-5">
        <div class="col-md-auto">在中等屏幕下由内容撑开宽度</div>
        <div class="col">自动平分剩余的宽度</div>
        <div class="col-lg-2">在大屏下占2列</div>
    </div>
    <!-- 设置所有尺寸下,都占同样的列数,使用.col-* -->
    <div class="row">
        <div class="col-8">所有尺寸都占8列</div>
        <div class="col-4">所有尺寸都占4列</div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
```

## Mixed arrangement or combination mode(混合排列或组合模式)
* 例子
```
<div class="container">
    <!-- 1.超大屏幕下,行显示6个div,一个div占2列 2.大屏幕下,一行显示4个div,一个div占2列 3.中等屏幕下,一行占3个div,一个div占4列 4.在小屏幕下,一行显示2个div,一个div占6列 5.超小屏幕下,一行显示1个div,一个div占12列 -->
    <div class="row">
        <div class="col-xl-2 col-lg-3 col-md-4 col-sm-6 col-12">超大屏6,大屏4个,中等屏3,小屏2个,超小屏1个</div>
        <div class="col-xl-2 col-lg-3 col-md-4 col-sm-6 col-12">超大屏6,大屏4个,中等屏3,小屏2个,超小屏1个</div>
        <div class="col-xl-2 col-lg-3 col-md-4 col-sm-6 col-12">超大屏6,大屏4个,中等屏3,小屏2个,超小屏1个</div>
        <div class="col-xl-2 col-lg-3 col-md-4 col-sm-6 col-12">超大屏6,大屏4个,中等屏3,小屏2个,超小屏1个</div>
        <div class="col-xl-2 col-lg-3 col-md-4 col-sm-6 col-12">超大屏6,大屏4个,中等屏3,小屏2个,超小屏1个</div>
        <div class="col-xl-2 col-lg-3 col-md-4 col-sm-6 col-12">超大屏6,大屏4个,中等屏3,小屏2个,超小屏1个</div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
```

## Grid system alignment
* 垂直对齐
  - 1.行的对齐方式
    - align-items-start 顶对齐
    - align-items-center 中间对齐
    - align-items-end 底对齐
  - 2.列的单独对齐方式
    - align-self-start 顶对齐
    - align-self-center 中间对齐
    - align-self-end 底对齐
* 水平对齐
  - 1.justify-content-start 左对齐
  - 2.justify-content-center 居中对齐
  - 3.justify-content-end 右对齐
  - 4.justify-content-around 分散居中对齐(每个元素两侧的间距是相等的)
  - 5.justify-content-between 左右两端对齐(元素之间的间距是自动平分的)
**Bootstrap3 使用流式布局所以没有对齐方式**
```
<div class="container">
    <!-- 垂直对齐 -->
    <!-- 默认值是align-items-start -->
    <div class="row v-align align-items-start">
        <div class="col">垂直对齐-顶部对齐-行的对齐方式</div>
        <div class="col">垂直对齐-顶部对齐-行的对齐方式</div>
        <div class="col">垂直对齐-顶部对齐-行的对齐方式</div>
    </div>
    <div class="row v-align align-items-center">
        <div class="col">垂直对齐-中间对齐-行的对齐方式</div>
        <div class="col">垂直对齐-中间对齐-行的对齐方式</div>
        <div class="col">垂直对齐-中间对齐-行的对齐方式</div>
    </div>
    <div class="row v-align align-items-end">
        <div class="col">垂直对齐-底部对齐-行的对齐方式</div>
        <div class="col">垂直对齐-底部对齐-行的对齐方式</div>
        <div class="col">垂直对齐-底部对齐-行的对齐方式</div>
    </div>
    <div class="row v-align ">
        <!-- 默认值是align-self-start -->
        <div class="col align-self-start">垂直对齐-底部对齐-行的对齐方式</div>
        <div class="col align-self-center">垂直对齐-底部对齐-行的对齐方式</div>
        <div class="col align-self-end">垂直对齐-底部对齐-行的对齐方式</div>
    </div>
    <!-- 水平对齐 -->
    <div class="row v-align justify-content-start">
        <div class="col-4">水平对齐-左对齐</div>
        <div class="col-4">水平对齐-左对齐</div>
    </div>
    <div class="row v-align justify-content-center">
        <div class="col-4">水平对齐-居中对齐</div>
        <div class="col-4">水平对齐-居中对齐</div>
    </div>
    <div class="row v-align justify-content-end">
        <div class="col-4">水平对齐-右中对齐</div>
        <div class="col-4">水平对齐-右中对齐</div>
    </div>
    <div class="row v-align justify-content-around">
        <div class="col-4">水平对齐-分散居中对齐</div>
        <div class="col-4">水平对齐-分散居中对齐</div>
    </div>
    <div class="row v-align justify-content-between">
        <div class="col-4">水平对齐-左右两端对齐</div>
        <div class="col-4">水平对齐-左右两端对齐</div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
.v-align{
    height: 100px;
    background: rgba(255, 0, 0, 0.1);
    margin: 10px -15px;
}
.v-align div{
    height: 40px;
    line-height: 40px;
    background: rgba(86, 61, 124, 0.15);
    border: 1px solid rgba(86, 61, 124, 0.2);
    color: #333;
}
```

## column sort
* 列排序 使用order-{breakpoint}-*
* Bootstrap3的版本使用.col-{breakpoint}-push-*和.col-{breakpoint}-pull-*来排序
```
<div class="container">
    <div class="row mt-5">
        <div class="col">第一列</div>
        <div class="col order-5">第二列</div>
        <div class="col order-6">第三列</div>
    </div>
    <div class="row mt-5">
        <div class="col">第一列</div>
        <!-- 只有当屏幕尺寸 >= 1200px的时候,才会进行排序 -->
        <div class="col order-xl-5">第二列</div>
        <div class="col order-xl-2">第三列</div>
    </div>
    <div class="row">
        <div class="col">第一列</div>
        <!-- order-first代表排在第一位,order-last代表排在最后一位 -->
        <div class="col order-first">第二列</div>
        <div class="col order-last">第三列</div>
        <div class="col">第四列</div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
.v-align {
    height: 100px;
    background: rgba(255, 0, 0, 0.1);
    margin: 10px -15px;
}
.v-align div {
    height: 40px;
    line-height: 40px;
    background: rgba(86, 61, 124, 0.15);
    border: 1px solid rgba(86, 61, 124, 0.2);
    color: #333;
}
```

## column offset
* 列偏移,使用offset-{breakpoint}-*
```
<div class="container">
    <div class="row mt-5">
        <div class="col-md-4">第一列</div>
        <div class="col-md-4 offset-md-4">往右偏移四列</div>
    </div>
    <div class="row mt-5">
        <!-- 前面的列发生偏移后面的列同样会跟着偏移 -->
        <div class="col-3 offset-md-3">第一列</div>
        <div class="col-3">第二列</div>
    </div>
    <div class="row mt-5">
        <div class="col-sm-5 col-md-6">小屏幕占五列,中屏占六列</div>
        <div class="col-sm-5 col-md-6 offset-sm-3 offset-md-5">小屏偏移三列,中屏偏移五列</div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
.v-align {
    height: 100px;
    background: rgba(255, 0, 0, 0.1);
    margin: 10px -15px;
}
.v-align div {
    height: 40px;
    line-height: 40px;
    background: rgba(86, 61, 124, 0.15);
    border: 1px solid rgba(86, 61, 124, 0.2);
    color: #333;
}
```

## column spacing
* 间距 使用margin工具可以让列之间产生间距
  - mr-{breakpoint}-auto 使右侧的列远离到最右边(就是右侧的列到最左边)
  - ml-{breakpoint}-auto 使左侧的列远离到最左边(就是左侧的列到最右边)
```
<div class="container">
    <div class="row mt-5">
        <div class="col-md-4">第一列</div>
        <div class="col-md-4 ml-auto">第二列,跑到最右边</div>
    </div>
    <div class="row mt-5">
        <div class="col-md-3 ml-md-auto">在中屏下,离左边距离自动计算</div>
        <div class="col-md-3 ml-md-auto">在中屏下,离左边距离自动计算</div>
    </div>
    <div class="row mt-5">
        <div class="col-auto mr-auto">宽度由内容撑开,离右边的距离是auto</div>
        <div class="col-auto">宽度由内容撑开</div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
.v-align {
    height: 100px;
    background: rgba(255, 0, 0, 0.1);
    margin: 10px -15px;
}
.v-align div {
    height: 40px;
    line-height: 40px;
    background: rgba(86, 61, 124, 0.15);
    border: 1px solid rgba(86, 61, 124, 0.2);
    color: #333;
}
```

## column nesting
* 嵌套 每一个列里面可以再继续放行,嵌套里面的元素会以父级的宽度为标准,再分12个列
```
<div class="container">
    <div class="row mt-5">
        <div class="col-sm-9" style="height: 150px; background: grey;">父级的第一列
          <div class="row">
            <div class="col-sm-8 col-6">子级的第一列,小屏下占八列,超小屏下占六列</div>
            <div class="col-sm-4 col-6">子级的第一列,小屏下占四列,超小屏下占六列</div>
          </div>
        </div>
        <div class="col-sm-3" style="height: 150px; background: pink;"></div>
    </div>
</div>

.row div {
    height: 100px;
    background: #0f0;
    border: 1px solid #000;
    color: #fff;
}
.v-align {
    height: 100px;
    background: rgba(255, 0, 0, 0.1);
    margin: 10px -15px;
}
.v-align div {
    height: 40px;
    line-height: 40px;
    background: rgba(86, 61, 124, 0.15);
    border: 1px solid rgba(86, 61, 124, 0.2);
    color: #333;
}
```