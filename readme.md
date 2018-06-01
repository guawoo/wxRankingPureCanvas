# 简介
本微信小游戏排行榜纯canvas通用模块是基于egret一个开源的纯canvas排行榜修改而来，原项目地址是
[https://github.com/peony-ma/wxOpenDataContext/tree/proto][1]

感谢原作者的辛勤劳动。

我修改了其中部分代码，主要是增加了对玩家头像的处理和添加了部份注释。


# 关于Demo
Demo是以cocos creator为例子编写的，因为其它引擎操作步骤都差不多，如果是egret则可以直接使用原项目的工程。

# 一些问题
不知道为什么在cocos creator项目中，子域的显示会有一些模糊，别的引擎没有这个现象，但基本不影响整体效果。可以接受。

# 如何使用
### cocos creator
生成好微信小游戏后，打开微信小游戏的目录，找到game.json文件，修改里面的内容，把它原来的关于子域的字段删除，它的默认子域字段是

"subContext": "wx-____"

删除它，添加

"openDataContext": "openDataContext"

如有不同，请参看Demo里的game.json文件。
然后把assets文件夹和openDataContext文件夹复杂到你的微信小游戏目录，即可使用。

assets文件夹是存放排行榜的图片素材。
openDataContext文件夹下的index.js是排行榜绘制的主要文件。

如果需要修改排行榜，直接编辑openDataContext文件夹下的index.js文件即可。

### egret或者其它引擎
同上，主要是修改game.json文件，保证拥有字段
"openDataContext": "openDataContext"
然后把assets文件夹和openDataContext文件夹复杂到你的微信小游戏目录。


# 注意
cocos creator每次生成微信小游戏都会把原工程项目删除，请注意保存你的assets文件夹和openDataContext文件夹。

# 为什么使用纯canvas绘制子域排行榜
原因很简单，因为占用空间小，只有一个index.js文件，才10几k，如果用引擎生成的话，估摸都要几百k

# 缺点
没有引擎的支付，很多功能的制作都将变得复杂。手动对坐标绘制也十分麻烦。

  [1]: https://github.com/peony-ma/wxOpenDataContext/tree/proto
