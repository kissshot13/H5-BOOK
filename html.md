    Bootstrap 使用一种响应式网格布局——可轻松实现将多个元素放入一行并指定各个元素的相对宽度的需求。Bootstrap 中大多数的class属性都可以设置于 `div` 元素中

请注意，在这张图表中，class属性 `col-md-*` 正被使用。在这里，`md` 表示 medium \(中等的\)，`*` 代表一个数字，它指定了这个元素所占的列宽。通过此图表的属性设置可知，在中等大小的屏幕上\(例如笔记本电脑\)，元素的列宽被指定了。

在我们创建的 Cat Photo App 中，将会使用`col-xs-*` ，其中 `xs` 是 extra small 缩写（应用于较小的屏幕，比如手机屏幕），`*`是你需要填写的数字，代表在一行中,各个元素应该占的列宽。![](/assets/FaYuui8.png)

`<div class="row">```` <div class="col-xs-4"><button class="btn btn-block btn-primary">Like</button></div>```` <div class="col-xs-4"><button class="btn btn-block btn-info">Info</button></div>```` <div class="col-xs-4"><button class="btn btn-block btn-danger">Delete</button></div>```` </div>`

结果如下：

![](/assets/Snip20161009_2.png)



