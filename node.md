# 警告框、徽章、面包屑导航、按钮、按钮组

## 警告框

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <!-- integrity属性是为了防止CDN被劫持，导致下载的文件是被篡改过的（比如通过 DNS 劫持），有了 integrity 就可以检查文件是否是原版 -->
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css"
      integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk"
      crossorigin="anonymous"
    />
  </head>
  <body>
    <!-- 提醒框 -->
    <div class="container">
      <div class="alert alert-primary">alert-primary</div>
      <div class="alert alert-secondary">alert-secondary</div>
      <div class="alert alert-success">alert-success</div>
      <div class="alert alert-danger">alert-danger</div>
      <div class="alert alert-warning">alert-warning</div>
      <div class="alert alert-info">alert-info</div>
      <div class="alert alert-light">alert-light</div>
      <div class="alert alert-dark">alert-dark</div>
      <!-- 链接颜色 -->
      <div class="alert alert-primary">
        <a class="alert-link" href="#">alert-primary</a>
      </div>
      <div class="alert alert-secondary">
        <a class="alert-link" href="#">alert-secondary</a>
      </div>
      <div class="alert alert-success">
        <a class="alert-link" href="#">alert-success</a>
      </div>
      <div class="alert alert-danger">
        <a class="alert-link" href="#">alert-danger</a>
      </div>
      <div class="alert alert-warning">
        <a class="alert-link" href="#">alert-warning</a>
      </div>
      <div class="alert alert-info">
        <a class="alert-link" href="#">alert-info</a>
      </div>
      <div class="alert alert-light">
        <a class="alert-link" href="#">alert-light</a>
      </div>
      <div class="alert alert-dark">
        <a class="alert-link" href="#">alert-dark</a>
      </div>
      <!-- 在警告框里面添加额外内容 -->
      <div class="alert alert-success">
        <h4 class="alert-heading">这是一个标题</h4>
        <p>
          这是一段很长很长的内容,这是一段很长很长的内容,这是一段很长很长的内容,这是一段很长很长的内容,这是一段很长很长的内容
        </p>
      </div>
      <!-- 关闭提示框
      在提醒框中加入一个按钮并加上 .alert-dismissible 类就可以了。 如果你要将按钮放在右上角的位置可以使用 .close 将按钮的位置进行调整。
      关闭用的按钮请加上 data-dismiss="alert" 属性用来触发 JavaScript 函数。另外尽量使用 <button> 元素来创建按钮，这可以在所有设备上提供正确的效果。
      不想用 JS？你还可以使用 .fade 和 .show 类来调整提醒框的显示或隐藏，通过transition来完成；bootstrap3版本中没有fade和show，但是有fade和in；这两个类名必须同时出现才有效
    -->
      <div class="alert alert-warning alert-dismissible fade show">
        可以关闭的警告框,但是需要引入到jquery和bootstrap.js
        <button class="close" data-dismiss="alert">&times;</button>
      </div>
      <div class="alert alert-danger myAlert">
        通过按钮关闭警告框
      </div>
      <button class="colseBtn">关闭警告框</button>
    </div>
    <script src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.0/dist/js/bootstrap.min.js"
      integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI"
      crossorigin="anonymous"
    ></script>
    <script>
      //通过方法关闭警告框
      $(".colseBtn").click(function(){
        $(".myAlert").alert("close");
      });
      //通过事件监听警告框关闭事件
      $(".myAlert").on("close.bs.alert", function(){ //第一个参数事件名，第二个参数回调函数
        alert("close方法被调用了");
      });
      $(".myAlert").on("closed.bs.alert", function(){ //第一个参数事件名，第二个参数回调函数
        alert("警告框关闭了");
      });
    </script>
  </body>
