## 直线
demo看index.html
## 注意点
1.默认宽高
canvas 有 默认的 宽度(300px) 和 高度(150px)
如果不在 canvas 上设置宽高，那 canvas 元素的默认宽度是300px，默认高度是150px。

2.设置 canvas 宽高
canvas 元素提供了 width 和 height 两个属性，可设置它的宽高。
需要注意的是，这两个属性只需传入数值，不需要传入单位（比如 px 等）。

```html
<canvas width="600" height="400"></canvas>
```

3.不能通过 CSS 设置画布的宽高
使用 css 设置 canvas 的宽高，会出现 内容被拉伸 的后果！！！

例如: index1所示

canvas 的默认宽度是300px，默认高度是150px。

如果使用 css 修改 canvas 的宽高（比如本例变成 400px * 400px），那宽度就由 300px 拉伸到 400px，高度由 150px 拉伸到 400px。
使用 js 获取 canvas 的宽高，此时返回的是 canvas 的默认值。
具体效果看index1.html

4.线条默认宽度和颜色
线条的默认宽度是 1px ，默认颜色是黑色。
但由于默认情况下 canvas 会将线条的中心点和像素的底部对齐，所以会导致显示效果是 2px 和非纯黑色问题。

5.IE兼容性高
暂时只有 IE 9 以上才支持 canvas 。但好消息是 IE 已经有自己的墓碑了。
如需兼容 IE 7 和 8 ，可以使用 ExplorerCanvas 。但即使是使用了 ExplorerCanvas 仍然会有所限制，比如无法使用 fillText() 方法等。

## 设置样式

lineWidth：线的粗细
strokeStyle：线的颜色
lineCap：线帽：默认: butt; 圆形: round; 方形: square
demo看index2.html

## 新开路径

开辟新路径的方法： beginPath()
在绘制多条线段的同时，还要设置线段样式，通常需要开辟新路径。
要不然样式之间会相互污染。
demo看index3.html

## 折线

如index4.html所示
