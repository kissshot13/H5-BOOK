```
标签云的时候，好象除了点击率高的字体会放的特别大外，点击率差不多的，往往都是采用不同的颜色来进行区分，如果页面上内容很少，我们还能手动控制一下。如果数据很多。。。黑黑，恐怕你只能随机了。

如果你想用javascript的随机，那么，司徒正美可是为你收集了不少方法哦，你可以挑一些作为自己的项目中的基本代码。

原文如下：

在制作饼图或标签云时，我们通常需要很多颜色，方法有二。一是准备一组漂亮的候选颜色，二是随机生成颜色。在数量很多或不明确时，我想后者就是唯一的出路了。谷歌了一下，整理如下，按由浅入深的顺序排列。

实现1 JavaScript代码
var getRandomColor = function(){ return '#' + (function(color){ return (color += '0123456789abcdef'[Math.floor(Math.random()*16)]) && (color.length == 6) ? color : arguments.callee(color); })(''); }

随机生成6个字符然后再串到一起，闭包调用自身与三元运算符让程序变得内敛，初心者应该好好学习这种写法。

实现2JavaScript代码var getRandomColor = function(){ return (function(m,s,c){ return (c ? arguments.callee(m,s,c-1) : '#') + s[m.floor(m.random() * 16)] })(Math,'0123456789abcdef',5) }

把Math对象，用于生成hex颜色值的字符串提取出来，并利用第三个参数来判断是否还继续调用自身。

实现3JavaScript代码Array.prototype.map = function(fn, thisObj) { var scope = thisObj || window; var a = []; for ( var i=0, j=this.length; i < j; ++i ) { a.push(fn.call(scope, this[i], i, this)); } return a; }; var getRandomColor = function(){ return '#'+'0123456789abcdef'.split('').map(function(v,i,a){ return i>5 ? null : a[Math.floor(Math.random()*16)] }).join(''); }

这个要求我们对数组做些扩展，map将返回一个数组，然后我们再用join把它的元素串成字符。

实现4JavaScript代码var getRandomColor = function(){ return '#'+Math.floor(Math.random()*16777215).toString(16); }

这个实现非常逆天，虽然有点小bug。我们知道hex颜色值是从#000000到#ffffff，后面那六位数是16进制数，相当于"0x000000" 到"0xffffff"。这实现的思路是将hex的最大值ffffff先转换为10进制，进行random后再转换回16进制。我们看一下，如何得到 16777215 这个数值的。

JavaScript代码

alert(parseInt("0xffffff",16).toString(10));



实现5JavaScript代码var getRandomColor = function(){ return '#'+(Math.random()*0xffffff<<0).toString(16); }



基本实现4的改进，利用左移运算符把0xffffff转化为整型。这样就不用记16777215了。由于左移运算符的优先级比不上乘号，因此随机后再左移，连Math.floor也不用了。

实现6JavaScript代码var getRandomColor = function(){ return '#'+(function(h){ return new Array(7-h.length).join("0")+h })((Math.random()*0x1000000<<0).toString(16)) }

修正上面版本的bug（无法生成纯白色与hex位数不足问题）。0x1000000相当0xffffff+1，确保会抽选到0xffffff。在闭包里我们处理hex值不足6位的问题，直接在未【应该是末】位补零。

实现7JavaScript代码var getRandomColor = function(){ return '#'+('00000'+(Math.random()*0x1000000<<0).toString(16)).slice(-6); }

这次在前面补零，连递归检测也省了。

上面版本生成颜色的范围算是大而全，但随之而来的问题是颜色不好看，于是实现8搞出来了。它生成的颜色相当鲜艳。

实现8JavaScript代码var getRandomColor = function(){ return "hsb(" + Math.random() + ", 1, 1)"; }
```