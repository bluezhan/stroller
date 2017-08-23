# stroller

> `stroller`	英[ˈstrəʊlə(r)]、美[ˈstroʊlə(r)]  
  n.	散步者，闲逛者;


### 一、知乎-建议反馈-屏幕截图-原理(asterizeHTML)


将HTML渲染到指定的Canvas里  
知乎就是采用了这个库  

项目地址：[rasterizeHTML.js]()  

#### API

实现将浏览器整个或部分页面渲染到Canvas里。

```js
rasterizeHTML.drawURL( url [, canvas] [, options] )
rasterizeHTML.drawHTML( html [, canvas] [, options] )
rasterizeHTML.drawDocument( document [, canvas] [, options] )
```

查看 [完整文档](https://github.com/cburgmer/rasterizeHTML.js/wiki/API) 和 [案例](https://github.com/cburgmer/rasterizeHTML.js/wiki/Examples)。

#### 原理

出于对安全的考虑，渲染HTML到Canvas上对浏览器是有限制的。 Firefox 提供`ctx.drawWindow()`这个方法来实现 , 但只有Chrome提供了 ([Canvas绘画图像](https://developer.mozilla.org/en/Drawing_Graphics_with_Canvas))。

如此描述到[绘画DOM内容到Canvas](http://robert.ocallahan.org/2011/11/drawing-dom-content-to-canvas.html) 和 [绘画DOM节点对象到Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Drawing_DOM_objects_into_a_canvas)，然而有可能通过将HTML嵌入SVG图像`<foreignObject>`,然后通过`ctx.drawImage`绘画产生的图像()。

除了SVG是不允许所以rasterizeHTML链接到外部资源。js将加载外部图像、字体和内联通过样式表和存储它们 [data: URIs](https://en.wikipedia.org/wiki/Data_URI_scheme) (或者是内联样式的元素)。

由鄙人修改和更新了一下下，别见笑： [bluezhan\rasterizeHTML.js]()   
这个项目原处出自 [cburgmer](https://github.com/cburgmer)-[rasterizeHTML.js](https://github.com/cburgmer/rasterizeHTML.js)

### 二、添加Github标题和提交commit的图标

Emoji Cheat Sheet 是绘文字短代码小抄列表。Github上支持Emoji表情符号，短码，而不是特殊字符。 ：heart_eyes： 相当于 :heart_eyes: 。只需将鼠标悬停显示短代码，点击复制简码。有许多网站的支持这种类型的短代码： Github, Basecamp, Slack, Trello, Hackpad, Qiita, Zendesk, Ello. 

网址：https://www.webpagefx.com/tools/emoji-cheat-sheet/
