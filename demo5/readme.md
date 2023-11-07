## 文本
### 样式 font 
和 CSS 设置 font 差不多，Canvas 也可以通过 font 设置样式。
```javascript
cxt.font = 'font-style font-variant font-weight font-size/line-height font-family'
// 如果需要设置字号 font-size，需要同时设置 font-family。
cxt.font = '30px 宋体'
```

### 描边 strokeText() <index.html>
使用 strokeText() 方法进行文本描边
```javascript
// text: 字符串，要绘制的内容
// x: 横坐标，文本左边要对齐的坐标（默认左对齐）
// y: 纵坐标，文本底边要对齐的坐标
// maxWidth: 可选参数，表示文本渲染的最大宽度（px），如果文本超出 maxWidth 设置的值，文本会被压缩。
strokeText(text, x, y, maxWidth)
```

### 设置描边颜色 strokeStyle <index1.html>
使用 strokeStyle 设置描边颜色。

### 填充 fillText <index2.html>
使用 fillText() 可填充文本。
语法和 strokeText() 一样。
```javascript
fillText(text, x, y, maxWidth)
```

### 设置填充颜色 fillStyle <index3.html>
使用 fillStyle 可以设置文本填充颜色。

### 获取文本长度 measureText() <index4.html>
measureText().width 方法可以获取文本的长度，单位是 px 。

### 水平对齐方式 textAlign <index5.html>
使用 textAlign 属性可以设置文字的水平对齐方式，一共有5个值可选

start: 默认。在指定位置的横坐标开始。
end: 在指定坐标的横坐标结束。
left: 左对齐。
right: 右对齐。
center: 居中对齐。

从上面的例子看，start 和 left 的效果好像是一样的，end 和 right 也好像是一样的。
在大多数情况下，它们的确一样。但在某些国家或者某些场合，阅读文字的习惯是 从右往左 时，start 就和 right 一样了，end 和 left 也一样。这是需要注意的地方。

### 垂直对齐方式 textBaseline <index6.html>
使用 textBaseline 属性可以设置文字的垂直对齐方式。
在使用 textBaseline 前，需要自行了解 css 的文本基线。
textBaseline 可选属性：
  alphabetic: 默认。文本基线是普通的字母基线。
  top: 文本基线是 em 方框的顶端。
  bottom: 文本基线是 em 方框的底端。
  middle: 文本基线是 em 方框的正中。
  hanging: 文本基线是悬挂基线。

注意：在绘制文字的时候，默认是以文字的左下角作为参考点进行绘制