# 个人信息

* 谢达 / 男 / 1995
* 本科 / 华中农业大学 / 动物医学
* Github: [https://github.com/xiedacon](https://github.com/xiedacon)
* Blog: [https://github.com/xiedacon/blog/issues](https://github.com/xiedacon/blog/issues)
* 期望职位: Node.js 初级程序员
* 到岗时间: 随时

# 联系方式

* 手机: 15271883834
* QQ: 1063462598
* Email: xiedacon@qq.com

# 自我评价

* 定位: 主攻 Node.js、其他方面可以打打辅助
* 态度: Talk is cheep, show me the code
* 学习策略: 官方文档/书籍 => 技术博客 => google => bing
* 优势: 学习能力强、自制力强、严以律己宽以待人、爱钻研原理、轻度代码洁癖
* 劣势: 非科班出身
  * 读书 - [书单](https://github.com/xiedacon/notes/blob/master/books.md)
  * leetcode 刷题 - [项目地址](https://github.com/xiedacon/leetcode)

# 学习经历

* 2015.6~2016.1 自学 javaweb 基础
* 2016.1~2016.2 自学前端 ( HTML、CSS、JS )
* 2016.3~2016.5 bar 1.0 项目
* 2016.5~2016.6 bar 2.0 项目
* 2016.6-2016.7 重构前端知识 ( 从 MDN 学习 ECMAScript6、HTML5、CSS3 )
* 2016.7~2016.10 music 项目
* 2016.10~今 学习 linux
* 2017.1~2017.2 深入 java: jvm ( 深入理解Java虚拟机 ) / jdk源码 ( 集合、并发 )
* 2017.2~2017.3 leetcode 刷题
* 2017.3~今 自学 node ( 深入浅出 Node.js、官网 api、... )
* 2017.4~2017.5 nodeclub-koa 项目
* 2017.6~今 spider-trending 项目

# 开源项目

### [spider-trending](https://github.com/xiedacon/spider-trending)

  专门用于爬取 github trending 的爬虫，数据分析部分尚未完成

  * 起源: 做完 nodeclub-koa 后，对做 web 应用有些厌倦，闲了一段时间，想起以前一直想做的爬虫项目，就有了这个项目
  * 技术栈: 使用 superagent 请求页面、cheerio 处理页面、redis 键空间通知做周期控制
  * 困难: 目前项目的难点在于周期控制，其普适的解决方案可分为两种: 仅使用 js ( node 的 timer ) 和配合第三方软件 ( linux 的 cron、使用 redis 的键空间通知、mq 等 )。个人觉得，以 js 为核心做周期控制不大靠谱，因为不清楚 node 进程什么时候会挂掉，在加上对于 redis 的操作比较熟悉，因此，项目采用的 redis 键空间通知做周期控制。这种方案发生错误的可能性较小，除非 node 进程挂掉并重启的同时，正好有一个键到期，这时可以采用执行日志等进行补救
  * 总结: 项目根据传统爬虫功能划分为: 控制器 ( spider.js + cron ) 、下载器 ( downloader ) 、解析器 ( parser ) 、储存器 ( store ) 。关于爬虫目标为什么是 github trending，而不是像别的爬虫爬妹子图什么的。因为，个人觉得，爬虫本身的技术的是简单的，无非是获取解析 html 页面，其难点在于，爬到数据之后的处理分析。相对而言 github trending 的数据是可分析的，例如: 统计某个项目一年的 star 数，哪一月 / 周 / 天的 star 数最多 / 最少，趋势如何，是突然上升而后消失不见还是趋于稳定等等，以后还可加上数据可视化等知识点

### [nodeclub-koa](https://github.com/xiedacon/nodeclub-koa)

  nodeclub-koa 是 nodeclub 的 koa 版本，采用 es6 语法重写，功能与 nodeclub 社区基本相同

  * 起源: 从 java 转到 node 后，手头一直没有一个看得过去的 node 项目，所以就用新语法与中间件重写了 nodeclub，整个过程相当于看源码
  * 技术栈: 使用 es6 语法、koa 框架、redis 缓存、mongoDB 数据库、async / await + promise ( bluebird ) 作为异步流程控制
  * 困难: 这个项目的难点在于对异步的理解，async / await 是什么？promise 又是什么？async / await 本质上是一个 promise 处理器的语法糖，负责前一个 await 的 promise 解决之后，继续执行代码直到 await 到下一个 promise 或函数执行完毕为止，期间如果发生异常则直接抛出，以 try-catch 的形式处理，而不是 promise.catch()。promise 是一种组织异步代码的形式，保证 promise 链上的函数依次执行，相对于 callback 来说，promise 是用由内向外的思维组织异步代码，需要控制异步时，将 promise 从底层函数返回到顶层函数，callback 则是用由外向内的思维组织异步代码，需要控制异步时，将 callback 从顶层函数传递到底层函数
  * 总结: 在做这个项目的过程中，学会了 promise 异步流程控制，练习使用 git 版本管理、ci 集成、mocha 测试

### [music](https://github.com/xiedacon/music)

  一个前端页面仿网易云音乐的音乐类网站

  * 起源: 做完 bar 项目后，觉得自己前端部分学得太差，特别是 js 部分。于是通过 MDN 重构前端知识后，做的一个音乐类网站
  * 技术栈: 前端 jquery、后端 springmvc + spring + mybaits、mysql 数据库、Oauth 2.0、POI 导入 / 出 excel 表格
  * 总结: 初次在项目中尝试使用前后端分离开发，前后端位于不同服务器，前端 nginx、后端 tomcat，并练习使用 git 版本管理、ci 集成

### bar

  一个前端页面仿百度贴吧的论坛类网站，有两个版本:

  * 基础版本
    * 起源: 刚学完 javaweb 基础，想做一个专属于自己的 javaweb 项目，由于那时候贴吧逛得比较多，就有了该项目
    * 技术栈: jsp + struts2 + spring + hibernate、mysql 数据库、ueditor 富文本编辑器
    * 总结: 第一次独立动手做项目，从前端页面到后端数据库
  * 前后端分离版本
    * 起源: 接触了许多前后端分离相关的思想，决定将项目前后端分离，前端处理和生成页面，后端只提供接口
    * 技术栈: jquery + struts2 + spring + hibernate、mysql 数据库、ueditor 富文本编辑器
    * 总结: 初次在项目中尝试前后端分离

# 技能清单

* 熟悉 ``Node.js`` / ``Java``
* 熟悉 ``linux`` 基本使用，将 ``linux`` 作为主力操作系统
* 熟悉 ``mysql`` / ``mongodb`` / ``redis`` 基本使用
* 熟悉 ``HTML`` / ``CSS`` / ``JS``
* 熟悉 ``koa`` 基本使用与中间件编写
* 熟练使用 ``async / await`` + ``promise`` 异步流程控制
* 熟练使用 ``git`` 作为版本控制
* 了解持续集成、单元测试
