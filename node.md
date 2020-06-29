# Bootstrap官方地址https://getbootstrap.com/

**Bootstrap可以快速构建响应式网站，所谓响应式就是同一个网站模板在不同终端设备中显示的内容都是相同。**

目前,大多数网站使用的Bootstrap的版本是3.3.7跟目前最新的4版本之间是有差异的，但核心内容不变。

**Bootstrap3版本和4版本之间的主要区别在于一些样式类名上的改变、浏览器的兼容性,主要关注IE浏览器，在3版本中能支持IE8(除了border-radius、box-shadow、transform、transition和placeholder这5个css3属性不支持),而4版本支持的IE最低版本是IE10，所以需要工作环境选用不同版本的Bootstrap版本。**

使用Bootstrap可以通过下载到本地，然后在页面中引入或者通过引入CDN
介绍3版本Bootstrap官网中下载的Bootstrap内容(https://getbootstrap.com/docs/3.3/getting-started/)
Download Bootstrap表示下载的Bootstrap是经过压缩处理,不包含任何文档或原始源文件。
Download source表示下载的Bootstrap里面包含源less、文档等核心描述文件,可以通过修改源less来改变Bootstrap。
Download Sass表示当前项目使用Sass预处理语言就可以下载此版本的Bootstrap。
4版本Bootstrap中使用的JS文件需要使用到jquery，但Bootstrap没有包含JS文件，所以需要自动添加。

# CND的引入
```
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
```
其中crossorigin和integrity两个属性是为了保证安全,corssoring是发送一个跨域请求,integrity的值是经过加密的hash值，发送请求时会将hash值带上,服务器收到请求后会查看是否匹配hash值,如果匹配服务器才会响应,如果不匹配服务器可以拒绝响应。

```
<meta name="viewport" content="width=devive-width, initial-scale=1, shrink-to-fit=0">
```
设置移动端设备的宽度,其中4版本Bootstrap比3版本Bootstrap多出一条属性shrink-to-fit=0;这一条主要是针对iso 9