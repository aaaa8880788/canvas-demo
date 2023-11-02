## 图片
### 渲染图片
在 Canvas 中可以使用 drawImage() 方法绘制图片。
渲染图片的方式有2中，一种是在JS里加载图片再渲染，另一种是把DOM里的图片拿到 canvas 里渲染。

渲染的语法：
```javascript
// image: 要渲染的图片对象。
// dx: 图片左上角的横坐标位置。
// dy: 图片左上角的纵坐标位置。
drawImage(image, dx, dy)
```

## JS版 <index.html>
在 JS 里加载图片并渲染，有以下几个步骤：
创建 Image 对象
引入图片
等待图片加载完成
使用 drawImage() 方法渲染图片

## DOM版 <index1.html>
因为图片是从 DOM 里获取到的，所以一般来说，只要在 window.onload 这个生命周期内使用 drawImage 都可以正常渲染图片。
本例使用了 css 的方式，把图片的 display 设置成 none 。因为我不想被 <img> 影响到本例讲解。
实际开发过程中按照实际情况设置即可。

## 设置图片宽高 <index2.html>
前面的例子都是直接加载图片，图片默认的宽高是多少就加载多少。
如果需要指定图片宽高，可以在前面的基础上再添加两个参数：
```javascript
drawImage(image, dx, dy, dw, dh)
```
image、 dx、 dy 的用法和前面一样。
dw 用来定义图片的宽度，dh 定义图片的高度。

## 截取图片 <index3.html>
截图图片同样使用drawImage() 方法，只不过传入的参数数量比之前都多，而且顺序也有点不一样了。
```javascript
drawImage(image, sx, sy, sw, sh, dx, dy, dw, dh)
// 以上参数缺一不可
// image: 图片对象
// sx: 开始截取的横坐标
// sy: 开始截取的纵坐标
// sw: 截取的宽度
// sh: 截取的高度
// dx: 图片左上角的横坐标位置
// dy: 图片左上角的纵坐标位置
// dw: 图片宽度
// dh: 图片高度
```