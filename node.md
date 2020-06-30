# 图片、表格、图文
## 图片
* 响应式图片(只要添加上img-fluid类名图片就变成响应式图片)
```
<img
    src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
      alt="Responsive image"
      class="img-fluid"
/>
```
* 缩略图(只要添加上img-thumbnail类名图片的外层会套上一个1px宽度的圆角边框)
```
<img
    src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
      alt="缩略图"
      class="img-thumbnail"
/>
```
* 圆角图片(只要添加上rounded类名图片就变成圆角,但是不是响应式图片,添加上img-fluid之后才是响应式图片)
```
<img
    src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
      alt="圆角图片"
      class="rounded img-fluid"
/>
```
* 图片对齐方式
```
<div class="container">
    <div class="row mt-5">
        <!-- 图片自己对齐通过浮动float-left和float-right类名 -->
        <div class="col">
          <img
            src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
            alt=""
            height="200px"
            class="float-left"
          />
          <img
            src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
            alt=""
            height="200px"
            class="float-right"
          />
        </div>
    </div>
</div>
```
```
<div class="container">
    <div class="row mt-5 text-left">
        <div class="col">
          <!-- 通过父级调整对齐,使用文本对齐方式,添加text-center、text-left或text-right类名 -->
          <img
            src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
            alt=""
            height="200px"
          />
          <img
            src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
            alt=""
            height="200px"
          />
        </div>
    </div>
</div>
```
```
<div class="container">
    <div class="row mt-5">
        <!-- 给图片添加d-block先变成block元素,在使用mx-auto设置margin: 0 auto -->
        <div class="col">
          <img
            src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png"
            alt=""
            height="200px"
            class="d-block mx-auto"
          />
        </div>
    </div>
</div>
```
* Picture标签
```
<div class="container">
    <div class="row mt-5">
        <picture>
          <source
            media="(min-width: 1200px)"
            srcset="
              https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593532915721&di=cd2fb4ca9fad3bc7cbb0c7ca7caba791&imgtype=0&src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fitem%2F201502%2F11%2F20150211214842_mWR8d.png
            "
          />
          <source
            media="(min-width: 992px)"
            srcset="
              https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593535559156&di=f47f00201303de0c388a428de3e5592c&imgtype=0&src=http%3A%2F%2Fimg.boqiicdn.com%2FData%2FBK%2FA%2F1409%2F5%2Fimg64991409897999.jpg
            "
          />
          <source
            media="(min-width: 768px)"
            srcset="
              https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593535833891&di=a5f770d1136c30e1e6af738bc8155857&imgtype=0&src=http%3A%2F%2Fdik.img.kttpdq.com%2Fpic%2F40%2F27835%2F3eaed79cd11788ce_1366x768.jpg
            "
          />
          <source
            media="(min-width: 576px)"
            srcset="
              https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593535875546&di=78214675d7dce83fba61908389161a6a&imgtype=0&src=http%3A%2F%2Fn.sinaimg.cn%2Ffront%2F496%2Fw640h656%2F20180829%2FNLqa-hikcahf2392709.jpg
            "
          />
          <!-- 当屏幕尺寸小于576px时显示该图片 -->
          <img
            src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593535730162&di=fab10e11d950ef6028b556cc36f3fa26&imgtype=0&src=http%3A%2F%2Fimg.wenjiwu.com%2Flife%2F201706%2F16-1F603110337.jpg"
            alt=""
          />
        </picture>
    </div>
</div>
```
**.webp图片格式,专门针对网页的图片,这种图片格式比png、jpg图片格式小几十倍,但是.webp格式的图片是高清图片,非常强大;但是这个格式的图片只有比较高级的浏览器才支持,所以就可以使用picture标签处理;PC端浏览器兼容情况：Chrome和fireFox完美支持,IE不支持;移动端：ios9.3版本及以上支持,android4.4版本以上支持,不包括android4.4版本**

