## 矩形(strokeRect)

1.使用线段描绘矩形,如<index.html>所示
2.使用 strokeRect() 描边矩形 如<index1.html>所示
strokeStyle：设置描边的属性（颜色、渐变、图案）
strokeRect(x, y, width, height)：描边矩形（x和y是矩形左上角起点；width 和 height 是矩形的宽高）
strokeStyle 必须写在 strokeRect() 前面，不然样式不生效。

## 填充(fillRect)
使用 fillRect() 填充矩形 如<index2.html>所示
fillRect() 和 strokeRect() 方法差不多，但 fillRect() 的作用是填充
需要注意的是，fillStyle 必须写在 fillRect() 之前，不然样式不生效。

同时使用 strokeRect() 和 fillRect()
同时使用 strokeRect() 和 fillRect() 会产生描边和填充的效果如<index3.html>所示

## 矩形(rect)
使用 rect() 生成矩形 如<index4.html>所示
rect() 和 fillRect() 、strokeRect() 的用法差不多，唯一的区别是：
strokeRect() 和 fillRect() 这两个方法调用后会立即绘制；rect() 方法被调用后，不会立刻绘制矩形，而是需要调用 stroke() 或 fill() 辅助渲染。