</html>
```

## 徽章

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
      .first {
        font-size: 1.5rem;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- 徽章通过badge提供基础样式，徽章通过badge-primary等提供背景颜色 -->
      <div class="row first">
        <!-- 徽章通过使用相对字体大小和 em 单位来缩放以匹配直接父元素的大小 -->
        <span class="badge">徽章</span>
        <span class="badge badge-primary">徽章</span>
        <span class="badge badge-secondary">徽章</span>
        <span class="badge badge-success">徽章</span>
        <span class="badge badge-warning">徽章</span>
        <span class="badge badge-danger">徽章</span>
        <span class="badge badge-info">徽章</span>
        <span class="badge badge-light">徽章</span>
        <span class="badge badge-dark">徽章</span>
      </div>
      <div class="row mt-5">
        <h1><span class="badge badge-primary">徽章</span></h1>
        <h2><span class="badge badge-secondary">徽章</span></h2>
        <h3><span class="badge badge-success">徽章</span></h3>
        <h4><span class="badge badge-warning">徽章</span></h4>
        <h5><span class="badge badge-danger">徽章</span></h5>
        <h6><span class="badge badge-info">徽章</span></h6>
      </div>
      <!-- 再按钮中使用徽章 -->
      <div class="row mt-5">
        <button class="btn btn-primary">
          在按钮中使用徽章<span class="badge badge-light">5</span>
        </button>
      </div>
      <!-- 胶囊徽章 -->
      <div class="row mt-5">
        <span class="badge badge-primary badge-pill">胶囊徽章</span>
        <span class="badge badge-secondary badge-pill">胶囊徽章</span>
        <span class="badge badge-success badge-pill">胶囊徽章</span>
        <span class="badge badge-warning badge-pill">胶囊徽章</span>
        <span class="badge badge-danger badge-pill">胶囊徽章</span>
        <span class="badge badge-info badge-pill">胶囊徽章</span>
        <span class="badge badge-light badge-pill">胶囊徽章</span>
        <span class="badge badge-dark badge-pill">胶囊徽章</span>
      </div>
      <!-- 再链接上使用徽章，使用 .badge-* 可在 <a> 元素上调整 hover 和 focus 的效果 -->
      <div class="row mt-5">
        <a href="#" class="badge badge-primary">链接徽章</a>
        <a href="#" class="badge badge-success">链接徽章</a>
      </div>
    </div>
  </body>
</html>

```

## 面包屑导航

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
  </head>
  <body>
    <div class="container">
      <div class="row d-block">
        <nav aria-label="breadcrumb">
          <ol class="breadcrumb">
            <li class="breadcrumb-item">
              <a href="#">首页</a>
            </li>
            <li class="breadcrumb-item">
              <a href="#">关于我们</a>
            </li>
            <li class="breadcrumb-item active">
              联系我们
            </li>
          </ol>
        </nav>
      </div>
    </div>
  </body>
</html>
```

## 按钮

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
  </head>
  <body>
    <div class="container">
      <div class="row d-block mt-5">
        <button class="btn">按钮</button>
        <button class="btn btn-primary">按钮</button>
        <button class="btn btn-secondary">按钮</button>
        <button class="btn btn-success">按钮</button>
        <button class="btn btn-info">按钮</button>
        <button class="btn btn-warning">按钮</button>
        <button class="btn btn-danger">按钮</button>
        <button class="btn btn-light">按钮</button>
        <button class="btn btn-dark">按钮</button>
        <button class="btn btn-link">按钮</button>
      </div>
      <!-- 其它类型的按钮 -->
      <div class="row mt-5 d-block">
        <a href="#" class="btn btn-primary">a标签按钮</a>
        <button class="btn btn-secondary" type="submit">
          button标签按钮
        </button>
        <input type="button" value="input标签" class="btn btn-success" />
        <input type="sbumit" value="input标签" class="btn btn-warning" />
        <input type="reset" value="input标签" class="btn btn-danger" />
      </div>
      <!-- 外框按钮 -->
      <div class="mt-5 row d-block">
        <button class="btn btn-outline-primary">外框按钮</button>
        <button class="btn btn-outline-danger">外框按钮</button>
      </div>
      <!-- 按钮大小 -->
      <div class="row mt-5 d-block">
        <button class="btn btn-primary btn-lg">大按钮</button>
        <button class="btn btn-warning btn-sm">小按钮</button>
      </div>
      <!-- block类型的按钮 -->
      <div class="row mt-5 d-block">
        <button class="btn btn-primary btn-lg btn-block">块级大按钮</button>
        <button class="btn btn-info btn-block">块级按钮</button>
      </div>
      <!-- 启用与停用状态按钮 -->
      <div class="row mt-5 d-block">
        <a href="#" class="btn btn-success active">启用按钮</a>
        <button class="btn btn-primary active">启用状态</button>

        <a href="#" class="btn btn-primary disabled">停用状态</a>
        <button class="btn btn-info" disabled>停用状态</button>
      </div>
      <!-- 切换按钮的active状态 -->
      <div class="row d-block mt-5">
        <button class="btn btn-primary" data-toggle="button">
          点击切换按钮
        </button>
      </div>
      <!-- 选项卡效果 -->
      <div class="row mt-5">
        <div class="btn-group btn-group-toggle" data-toggle="buttons">
          <label class="btn btn-secondary active">
            <input type="radio" name="options" checked />Active
          </label>
          <label class="btn btn-secondary">
            <input type="radio" name="options" />Radio
          </label>
          <label class="btn btn-secondary">
            <input type="radio" name="options" />checkoutBox
          </label>
        </div>
      </div>
      <!-- 动态切换按钮active状态 -->
      <div class="row mt-5 d-block">
        <button class="btn btn-primary" id="btn">动态切换</button>
      </div>
    </div>
    <script src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.0/dist/js/bootstrap.min.js"
      integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI"
      crossorigin="anonymous"
    ></script>
    <script>
      //获取id属性为btn的按钮，如果按钮是激活状态(具有active类名)就变成没有激活状态，如果按钮是没有激活状态就变成激活状态
      $("#btn").button("toggle");
    </script>
  </body>
</html>
```

