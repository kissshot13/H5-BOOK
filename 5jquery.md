###事件
 - 在页面加载后执行任务。`$(document).ready()`处理程序可以用来触发函数中的代码。与Windows.onload事件相比：
  - 当文档完全下载到浏览器中时。会触发Windows.onload事件。这意味着页面上的全部元素对于js都可以操作。
  - `$(document).ready()`注册的事件处理程序。则会在DOM完全就绪并可以使用时调用。却并不意味着所有关联文件都已经下载好了。
  - 一般来说，使用`$(document).ready()`要优于使用onload事件。单必须明白，因为支持的文件并没有加载完成，所以类似图像的高度和宽度这样的属性不一定有效。如果要访问这些属性，就可能要实现一个onload事件处理程序。
   - `$(document).ready(function(){})`可以简写成`$(function(){})`
 - 向.ready()回调函数传入参数
  - 在某些情况下，可能有必要在同一个页面使用多个JavaScript库。由于很多库都使用$标识符，因此就需要一种方式来避免名称冲突。
  - jq提供jQuery.noConfict()方法。调用该方法可以把$控制符的控制权让渡还给其他库。使用的一般模式为：
```
<script src="prototype.js"></script>
<script src="jquery.js"></script>
<script>
    jQuery.noConflict();
</script>
<script src="myscript.js"></script>
```