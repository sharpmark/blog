---
layout: post
title: "拳打南山敬老院，脚踢北海幼儿园的 JavaScript"
date: 2016-04-09 18:00
comments: true
published: true
categories:
  - 产品和技术
---

起因是我近日对 [Atom 编辑器](https://atom.io/)的架构好奇，就去读了 Atom 和 Electron 的诞生历程。然后顺藤摸瓜的撸了 Node.js 等一些新的技术介绍，发觉 JavaScript 已经不是 20 年前的毛头小伙了……。它的触角已经伸展到几乎所有的编程领域，成了名副其实的万金油。本文就简单梳理一下我这几天看的无所不能的 JavaScript。


一、为表单验证而诞生的 JavaScript

1995 年 Erendan Eich 为网景（Netscape）设计了第一版 JavaScript，主要用于表单校验并获成功。爱搞自己一套的微软（Microsoft）随后也发布了自己的 JavaScript 方言 JScript。在其后几年微软和网景互坑互助，最终联合推动了 JavaScript 的标准化版本—— ECMAScript 的确立。

2000 年左右随着网站的高速发展， JavaScript 的价值越来越大，跟 <del>Dreamweaver/Fireworks （大雾）</del>HTML 和 CSS 并称网页三剑客。HTML 负责结构，CSS 负责样式，JavaScript 负责行为。JavaScript 成为网页必不可少的组成部分。

由于当时的机能限制，JavaScript 的使用场景有限，惊艳的动效都是由 Flash 负责。


二、前端制霸的 Ajax

1999 年，爱搞自己一套的微软又在 IE 里做了个 XMLHttpRequest 的对象，却没有太重视，直到 2005 年，Jesse James Garrett 基于当时的一些 XMLHttpRequest 的应用，提出了 Ajax (Asynchronous JavaScript and XML) 的概念。之前，网页向服务器提交数据（如发帖）就需要刷新页面来显示操作的结果，Ajax 通过异步交互实现无刷新的网页更新方式，使得网站的交互操作更接近原生应用。还记得我在大学机房第一次用 Google Maps 的时候，感受它丝滑流畅的拖动和放大缩小，直接跪了，这才是黑科技！

这个时期，随着 HTML/CSS 标准化，使得 JavaScript 具有了更重要的作用，比如操作 DOM 树；机能提升使得 JavaScript 可以实现比肩 Flash 的动画效果，而且更加轻量。所以涌现出以 [jQuery](http://jquery.com/) 为代表的无数前端库，极大的提升用网站的交互体验和视觉效果。JavaScript 借着 Ajax 和 Web2.0 的浪潮，成为真正意义上的前端王者。

再之后则涌现出 MVC 架构的 [Angular.js](https://angularjs.org)，专注于表现层的 [React.js](https://facebook.github.io/react/) 等框架，则是在“网页即是应用”的路上持续进化。


三、魔爪伸向服务端的 Node.js

2008年，Lars Bak 在他的丹麦农场为谷歌（Google）的 Chrome 写了性能超群的 JavaScript 引擎 V8，V8 做为 Chrome 杀手级的亮点功能之一（沙盒和多进程是我认为的另外两大杀手功能），对 Chrome 的成功功不可没。

2009年，Ryan Dahl 借助 V8 的卓越性能和 JavaScript 天生的单线程缺陷特性，脑洞大开的发布了 [Node.js](http://nodejs.org/) 项目。Node.js 是具有事件驱动，异步 I/O 特性的高性能，高并发，轻量级 Web 服务框架。江湖中也不时传来某公司用 Node.js 后少用了多少服务器的故事。

需要说明的是，Node.js 本身是基于 V8 引擎，也就是说它本身并不是用 JavaScript 编写的，而是用 C++。Node.js 服务上面跑的脚本语言是 JavaScript 而已。Node.js + JavaScript 的组合就像 Nginx + Lua，一个是底层服务，一个是上层脚本。

后来，Node.js 变成了一个通用的 JavaScript 运行时，可应用的领域不仅限于服务器。如果说 Ajax 是第一个引爆点，帮助 JavaScript 奠定了前端老大的地位，那 Node.js 就是第二个引爆点。随着 Node.js 的快速发展，JavaScript 真正变成了一种通用的脚本语言，在下面的各种领域大放异彩。


四、 CLI 应用的军火库 NPM

如果说 Node.js 是厨房，[NPM（Node Package Manager)](http://www.npmjs.com/) 则提供了丰富的各式食材，并在很短的时间成为了开发界最大的包管理平台。
在 NPM 上涌现出涵盖网络服务，数学，文档处理，数据库，开发工具等几乎涵盖所有领域的各类应用。可以访问 [Awesome Node.js](https://github.com/sindresorhus/awesome-nodejs#command-line-apps) 了解其强大之处。

五、奋战在移动端的 Hybird App

随着 iOS 和 Android 的崛起，只会 JavaScript 的前端工程师开始眼红收入超越自己的 iOS 和 Android 工程师，于是他们联合起来提出了 [PhoneGap](http://phonegap.com/)，一个将 HTML5 和 JavaScript 封装成移动应用的平台。希望借此实现开发一份代码，适配两个平台，赚三份工资的伟大理想。然而事与愿违， PhoneGap 生成的跨平台应用（Hybird App）由于性能、兼容性、对 native 功能支持不理想等问题，并没有被特别广泛的使用，也没有实现前端工程师的涨薪梦想。

基于网页的 Hybrid App 也有一些独特优势，比如可以远程推送更新，无需像原生程序一样需要编译和发布新版本，这个特性尤其适合电商或内容为主的应用。而且毕竟开发容易，可用于早期试错和产品方向验证。真正要追求性能和品质，还是要用原生代码（native code）来改写。所以很多应用采用了原生和网页混合模式，交互操作多，有性能要求，内容相对固定的部分用原生实现；重内容重排版需要经常更新的部分用网页实现，最大化两者的优势。


六、桌面端即是网页的 Electron

2014年，Atom 项目启动。随着 Atom 的演化，团队独立出用于支撑 Atom 跨平台的底层架构 Atom Shell，后更名为 [Electron](http://electron.atom.io/)。包括著名的 Slack，Visual Studio Code 的客户端都是基于 Electron 构建的。

Electron 底层是基于 Chromium 和 Node.js。Electron 做了几件事：

	1. 创建主进程（main process），主进程将为每个界面创建单独的渲染进程（renderer process）。
	2. 每个界面本质上就是一个网页，渲染进程将网页代码在 Chromium 中渲染成网页显示出来。
	3. Electron 实现了各平台的特殊功能（比如菜单，Dock），并为这些网页界面提供原生功能的调用接口，使得应用可以实现原生应用才能做的很多功能，并可以使用 Node.js 的全部模块（Module）。

如果你需要实现一些 Electron 或 Node.js 不支持的功能，可以自己用 C++ 写 Module 来实现。

由于 Electron  内建了特定版本的 Chromium，所以优势是网页设计时不用考虑兼容性（谢天谢地），劣势是会导致 Electron 什么也不做的情况下，应用体积也在 100 MB 左右，打包压缩后大约 30-50 MB。Electron 也继承了 Chromium 的特点，启动慢，利用资源（内存占用）换性能（流畅度）。

[NW.js](http://nwjs.io) 也是类似的框架，他采用了 Node.js + Webkit 组合。两者各有优劣[NW.js 跟 Electron 的完整功能对比](http://tangiblejs.com/posts/nw-js-electron-compared)。国内钉钉客户端是基于 NW.js 做的。网易自己造了两个轮子貌似已经停更的 [Hex](http://hex.youdao.com/zh-cn/index.html) 和 [NEJ](http://nej.netease.com/)，网易云音乐客户端是基于 NEJ 的。

Electron 类的网页封装成客户端另一个问题是源代码很难被保护。由于 JavaScript 是解释型语言，无法通过编译来保护代码，自身也没有很好的代码混淆方式，所以并不适用于需要版权保护或者纯靠客户端功能收费的应用。Electron 上曾有 issus 讨论源代码保护的话题，但官方的态度是 wontfix 。如果需要写一些需要保密的代码，可以考虑用 C++ 写 Node module 来解决。


结语、Learn once, write everywhere

这几天查资料时而感觉 JavaScript 威力无穷，时而又觉得它在哪个平台都是点到为止，像玩具和试验，距离工程性还有距离。JavaScript 有种鸠摩智用吐蕃内功练少林七十二绝学的意味。

或许照这个发展势头，以后世上只有两种工程师， JavaScript 工程师和其他工程师……

这几天调研有些仓促，如果写的不对的地方也请斧正。
