
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

* [一、知乎-建议反馈-屏幕截图-原理(rasterizeHTML)](#一知乎-建议反馈-屏幕截图-原理rasterizehtml)
* [二、添加Github标题和提交commit的图标](#二添加github标题和提交commit的图标)
* [三、知乎加载图片时从模糊到清晰的这个效果](#三知乎加载图片时从模糊到清晰的这个效果)
* [四、百度M站将公共的代码缓存到localStorage](#百度M站将公共的代码缓存到localStorage)
* [五、淘宝和天猫首页都用到了哪些技巧或者技术](#淘宝和天猫首页都用到了哪些技巧或者技术)
* [六、新浪微博都用到了哪些技巧或者技术](#新浪微博都用到了哪些技巧或者技术)

## 一、知乎-建议反馈-屏幕截图-原理(rasterizeHTML)

将HTML渲染到指定的Canvas里  
知乎就是采用了这个库  

项目地址：[rasterizeHTML.js](http://bluezhan.com/stroller/rasterizeHTML/)  

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

由鄙人修改和更新了一下下，别见笑： [bluezhan\rasterizeHTML.js](http://bluezhan.com/stroller/rasterizeHTML/)   
这个项目原处出自 [cburgmer](https://github.com/cburgmer)-[rasterizeHTML.js](https://github.com/cburgmer/rasterizeHTML.js)

## 二、添加Github标题和提交commit的图标

Emoji Cheat Sheet 是绘文字短代码小抄列表。Github上支持Emoji表情符号，短码，而不是特殊字符。 ：heart_eyes： 相当于 :heart_eyes: 。只需将鼠标悬停显示短代码，点击复制简码。有许多网站的支持这种类型的短代码： Github, Basecamp, Slack, Trello, Hackpad, Qiita, Zendesk, Ello. 

网址：https://www.webpagefx.com/tools/emoji-cheat-sheet/

:sunglasses::dizzy_face::imp::smiling_imp::neutral_face::no_mouth::innocent::alien::yellow_heart::blue_heart::purple_heart::heart::green_heart::broken_heart::heartbeat::heartpulse::two_hearts::revolving_hearts::cupid::dizzy::boom::collision::anger::exclamation::question::grey_exclamation::grey_question::zzz::dash::sweat_drops::notes::musical_note::fire::hankey::poop::shit::runner::running::couple::trollface::sunny::umbrella::cloud::snowflake::snowman::zap::cyclone::foggy::ocean::cat::dog::mouse::hamster::rabbit::wolf::frog::tiger::koala::bear::pig::pig_nose::cow::boar::monkey_face::monkey::horse::racehorse::camel::sheep::elephant::panda_face::snake::bird::baby_chick::hatched_chick::hatching_chick::chicken::penguin::turtle::bug::honeybee::ant::beetle::snail::octopus::tropical_fish::fish::whale::whale2::dolphin::cow2::ram::rat::water_buffalo::tiger2::rabbit2::dragon::goat::rooster::dog2::pig2::mouse2::ox::dragon_face::blowfish::crocodile::dromedary_camel::leopard::cat2::poodle::paw_prints::bouquet::cherry_blossom::tulip::four_leaf_clover::rose::sunflower::hibiscus::maple_leaf::leaves::fallen_leaf::herb::mushroom::cactus::palm_tree::evergreen_tree::deciduous_tree::chestnut::seedling::blossom::ear_of_rice::shell::globe_with_meridians::sun_with_face::full_moon_with_face::new_moon_with_face::new_moon::waxing_crescent_moon::first_quarter_moon::waxing_gibbous_moon::full_moon::waning_gibbous_moon::last_quarter_moon::waning_crescent_moon::last_quarter_moon_with_face::first_quarter_moon_with_face::crescent_moon::earth_africa::earth_americas::earth_asia::volcano::milky_way::partly_sunny::octocat::squirrel::bamboo::gift_heart::dolls::school_satchel::mortar_board::flags::fireworks::sparkler::wind_chime::rice_scene::jack_o_lantern::ghost::santa::christmas_tree::gift::bell::no_bell::tanabata_tree::tada::confetti_ball::balloon::crystal_ball::cd::dvd::floppy_disk::camera::video_camera::movie_camera::computer::tv::iphone::phone::telephone::telephone_receiver::pager::fax::minidisc::vhs::sound::speaker::mute::loudspeaker::mega::hourglass::hourglass_flowing_sand::alarm_clock::watch::radio::satellite::loop::mag::mag_right::unlock::lock::lock_with_ink_pen::closed_lock_with_key::key::bulb::flashlight::high_brightness::low_brightness::electric_plug::battery::calling::email::mailbox::postbox::bath::bathtub::shower::toilet::wrench::nut_and_bolt::hammer::seat::moneybag::yen::dollar::pound::euro::credit_card::money_with_wings::e-mail::inbox_tray::outbox_tray::envelope::incoming_envelope::postal_horn::mailbox_closed::mailbox_with_mail::mailbox_with_no_mail::package::door::smoking::bomb::gun::hocho::pill::syringe::page_facing_up::page_with_curl::bookmark_tabs::bar_chart::chart_with_upwards_trend::chart_with_downwards_trend::scroll::clipboard::calendar::date::card_index::file_folder::open_file_folder::scissors::pushpin::paperclip::black_nib::pencil2::straight_ruler::triangular_ruler::closed_book::green_book::blue_book::orange_book::notebook::notebook_with_decorative_cover::ledger::books::bookmark::name_badge::microscope::telescope::newspaper::football::basketball::soccer::baseball::tennis::8ball::rugby_football::bowling::golf::mountain_bicyclist::bicyclist::horse_racing::snowboarder::swimmer::surfer::ski::spades::hearts::clubs::diamonds::gem::ring::trophy::musical_score::musical_keyboard::violin::space_invader::video_game::black_joker::flower_playing_cards::game_die::dart::mahjong::clapper::memo::pencil::book::art::microphone::headphones::trumpet::saxophone::guitar::shoe::sandal::high_heel::lipstick::boot::shirt::tshirt::necktie::womans_clothes::dress::running_shirt_with_sash::jeans::kimono::bikini::ribbon::tophat::crown::womans_hat::mans_shoe::closed_umbrella::briefcase::handbag::pouch::purse::eyeglasses::fishing_pole_and_fish::coffee::tea::sake::baby_bottle::beer::beers::cocktail::tropical_drink::wine_glass::fork_and_knife::pizza::hamburger::fries::poultry_leg::meat_on_bone::spaghetti::curry::fried_shrimp::bento::sushi::fish_cake::rice_ball::rice_cracker::rice::ramen::stew::oden::dango::egg::bread::doughnut::custard::icecream::ice_cream::shaved_ice::birthday::cake::cookie::chocolate_bar::candy::lollipop::honey_pot::apple::green_apple::tangerine::lemon::cherries::grapes::watermelon::strawberry::peach::melon::banana::pear::pineapple::sweet_potato::eggplant::tomato::corn:

## 三、知乎加载图片时从模糊到清晰的这个效果

[[译]Medium 是如何优化图片加载的](http://www.jackpu.com/medium-shi-ru-he-zuo-tu-pian-jia-zai-de/)  
[使用渐进式JPEG来提升用户体验](https://www.biaodianfu.com/progressive-jpeg.html)  
[网站如何解决图片过大加载慢的问题？](https://www.zhihu.com/question/23655692/answer/164643803)  
[使用高斯模糊的效果逐步加载图片（仿 Medium）](https://segmentfault.com/a/1190000006743512)  

__TODO__

-动手弄个Demo

## 四、百度M站将公共的代码缓存到localStorage

百度M站使用了localStorage缓存Js和css文件。

[webapp之路--百度手机前端经验（转）](http://www.cnblogs.com/dunken/p/4383101.html)   
[Web移动端使用localStorage缓存Js和css文件](http://blog.csdn.net/a497785609/article/details/48321405)    
[手机百度localstorage细粒度缓存介绍](http://js8.in/2015/12/06/%E6%89%8B%E6%9C%BA%E7%99%BE%E5%BA%A6localstorage%E7%BB%86%E7%B2%92%E5%BA%A6%E7%BC%93%E5%AD%98%E4%BB%8B%E7%BB%8D/)    
[localStorage的黑科技-js和css缓存机制](http://www.jianshu.com/p/0fa0bf842bbb)


## 五、淘宝和天猫首页都用到了哪些技巧或者技术

[知乎-淘宝和天猫首页都用到了哪些技巧或者技术？](https://www.zhihu.com/question/46149490)    

![](https://github.com/bluezhan/stroller/raw/master/images/taobao.png) 

#### 淘宝：  
```
    background: url(jpg) no-repeat #F40;
    background-image: -webkit-image-set(url(jpg) 1x,url(.png) 2x);
    background-image: -moz-image-set(url(jpg) 1x,url(.png) 2x);
    background-image: -ms-image-set(url(jpg) 1x,url(.png) 2x);
    background-image: -o-image-set(url(jpg) 1x,url(.png) 2x);
    _background-image: url(jpg);
```
```
 <ins></ins>
```

在隐藏元素的时候记得把动画过渡也关闭了。   
display: none;  
transition: none;  

像大部分优化的机制就是使用JavaScript来处理DOM的植入   
不过淘宝使用textatea来装 HTML ~~~  

![](https://github.com/bluezhan/stroller/raw/master/images/1479696653291.png) 
  
对字体渲染  

-webkit-font-smoothing（听说在Mac OS 才有效）   
[CSS 中 -webkit-font-smoothing: antialiased 反而让字体更难看了?](https://segmentfault.com/q/1010000000467910)

## 六、新浪微博都用到了哪些技巧或者技术

长链接的技术，long polling  
cometd 支持长连接，WebSocket

[新浪微博平台架构解析](https://sdk.cn/news/5593)  
[从新浪微博的改版谈网页重构](http://kb.cnblogs.com/page/114649/)  
[使用BigPipe提升浏览速度](http://velocity.oreilly.com.cn/2011/ppts/WK_velocity.pdf)  
[名站技术分析 — facebook奇特的页面加载技术](http://www.cnblogs.com/BearsTaR/archive/2010/06/18/facebook_html_chunk.html)  
[围观STK](http://www.cnblogs.com/jkisjk/archive/2012/08/11/about_stk.html) 


### 关于新浪微博的那些前端知识

大概在2年前，我在查看新浪微博web源码的时候，记得发现他们在对前端文件的压缩方式很有印象。

我们来看看这JavaScript文件请求链接：

```js
https://g.alicdn.com/kissy/k/1.4.2/??event-min.js,event/dom/base-min.js,event/base-min.js,dom/base-min.js,event/dom/shake-min.js,event/dom/focusin-min.js,event/custom-min.js,node-min.js,anim-min.js,anim/base-min.js,promise-min.js,anim/timer-min.js,anim/transition-min.js
```

```js
https://g.alicdn.com/kissy/k/1.4.2/??cookie-min.js,overlay-min.js,component/container-min.js,component/control-min.js,base-min.js,component/manager-min.js,xtemplate/runtime-min.js,component/extension/shim-min.js,component/extension/align-min.js,component/extension/content-xtpl-min.js,component/extension/content-render-min.js
```

是的，我们现在看到是这里面有个字眼 `kissy` ；这不难说，因为新浪微博被阿里承包了，固然会推广使用了阿里的技术。  

这不是重点，在新浪微博易主之前它也是这样弄的。  

就是这条链接放置所要请求的JavaScript并将它们一起合并了。  

我当时一脸懵逼，怎么这么吊，而且我当时是在用 Node 的相关压缩处理方式或工具，比如 r.js、grunt、gulp等等。  

这不难看出，这是服务器或者框架那边做了文件逻辑处理。  

好啦，简简单单谈个开始，我们再聊聊新浪微博的其它前端实现的知识。

### 资源目录

这就是网站请求的资源目录：  

![](https://github.com/bluezhan/stroller/raw/master/images/weibo-1.png)

不难看出来，对JavaScript、HTML、images启动了多个域名处理。

### 看看CSS结构


#### 未登录时请求的CSS

![](https://github.com/bluezhan/stroller/raw/master/images/weibo-2.png)

文件目录：

```js
  - frame.css
  - comb_login_v2.css
  - skin.css
  - base.css
```

##### frame.css

请求链接：  

```js
http://img.t.sinajs.cn/t6/style/css/module/base/frame.css
```

我还特么去看了一遍内容源码。  

大部分CSS命名有 `W_`、`B_` 、`WB_` 开头命名的，很明显吧。      
不过还有 `S_`、`SW_` 、`PCD_`、`UI_` 开头的....  
其它小写开头的命名的我就不提了。  

顾名思义这CSS是框架骨架CSS了。  

不过不过，这些简写命名也行是压缩工具或者等等其它东西特地弄的。

##### comb_login_v2.css

这个CSS从命名可以看出是对登录特殊的CSS。  
里面出现 `W_unlogin_`、`B_unlog`、`PCD_pictext_i` 为重。

##### skin.css

这个不用说了就是皮肤的CSS，里面控制呈现的CSS：

```
color: #fff;
background-color: #fff;
border-color: #fff;
...
```


##### base.css

至于base.css，为毛隔不到0.5ms加载了两次呢，不明白。  

![](https://github.com/bluezhan/stroller/raw/master/images/weibo-3.png)

看得出是嵌入淘宝登录逻辑带过来的，为毛要去请求淘宝账号呢，嘿嘿嘿.......你懂得。  

#### 登录时请求的CSS

![](https://github.com/bluezhan/stroller/raw/master/images/weibo-4.png)

多了几个CSS  

```
 - home_A.css
 - extra.css
 - PCD_mplayer.css
```


#### 定时请求push_count.json


每隔30秒请求一下下面这个链接：

```
Request URL:http://rm.api.weibo.com/2/remind/push_count.json?trim_null=1&with_dm_group=0&with_settings=1&exclude_attitude=1&with_common_cmt=1&with_comment_attitude=1&with_common_attitude=1&with_moments=1&with_dm_unread=1&msgbox=true&with_page_group=1&with_chat_group=1&with_chat_group_notice=1&_pid=1&count=0&source=351354573&status_type=0&callback=STK_14795361469975
```


#### bigpipe 技术

通过JavaScript动态生成HTML  
http://blog.csdn.net/fyqcdbdx/article/details/7042355  
http://idlelife.org/archives/969  
http://timyang.net/  
https://github.com/JacksonTian/fks  
http://caibaojian.com/some-fe  
http://www.yixieshi.com/10354.html  
http://web.jobbole.com/86343/  
http://kb.cnblogs.com/page/114649/  
http://tech.sina.com.cn/i/2010-11-16/14434871585.shtml  
https://zhuanlan.zhihu.com/p/23074882  

#### STK 脚本库

http://www.cnblogs.com/jkisjk/archive/2012/08/11/about_stk.html

#### 页面分片加载

http://www.cnblogs.com/BearsTaR/archive/2010/05/19/flush_chunk_encoding.html  
facebook使用了chunk 对页面进行分块输出

#### document.execCommand

https://developer.mozilla.org/zh-CN/docs/Web/API/Document/execCommand

#### 前端4秒的分水岭事件

// TODO

#### DNS Prefetch

// TODO

#### 微博背后的那些算法

http://blog.csdn.net/zhangyunpengchang/article/details/50349981

http://blog.csdn.net/stdcoutzyx/article/details/18814627

#### 千万级规模高性能、高并发

http://www.wtoutiao.com/p/1catvAN.html
http://mobile.51cto.com/comment-492447.htm
http://web.jobbole.com/86343/


#### 面试题

// TODO

#### 《新浪微博我们所不知道的发展》PPT

技术，小步快跑，媒体运营，定位，数据。

- 2009年 开始
- 2010年 推广起步
- 2011年 不断尝试，小步快跑
- 2012年 定位思考
- 2013年 大胆转型
- 2014年 媒体运营定型
- 2015年 起飞
- 2016年 起飞起飞再起飞

僵尸粉满天飞的那年，转行中...

#### 后文

一个勤奋的程序员不一定是一个好程序员，而一个懒惰的程序员却很有可能是一个好程序员。














