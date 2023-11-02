## 多边形
Canvas 要画多边形，需要使用 moveTo() 、 lineTo() 和 closePath() 。

1. 三角形 如<index.html>所示
虽然三角形是常见图形，但 canvas 并没有提供类似 rect() 的方法来绘制三角形。
需要确定三角形3个点的坐标位置，然后使用 stroke() 或者 fill() 方法生成三角形。

注意，默认情况下不会自动从最后一个点连接到起点。最后一步需要设置一下 cxt.lineTo(50, 50) ，让它与 cxt.moveTo(50, 50) 一样。这样可以让路径回到起点，形成一个闭合效果。
但这样做其实是有点问题的，而且也比较麻烦，要记住起始点坐标。
上面的闭合操作，如果遇到设置了 lineWidth 或者 lineJoin 就会有问题

2. 菱形 如<index1.html>所示

## 圆形
绘制圆形的方法是 arc()。 如<index2.html>所示
```javascript
// x 和 y: 圆心坐标
// r: 半径
// sAngle: 开始角度
// eAngle: 结束角度
// counterclockwise: 绘制方向（true: 逆时针; false: 顺时针），默认 false
arc(x, y, r, sAngle, eAngle，counterclockwise)
```
开始角度和结束角度，都是以弧度为单位。例如 180°就写成 Math.PI ，360°写成 Math.PI * 2 ，以此类推。
在实际开发中，为了让自己或者别的开发者更容易看懂弧度的数值，1°应该写成 Math.PI / 180。

100°: 100 * Math.PI / 180
110°: 110 * Math.PI / 180
241°: 241 * Math.PI / 180


注意：绘制圆形之前，必须先调用 beginPath() 方法！！！ 在绘制完成之后，还需要调用 closePath() 方法！！！

## 半圆
如果使用 arc() 方法画圆时，没做到刚好绕完一周（360°）就直接闭合路径，就会出现半圆的状态。如<index3.html>所示

## 弧线
使用 arc() 方法画半圆时，如果最后不调用 closePath() 方法，就不会出现闭合路径。也就是说，那是一条弧线。

在 canvas 中，画弧线有两种方法：arc() 和 arcTo() 。
arc() 画弧线
如果想画一条 0° ~ 30° 的弧线，可以这样写 如<index4.html>所示

arcTo() 画弧线
arcTo() 的使用方法会更加复杂，如果初学看不太懂的话可以先跳过，看完后面的再回来补补。
```javascript
// cx: 两切线交点的横坐标
// cy: 两切线交点的纵坐标
// x2: 结束点的横坐标
// y2: 结束点的纵坐标
// radius: 半径
arcTo(cx, cy, x2, y2, radius)
```
其中，(cx, cy) 也叫控制点，(x2, y2) 也叫结束点。
是不是有点奇怪，为什么没有 x1 和 y1 ？
(x1, y1) 是开始点，通常是由 moveTo() 或者 lineTo() 提供。

arcTo() 方法利用 开始点、控制点和结束点形成的夹角，绘制一段与夹角的两边相切并且半径为 radius 的圆弧。
举个例子 如<index5.html>所示