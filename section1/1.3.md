Bootstrap 使用一种响应式网格布局——可轻松实现将多个元素放入一行并指定各个元素的相对宽度的需求。Bootstrap 中大多数的class属性都可以设置于 \`div\` 元素中

请注意，在这张图表中，class属性 `col-md-*` 正被使用。在这里，`md` 表示 medium \(中等的\)，`*` 代表一个数字，它指定了这个元素所占的列宽。通过此图表的属性设置可知，在中等大小的屏幕上\(例如笔记本电脑\)，元素的列宽被指定了。

在我们创建的 Cat Photo App 中，将会使用`col-xs-*` ，其中 `xs` 是 extra small 缩写（应用于较小的屏幕，比如手机屏幕），`*`是你需要填写的数字，代表在一行中,各个元素应该占的列宽。![](/assets/FaYuui8.png)

`<div class="row">`

`<div class="col-xs-4"><button class="btn btn-block btn-primary">Like</button></div>`

`<div class="col-xs-4"><button class="btn btn-block btn-info">Info</button></div>`

`<div class="col-xs-4"><button class="btn btn-block btn-danger">Delete</button></div>`

`</div>`

结果如下：

![](/assets/Snip20161009_2.png)

你可以用 span 标签来创建行内元素。还记得我们是怎样使用 `.btn-block`来创建填满整行的按钮吗？

这张图展示了 `inline` 元素与 `block-level`块级元素的区别：

![](/assets/O32cDWE.png)

通过使用 `span` 元素，你可以把几个元素放在一起。你甚至可以用此为一个元素的不同部分指定样式


 - 导航条组件

.navbar——设置nav元素为导航条组件；

.navbar-default——指定导航条组件为默认主题；

.navbar-inverse——指定导航条组件为黑色主题；

.navbar-fixed-top——设置导航条组件固定在顶部；

.navbar-fixed-bottom——设置导航条组件固定在底部；

.container-fluid——设置宽度充满父元素，即为100%；

.navbar-header——主要指定div元素为导航条组件包裹品牌图标及切换按钮；

.navbar-toggle——设置button元素为导航条组件的切换钮；

.collapsed——设置button元素为在视口小于768px时才显示；

.navbar-brand——设置导航条组件内的品牌图标；

.collapse——设置div元素为视口大于768px时显示；

.navbar-collapse——设置div元素为导航条组件各列表项的父元素；

.navbar-nav——设置ul为导航条组件内的列表元素;

.navbar-left——设置导航条内元素向左对齐；

.navbar-right——设置导航条内元素向右对齐；

.navbar-form——为导航条组件内部的表单组件；

.navbar-btn——为导航条组件内部的按钮样式；

.navbar-text——为导航条组件内部的文本样式；

.navbar-link——在标准的导航组件之外添加标准链接，让链接有正确的颜色和反色设置；

.breadcrumb——设置列表元素显示为路径导航组件；




##JQuery
 - 你还可以用jQuery改变除了CSS以外的属性。比如，你可以让按钮变不可选。

当你把按钮设置成不可选以后，这会让按钮变灰并且不能点击。

jQuery有一个.prop()的方法让你来调整元素的属性.

我们是这样来让按钮不可选的:
```
$("button").prop("disabled", true);
$("button").prop("disabled", true);
```
 - jQuery有一个appendTo()方法可以把选中的元素加到其他元素中。```$("#target4").appendTo("#left-well");```

![](/assets/Snip20161010_3.png)