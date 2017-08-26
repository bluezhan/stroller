
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

https://www.zhihu.com/question/46149490

![](https://github.com/bluezhan/stroller/raw/master/images/taobao.png) 

## 六、新浪微博都用到了哪些技巧或者技术

长链接的技术，long polling  
cometd 支持长连接，WebSocket

[新浪微博平台架构解析](https://sdk.cn/news/5593)  
[从新浪微博的改版谈网页重构](http://kb.cnblogs.com/page/114649/)  
[使用BigPipe提升浏览速度](http://velocity.oreilly.com.cn/2011/ppts/WK_velocity.pdf)  
[名站技术分析 — facebook奇特的页面加载技术](http://www.cnblogs.com/BearsTaR/archive/2010/06/18/facebook_html_chunk.html)  
[围观STK](http://www.cnblogs.com/jkisjk/archive/2012/08/11/about_stk.html)  