## 表格
```
<div class="container">
    <div class="row">
        <!-- 响应式表格：响应式设计的表格允许水平滚动。 通过使用 .table 包装 .table-responsive ，使所有 viewport 都能响应。 或者，使用 .table-responsive{-sm|-md|-lg|-xl}选择一个最大断点，通过该断点可以获得响应;但是这里有一个问题：使用中文超过宽度会换行,而因为不会换行,所以使用中文需要屏幕尺寸很小才能看到滚动条,而使用英文很容易就撑开容器就能看到滚动条 -->
        <div class="table-responsive">
          <!-- 表格工具类：使用表格工具类可以给表格的列或者行单独上色,例如：table-active、table-default、table-primary、table-secondary、table-success、table-danger、table-warning、table-info、table-light、table-dark,其中table-dark颜色比较深,所以文字颜色也会改变需要形成对比 -->
          <!-- 带有条纹的行：给<table>使用 .table-striped 来给 <tbody> 的所有行添加条纹效果,结合表格工具类一起使用效果更佳-->
          <!-- 表格边框：加上这个 .table-bordered 类可以给表格内的所有单元添加边框 -->
          <!-- 去除表格边框：使用 .table-borderless 类来移除表格里的所有边框 -->
          <!-- 高亮：给<table>使用 .table-hover 类可以使 <tbody> 里的内容在获得鼠标停留时高亮显示 -->
          <!-- 更小的表格：使用 .table-sm 类可以让表格所有单元的间距缩小一半 -->
          <table
            class="table table-info table-striped table-bordered table-borderless table-hover table-sm"
          >
            <!-- <caption>的功能类似于表格的标题 -->
            <caption>
              课程表
            </caption>
            <!-- 表头选项：使用修饰符类 .thead-light 或 .thead-dark 使 <thead> 显示为浅灰色或深灰色 -->
            <thead class="thead-dark">
              <tr>
                <th>周一</th>
                <th>周二</th>
                <th>周三</th>
                <th>周四</th>
                <th>周五</th>
              </tr>
            </thead>
            <tbody>
              <!-- 暗色表格不提供常规表格背景类，但是，你可以使用文本或背景工具来实现类似的样式,例如：bg-primary、bg-success、bg-warning、bg-danger、bg-info -->
              <tr class="bg-primary">
                <td>语文</td>
                <td>数学</td>
                <td>英语</td>
                <td>生物</td>
                <td>化学</td>
              </tr>
              <tr>
                <td>语文</td>
                <td>数学</td>
                <td>英语</td>
                <td>生物</td>
                <td>化学</td>
              </tr>
              <tr>
                <td>语文</td>
                <td>数学</td>
                <td>英语</td>
                <td>生物</td>
                <td>化学</td>
              </tr>
              <tr>
                <td>语文</td>
                <td>数学</td>
                <td>英语</td>
                <td>生物</td>
                <td>化学</td>
              </tr>
              <tr>
                <td>语文</td>
                <td>数学</td>
                <td>英语</td>
                <td>生物</td>
                <td>化学</td>
              </tr>
            </tbody>
          </table>
        </div>
    </div>
</div>
```

## 图文区-Figures
* 图文去再Bootstrap3版本中没有,只有再Bootstrap4版本中才新增加
```
<div class="container">
    <div class="row">
        <!-- 图文区：所谓图文区就是展示图片及其说明,最外层是一个带有figure类名的figure标签,是HTML5中新出的标签,而里面的图片img需要添加img-fluid、rounded和figure-img使图片成为圆角响应式图片;然后figcaption标签是说明文字标签,需要添加类名figure-caption -->
        <figure class="figure">
          <img
            src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1593535875546&di=78214675d7dce83fba61908389161a6a&imgtype=0&src=http%3A%2F%2Fn.sinaimg.cn%2Ffront%2F496%2Fw640h656%2F20180829%2FNLqa-hikcahf2392709.jpg"
            alt=""
            class="img-fluid rounded figure-img"
          />
          <figcaption class="figure-caption text-center">一叶知秋</figcaption>
        </figure>
    </div>
</div>
```