# 轮播图

## 轮播图

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css"
      integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk"
      crossorigin="anonymous"
    />
    <style>
      body {
        margin-bottom: 200px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="row">
        <div class="col">
          <!-- carousel轮播图的基本样式,slide表示轮播图是否有过渡,carousel-fade表示轮播图使用透明度过渡(透明度必须配合slide，否则无效),data-ride="carousel"轮播图能否自动播放，默认值是false -->
          <div class="carousel slide" data-ride="carousel">
            <!-- carousel-inner内容区样式 -->
            <div class="carousel-inner">
              <!-- carousel-item轮播图每一项样式,轮播图哪项需要显示加上active -->
              <div class="carousel-item active">
                <!-- 图片自适应，可以设置img-fluid或者d-block和w-100 -->
                <img src="./images/pic_01.jpg" alt="" class="d-block w-100" />
              </div>
              <div class="carousel-item">
                <img src="./images/pic_02.jpg" alt="" class="d-block w-100" />
              </div>
              <div class="carousel-item">
                <img src="./images/pic_03.jpg" alt="" class="d-block w-100" />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row mt-5">
        <div class="col">
          <!-- data-interval设置轮播图的时间间隔，默认是5000,该属性可以不仅可以使用在轮播图父级也可以使用在每一项轮播图上,data-keyboard表示能否使用键盘左右键控制轮播图,默认值为true,data-pause表示鼠标悬停在轮播图上是否停止，默认值是hover，鼠标悬停停止,也可以设置成boolean类型的值,data-wrap表示轮播图是否循环播放 -->
          <div
            class="carousel slide"
            data-ride="carousel"
            id="control"
            data-interval="1000"
            data-keyboard="true"
            data-pause="true"
            data-wrap="true"
          >
            <div class="carousel-inner">
              <!-- 单独设置每一项的过渡时间 -->
              <div class="carousel-item active" data-interval="2000">
                <img class="img-fluid" src="./images/pic_01.jpg" alt="" />
                <!-- carousel-caption表示给每一项添加文本 -->
                <div class="carousel-caption d-none d-md-block">
                  <h5>第一张图片的标题</h5>
                  <p>第一张图的内容</p>
                </div>
              </div>
              <div class="carousel-item">
                <img class="img-fluid" src="./images/pic_02.jpg" alt="" />
                <div class="carousel-caption d-none d-md-block">
                  <h5>第一张图片的标题</h5>
                  <p>第一张图的内容</p>
                </div>
              </div>
              <div class="carousel-item">
                <img class="img-fluid" src="./images/pic_03.jpg" alt="" />
                <div class="carousel-caption d-none d-md-block">
                  <h5>第一张图片的标题</h5>
                  <p>第一张图的内容</p>
                </div>
              </div>
            </div>
            <!-- 添加左右箭头, carousel-control-prev是添加箭头样式,data-slide="prev"是添加箭头的事件
            href="#control"使用a标签的href绑定轮播图的id起到对应作用,三者缺一不可 -->
            <a href="#control" class="carousel-control-prev" data-slide="prev">
              <span class="carousel-control-prev-icon"></span>
            </a>
            <a href="#control" class="carousel-control-next" data-slide="next">
              <span class="carousel-control-next-icon"></span>
            </a>
            <!-- 添加指示器, carousel-indicators指示器的基本样式 -->
            <ol class="carousel-indicators">
              <!-- data-target表示目标轮播图的id，data-slide-to表示当前轮播图是第几项 active表示当前选中轮播图的项 -->
              <li data-target="#control" data-slide-to="0" class="active"></li>
              <li data-target="#control" data-slide-to="1"></li>
              <li data-target="#control" data-slide-to="2"></li>
            </ol>
          </div>
        </div>
      </div>
      <!-- 事件与方法 -->
      <div class="row mt-5">
        <div class="col">
          <div class="carousel slide" id="methods">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img class="img-fluid" src="./images/pic_01.jpg" alt="" />
              </div>
              <div class="carousel-item">
                <img class="img-fluid" src="./images/pic_02.jpg" alt="" />
              </div>
              <div class="carousel-item">
                <img class="img-fluid" src="./images/pic_03.jpg" alt="" />
              </div>
            </div>
            <!-- 因为通过事件去处理，所以不需要给轮播图添加data-的属性,而a标签中的href属性，不要删除，删除href属性会导致a标签失去一些特有属性，而且不用设置成href="#"会导致浏览器刷新，所以建议设置成href="javascript:;" -->
            <a href="javascript:;" class="carousel-control-prev btn-prev">
              <span class="carousel-control-prev-icon"></span>
            </a>
            <a href="javascript:;" class="carousel-control-next btn-next">
              <span class="carousel-control-next-icon"></span>
            </a>
            <ol class="carousel-indicators btn-dot">
              <li class="active"></li>
              <li></li>
              <li></li>
            </ol>
          </div>
        </div>
      </div>
      <button class="btn btn-primary play">开始</button>
      <button class="btn btn-primary pause">暂停</button>
    </div>
    <script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
    <script
      src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"
      integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV"
      crossorigin="anonymous"
    ></script>
    <script>
      //方法
      $(".carousel").carousel({
        interval: 2000,
      $(".play").click(function () {
        $(".carousel").carousel("cycle");
      });
      $(".pause").click(function () {
        $(".carousel").carousel("pause");
      });
      $(".btn-prev").click(function () {
        $("#methods").carousel("prev");
      });
      $(".btn-next").click(function () {
        $("#methods").carousel("next");
      });
      $(".btn-dot li").each(function(index, element){
        $(element).click(function(){
          $("#methods").carousel(index);
        });
      });
      //事件
      //所有轮播事件都在轮播本身（即 <div class="carousel">）下被触发,当调用 slide 方法时，此事件会立即触发
      $("#methods").on("slide.bs.carousel", function(e){
        console.log("开始走");
        //e.direction表示当前轮播方向, e.relatedTarget表示滑动到指定DOM元素，e.to表示下一项索引,e.from表示当前项索引
        console.log(e.direction, e.relatedTarget, e.to, e.from);
      });
      $("#methods").on("slid.bs.carousel", function(e){
        console.log("走完");
        console.log(e.direction, e.relatedTarget, e.to, e.from);
      });
    </script>
  </body>
</html>

```
