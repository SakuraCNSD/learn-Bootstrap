# 下拉菜单

## 下拉菜单

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
      <!-- 单一按钮下拉菜单 -->
      <div class="row mt-5">
        <div class="col-2">
          <!-- dropdown下拉菜单的初始化样式 -->
          <div class="dropdown">
            <!-- dropdown-toggle表示给点击标签添加箭头， data-toggle="dropdown"表示给按钮添加事件 -->
            <button
              class="btn btn-primary dropdown-toggle"
              data-toggle="dropdown"
            >
              button标签下拉
            </button>
            <!-- dropdown-menu表示下拉菜单内容区域的样式 -->
            <div class="dropdown-menu">
              <!-- dropdown-item表示下拉菜单每一项的样式,Bootstrap3版本中菜单每一项都必须使用a标签，而Bootstrap4版本没有要求 -->
              <a href="#" class="dropdown-item">Action</a>
              <a href="#" class="dropdown-item">Active</a>
              <a href="#" class="dropdown-item">Something</a>
            </div>
          </div>
        </div>
        <div class="col-2">
          <a
            href="javascript:;"
            class="btn btn-primary dropdown-toggle"
            data-toggle="dropdown"
            >a标签下拉</a
          >
          <div class="dropdown-menu">
            <a href="#" class="dropdown-item">Active</a>
            <a href="#" class="dropdown-item">Something</a>
            <!-- dropdown-divider用来添加分割线,在Bootstrap3版本中divider表示分割线 -->
            <div class="dropdown-divider"></div>
            <a href="#" class="dropdown-item">Each</a>
          </div>
        </div>
      </div>
      <!-- 分离式按钮下拉菜单 -->
      <div class="row mt-5">
        <div class="col-3">
          <!-- 父级可以不用dropdown类名，因为下拉菜单的父级只需要提供相对定位，只要有相对定位就行btn-group已经提供position:relative -->
          <div class="btn-group">
            <button class="btn btn-success">分离式按钮下拉菜单</button>
            <!-- dropdown-toggle-split只是将该按钮的尺寸变小(添加左右padding和white-space:nowarp) -->
            <button
              class="dropdown-toggle btn btn-success dropdown-toggle-split"
              data-toggle="dropdown"
            ></button>
            <div class="dropdown-menu">
              <div class="dropdown-item">Action</div>
              <div class="dropdown-item">Another action</div>
              <div class="dropdown-item">Something else here</div>
              <div class="dropdown-item">Separated link</div>
            </div>
          </div>
        </div>
      </div>
      <!-- 下拉菜单尺寸,在Bootstrap3版本中还有一个更小的尺寸btn-xs -->
      <div class="row mt-5">
        <div class="col-3">
          <div class="dropdown">
            <button
              class="btn btn-danger btn-lg dropdown-toggle"
              data-toggle="dropdown"
            >
              大按钮
            </button>
            <div class="dropdown-menu">
              <div class="dropdown-item">北京</div>
              <div class="dropdown-item">上海</div>
              <div class="dropdown-item">广州</div>
            </div>
          </div>
        </div>
        <div class="col-3">
          <button
            class="btn btn-danger btn-sm dropdown-toggle"
            data-toggle="dropdown"
          >
            小按钮
          </button>
          <div class="dropdown-menu">
            <div class="dropdown-item">北京</div>
            <div class="dropdown-item">上海</div>
            <div class="dropdown-item">广州</div>
          </div>
        </div>
        <div class="col-2 btn-group">
          <button class="btn btn-danger">大按钮</button>
          <button
            class="btn btn-danger dropdown-toggle dropdown-toggle-split"
            data-toggle="dropdown"
          ></button>
          <div class="dropdown-menu">
            <div class="dropdown-item">北京</div>
            <div class="dropdown-item">上海</div>
            <div class="dropdown-item">广州</div>
          </div>
        </div>
      </div>
      <!-- 下拉方向，Bootstrap3版本中只有上下两个方向没有左右方向 -->
      <div class="row mt-5">
        <!-- 通过给下拉菜单父级添加dropup、dropleft、dropright、dropdown显示不同方向的箭头 -->
        <div class="dropup">
          <button class="btn btn-dark dropdown-toggle" data-toggle="dropdown">
            不同方向下拉菜单
          </button>
          <div class="dropdown-menu">
            <div class="dropdown-item">北京</div>
            <div class="dropdown-item">上海</div>
            <div class="dropdown-item">广州</div>
          </div>
        </div>
      </div>
      <!-- 菜单项 -->
      <div class="row mt-5">
        <div class="col">
          <button
            class="btn btn-primary dropdown-toggle"
            data-toggle="dropdown"
          >
            菜单项按钮
          </button>
          <!-- dropdown-menu-right表示下拉菜单的对齐方式，默认值是dropdown-menu-left -->
          <div class="dropdown-menu dropdown-menu-right">
            <button class="dropdown-item">北京</button>
            <button class="dropdown-item">上海</button>
            <button class="dropdown-item">深圳</button>
          </div>
        </div>
      </div>
      <!-- 非交互式下拉菜单 -->
      <div class="row mt-5">
        <div class="col">
          <div class="dropdown-menu show">
            <!-- dropdown-item-text表示非交互式下拉菜单的内容样式 -->
            <span class="dropdown-item-text">非点击下拉菜单</span>
            <!-- dropdown-header表示下拉菜单的标题,这里样式会覆盖其它样式，无论是h1、h2等样式都会被覆盖 -->
            <h5 class="dropdown-header">下拉菜单标题</h5>
            <!-- active表示当前选中下拉菜单的哪一项，disabled表示下拉菜单该项禁用 -->
            <a href="#" class="dropdown-item">北京</a>
            <a href="#" class="dropdown-item active">上海</a>
            <a href="#" class="dropdown-item disabled">广州</a>
          </div>
        </div>
      </div>
      <!-- 偏移属性 -->
      <div class="row mt-5" style="margin-top: 200px !important;">
        <div class="col">
          <div class="dropdown">
            <!-- 按钮设置data-offset="x, y"表示下拉菜单偏移量 -->
            <button
              class="btn btn-success dropdown-toggle"
              data-toggle="dropdown"
              data-offset="10, 20"
            >
              菜单项中的偏移
            </button>
            <!-- data-referencw="parent"根据父级来改变下拉菜单的偏移 -->
            <div class="dropdown-menu" data-reference="parent">
              <a href="#" class="dropdown-item">北京</a>
              <a href="#" class="dropdown-item">上海</a>
              <a href="#" class="dropdown-item">广州</a>
            </div>
          </div>
        </div>
      </div>
      <!-- 方法 -->
      <div class="row mt-5">
        <div class="col">
          <div class="dropdown">
            <button class="btn btn-secondary dropdown-toggle methodsBtn">
              通过方法交换下拉菜单
            </button>
            <div
              class="dropdown-menu"
              id="dropdown-menu"
              data-reference="parent"
            >
              <a href="#" class="dropdown-item">北京</a>
              <a href="#" class="dropdown-item">上海</a>
              <a href="#" class="dropdown-item">广州</a>
            </div>
          </div>
        </div>
      </div>
      <!-- 事件 -->
      <div class="row mt-5">
        <div class="col">
          <div class="dropdown" id="eventMenu">
            <button
              class="btn btn-secondary dropdown-toggle"
              data-toggle="dropdown"
            >
              通过事件监听下拉菜单
            </button>
            <div class="dropdown-menu">
              <a href="#" class="dropdown-item">北京</a>
              <a href="#" class="dropdown-item">上海</a>
              <a href="#" class="dropdown-item">广州</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
    <script
      src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js"
      integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN"
      crossorigin="anonymous"
    ></script>
    <script
      src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"
      integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV"
      crossorigin="anonymous"
    ></script>
    <script>
      $(".methodsBtn").click(function () {
        // $("#dropdown-menu").dropdown("show");
        // $("#dropdown-menu").dropdown("hide");
        // $("#dropdown-menu").dropdown("toggle"); //使用方法操作下拉菜单定位有问题，点击按钮下拉菜单不知道父级是谁显示位置有问题，所以需要添加data-reference="parent"纠正，还有一个问题$("#dropdown-menu").dropdown("toggle");点击按钮显示之后无法隐藏
        //代替toggle方法
        $("#dropdown-menu").toggle(
          function () {
            $("#dropdown-menu").dropdown("show");
          },
          function () {
            $("#dropdown-menu").dropdown("hide");
          }
        );
      });
      //所有下拉选单事件在 .dropdown-menu 的父元素下触发，监听.dropdown元素
      $("#eventMenu").on("show.bs.dropdown", function () {
        console.log("下拉菜单显示"); //显示下拉菜单时触发
      });
      $("#eventMenu").on("hide.bs.dropdown", function () {
        console.log("下拉菜单隐藏"); //下拉菜单隐藏时触发
      });
      $("#eventMenu").on("shown.bs.dropdown", function () {
        console.log("下拉菜单显示并完成过渡动画"); //下拉菜单显示并完成过渡动画后触发
      });
      $("#eventMenu").on("hidden.bs.dropdown", function () {
        console.log("下拉菜单隐藏并完成过渡动画"); //下拉菜单隐藏并完成过渡动画后触发
      });
    </script>
  </body>
</html>
```
