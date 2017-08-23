
![](https://github.com/bluezhan/stroller/raw/master/images/logo.png)

<p align="center">
  <img src="https://img.shields.io/badge/language-HTML--CSS--JavaScript-green.svg">
  <img src="https://img.shields.io/badge/web-togo-orange.svg">
  <img src="https://img.shields.io/badge/license-MIT-ccc.svg">
  <img src="https://img.shields.io/badge/Don't-Panic-ff69b4.svg">
  <img src="https://img.shields.io/badge/stroller-0.1.1-ded76a.svg">
</p>


> `stroller`	英[ˈstrəʊlə(r)]、美[ˈstroʊlə(r)]  
  n.	散步者，闲逛者;


“作为个体的我到底是谁?”、“我又会成为谁?”、“我又如何成就着自己?”    

身份的焦虑带来了来自于空间、时间、及心灵的三重困境。在这个遥远的征途中，不断的调试、重叠、移位，以寻求精神的修复和重生。   

生活空间的位移所带来的变化，实际上又与传统和现代性的矛盾深刻交织在一起。   

我在我的代码下成为了一名浪荡子和闲逛者。  

__目了个录__

* [一、知乎-建议反馈-屏幕截图-原理(rasterizeHTML)](https://github.com/bluezhan/stroller#一知乎-建议反馈-屏幕截图-原理rasterizehtml)
* [二、添加Github标题和提交commit的图标](https://github.com/bluezhan/stroller#二添加github标题和提交commit的图标)


### 一、知乎-建议反馈-屏幕截图-原理(rasterizeHTML)

将HTML渲染到指定的Canvas里  
知乎就是采用了这个库  

项目地址：[rasterizeHTML.js](http://bluezhan.me/stroller/rasterizeHTML/)  

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

由鄙人修改和更新了一下下，别见笑： [bluezhan\rasterizeHTML.js](http://bluezhan.me/stroller/rasterizeHTML/)   
这个项目原处出自 [cburgmer](https://github.com/cburgmer)-[rasterizeHTML.js](https://github.com/cburgmer/rasterizeHTML.js)

### 二、添加Github标题和提交commit的图标

Emoji Cheat Sheet 是绘文字短代码小抄列表。Github上支持Emoji表情符号，短码，而不是特殊字符。 ：heart_eyes： 相当于 :heart_eyes: 。只需将鼠标悬停显示短代码，点击复制简码。有许多网站的支持这种类型的短代码： Github, Basecamp, Slack, Trello, Hackpad, Qiita, Zendesk, Ello. 

网址：https://www.webpagefx.com/tools/emoji-cheat-sheet/

:sunglasses::dizzy_face::imp::smiling_imp::neutral_face::no_mouth::innocent::alien::yellow_heart::blue_heart::purple_heart::heart::green_heart::broken_heart::heartbeat::heartpulse::two_hearts::revolving_hearts::cupid::dizzy::boom::collision::anger::exclamation::question::grey_exclamation::grey_question::zzz::dash::sweat_drops::notes::musical_note::fire::hankey::poop::shit::runner::running::couple::trollface::sunny::umbrella::cloud::snowflake::snowman::zap::cyclone::foggy::ocean::cat::dog::mouse::hamster::rabbit::wolf::frog::tiger::koala::bear::pig::pig_nose::cow::boar::monkey_face::monkey::horse::racehorse::camel::sheep::elephant::panda_face::snake::bird::baby_chick::hatched_chick::hatching_chick::chicken::penguin::turtle::bug::honeybee::ant::beetle::snail::octopus::tropical_fish::fish::whale::whale2::dolphin::cow2::ram::rat::water_buffalo::tiger2::rabbit2::dragon::goat::rooster::dog2::pig2::mouse2::ox::dragon_face::blowfish::crocodile::dromedary_camel::leopard::cat2::poodle::paw_prints::bouquet::cherry_blossom::tulip::four_leaf_clover::rose::sunflower::hibiscus::maple_leaf::leaves::fallen_leaf::herb::mushroom::cactus::palm_tree::evergreen_tree::deciduous_tree::chestnut::seedling::blossom::ear_of_rice::shell::globe_with_meridians::sun_with_face::full_moon_with_face::new_moon_with_face::new_moon::waxing_crescent_moon::first_quarter_moon::waxing_gibbous_moon::full_moon::waning_gibbous_moon::last_quarter_moon::waning_crescent_moon::last_quarter_moon_with_face::first_quarter_moon_with_face::crescent_moon::earth_africa::earth_americas::earth_asia::volcano::milky_way::partly_sunny::octocat::squirrel:
