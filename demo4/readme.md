## 基础样式
### 描边 stroke()
前面的案例中，其实已经知道使用 stroke() 方法进行描边了。这里就不再多讲这个方法。

### 线条宽度 lineWidth <index.html>
lineWidth 默认值是 1 ，默认单位是 px。
```javascript
lineWidth = 线宽
```

### 线条颜色 strokeStyle <index1.html>
```javascript
strokeStyle = 颜色值
```

### 线帽 lineCap <index2.html>
线帽指的是线段的开始和结尾处的样式，使用 lineCap 可以设置
```javascript
lineCap = '属性值'
// butt: 默认值，无线帽
// square: 方形线帽
// round: 圆形线帽
```
使用 square 和 round 的话，会使线条变得稍微长一点点，这是给线条增加线帽的部分，这个长度在日常开发中需要注意。
线帽只对线条的开始和结尾处产生作用，对拐角不会产生任何作用。

### 拐角样式 lineJoin <index3.html>
如果需要设置拐角样式，可以使用 lineJoin 。
```javascript
lineJoin = '属性值'
// miter: 默认值，尖角
// round: 圆角
// bevel: 斜角
```

### 虚线 setLineDash() <index4.html>
使用 setLineDash() 方法可以将描边设置成虚线。
```javascript
setLineDash([])
// 需要传入一个数组，且元素是数值型。
// 虚线分3种情况
// 1.只传1个值
// 2.有2个值
// 3.有3个以上的值
```
此外，还可以始终 cxt.getLineDash() 获取虚线不重复的距离；
用 cxt.lineDashOffset 设置虚线的偏移位。

### 填充 <index5.html>
使用 fill() 可以填充图形，根据前面的例子应该掌握了如何使用 fill()
可以使用 fillStyle 设置填充颜色，默认是黑色。

### 非零环绕填充 <index6.html>