## 按钮组

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
  </head>
  <body>
    <div class="container">
      <div class="row mt-5 d-block">
        <div class="btn-group">
          <button class="btn btn-primary">left</button>
          <button class="btn btn-primary">center</button>
          <button class="btn btn-primary">right</button>
        </div>
      </div>
      <!-- 按钮工具列 -->
      <div class="row mt-5 btn-toolbar">
        <div class="btn-group mr-2">
          <button class="btn btn-success">1</button>
          <button class="btn btn-success">2</button>
          <button class="btn btn-success">3</button>
        </div>
        <div class="btn-group mr-2">
          <button class="btn btn-success">4</button>
          <button class="btn btn-success">5</button>
          <button class="btn btn-success">6</button>
        </div>
        <div class="btn-group">
          <button class="btn btn-success">8</button>
        </div>
      </div>
      <div class="row mt-5 btn-toolbar">
        <div class="btn-group mr-2">
          <button class="btn btn-info">1</button>
          <button class="btn btn-info">2</button>
          <button class="btn btn-info">3</button>
          <button class="btn btn-info">4</button>
        </div>
        <div class="input-group">
          <div class="input-group-prepend">
            <div class="input-group-text">@</div>
          </div>
          <input
            type="text"
            placeholder="Input group example"
            class="form-control"
          />
        </div>
      </div>
      <!-- 缩放 -->
      <div class="row mt-5">
        <div class="btn-group btn-group-lg mr-2">
          <button class="btn btn-primary">大按钮</button>
          <button class="btn btn-primary">大按钮</button>
          <button class="btn btn-primary">大按钮</button>
        </div>
        <div class="btn-group mr-2">
          <button class="btn btn-primary">按钮</button>
          <button class="btn btn-primary">按钮</button>
          <button class="btn btn-primary">按钮</button>
        </div>
        <div class="btn-group btn-group-sm">
          <button class="btn btn-primary">小按钮</button>
          <button class="btn btn-primary">小按钮</button>
          <button class="btn btn-primary">小按钮</button>
        </div>
      </div>
      <!-- 下拉菜单 -->
      <div class="row mt-5">
        <div class="btn-group">
          <button class="btn btn-secondary">1</button>
          <button class="btn btn-secondary">2</button>
          <div class="btn-group">
            <button
              class="btn btn-secondary dropdown-toggle"
              data-toggle="dropdown"
            >
              Dropdown
            </button>
            <div class="dropdown-menu">
              <a class="dropdown-item" href="#">Dropdown link</a>
              <a class="dropdown-item" href="#">Dropdown link</a>
            </div>
          </div>
        </div>
      </div>
      <!-- 按钮垂直排列 -->
      <div class="row mt-5">
        <div class="btn-group-vertical">
          <button class="btn btn-danger">垂直按钮</button>
          <button class="btn btn-danger">垂直按钮</button>
          <div class="btn-group">
            <button
              class="btn btn-danger dropdown-toggle"
              data-toggle="dropdown"
            >
              Dropdown
            </button>
            <div class="dropdown-menu">
              <a href="#" class="dropdown-item">dropdown link</a>
              <a href="#" class="dropdown-item">dropdown link</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <script src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
  </body>
</html>
```
