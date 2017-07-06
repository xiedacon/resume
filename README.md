# 个人信息

* 谢达/男/1995
* 本科/华中农业大学/动物医学
* Github: [https://github.com/xiedacon](https://github.com/xiedacon)
* 期望职位: NodeJS初级程序员
* 到岗时间: 7月15号后

# 联系方式

* 手机: 15271883834
* QQ: 1063462598
* Email: xiedacon@qq.com

# 自我评价

* 定位: 主攻node、其他方面可以打打辅助 node node node只想做node，当然别的方面可以打打辅助
* 态度: Talk is cheep, show me the code
* 学习策略: 官方文档/书籍 => 技术博客 => google ==> bing(梯子不好用的时候)
* 优势: 学习能力强、自制力强、性格友善、爱钻研原理、轻度代码洁癖
* 劣势: 非科班出身
  * 读书 [书单]()
  * leetcode刷题 [项目地址](https://github.com/xiedacon/leetcode)

# 学习经历

* 2015.6~2016.1 自学 javaweb 基础
* 2016.1~2016.2 自学前端 ( html、css、js )
* 2016.3~2016.5 bar 1.0 项目
* 2016.5~2016.6 bar 2.0 项目
* 2016.6-2016.7 重构前端知识 ( 从 MDN 学习 es6、html5、css3 )
* 2016.7~2016.10 music 项目
* 2016.10~今天 学习 linux
* 2017.1~2017.2 深入 java: jvm ( 深入理解Java虚拟机 ) / jdk源码 ( 集合、并发 )
* 2017.2~2017.3 leetcode 刷题
* 2017.3~今天 自学 node ( 深入浅出Node.js、官网api、... )
* 2017.4~2017.5 nodeclue-koa 项目
* 2017.6~今天 spider-trending 项目

# 开源项目

### [spider-trending](https://github.com/xiedacon/spider-trending)

  专门用于爬取 github trending 的爬虫，数据分析部分尚未完成

  * 起源: 做完 nodeclub-koa 后，对做 web 应用有些厌倦，闲了一段时间，想起以前一直想做的爬虫项目，就有了这个项目
  * 技术栈: 使用 superagent 请求页面、cheerio 处理页面、redis 键空间通知做周期控制
  * 困难: 目前项目的难点在于周期控制，其普适的解决方案可分为两种: 仅使用js ( node 的 timer ) 和配合第三方软件 ( linux 的 cron、使用 redis 的键空间通知、mq 等 )。个人觉得，以 js 为核心做周期控制不大靠谱，因为不清楚 node 进程什么时候会挂掉，在加上对于 redis 的操作比较熟悉，因此，项目采用的redis键空间通知做周期控制。这种方案发生错误的可能性较小，除非 node 进程挂掉并重启的同时，正好有一个键到期，这时可以采用执行日志等进行补救
  * 总结: 项目根据传统爬虫功能划分为: 控制器 ( spider.js + cron ) 、下载器 ( downloader ) 、解析器 ( parser ) 、储存器 ( store ) 。关于爬虫目标为什么是github trending，而不是像别的爬虫爬妹子图什么的。因为，个人觉得，爬虫本身的技术的是简单的，无非是获取解析 html 页面，其难点在于，爬到数据之后的处理分析。相对而言 github trending 的数据是可分析的，例如: 统计某个项目一年的 star 数，哪一月 / 周 / 天的 star 数最多 / 最少，趋势如何，是突然上升而后消失不见还是趋于稳定等等，以后还可加上数据可视化等知识点

* [nodeclub-koa](https://github.com/xiedacon/nodeclub-koa)

  nodeclue-koa 是 nodeclue 的 koa 版本，采用 es6 语法重写，功能与 nodeclub 社区基本相同

  * 起源: 从 java 转到 node 后，手头一直没有一个看得过去的 node 项目，所以就用新语法与中间件重写了 nodeclue，整个过程相当于看源码
  * 技术栈: 使用 es6 语法、koa 框架、redis 缓存、mongoDB 数据库、async / await + promise ( bluebird ) 作为异步流程控制
  * 困难: 这个项目的难点在于对异步的理解，async / await 是什么？promise 是什么？callback 又是什么？async / await 本质上是一个 promise 处理器的语法糖，负责当前一个await的promise resolve之后，继续执行代码直到await到pedding状态的promise或函数执行完毕为止，期间发生异常则直接抛出，以try-catch的形式处理，而不是 promise.catch()。promise则是一种组织异步代码的形式，保证promise链上的函数依次执行，相对于callback来说，promise是以一种由内向外的思维组织异步代码，callback这是以由外向内的思维组织异步代码。callback的话，得先从io调用说起，最初的计算机需要io调用时，都是让cpu等待io读取完毕后再继续执行，后来人们认为这种方式太浪费cpu性能，当某个进程发起io调用时会长期占用cpu时间，就改为了，需要io调用，则会建立一个回调，cpu继续执行，当io调用完毕后，再通知cpu执行回调，继续上一次的运算，这样cpu就能在io调用的时间做其他运算，提高计算性能。类似的，进程之于硬件(cpu io)，相当于线程之于进程，将进程也看做一种资源，当某个线程发起io调用，此时，就有两种解决方案，一种是像之前那样，线程等待直到io调用完毕，这时进程需要在io调用完毕后
  * 总结

  * 从java转到node后，第一个还看得过去的项目，做这个项目的过程，几乎相当于看源码的过程，模块机制，异步流程控制(callback promise async/await)，koa中间件思想，开发环境／生产环境，mongoose，mongodb，redis（以前经常接触，第一次使用到项目中）
  * 整个项目使用es6语法，async/await+promise(bluebird)异步流程控制，并不是完全依赖async/await，只是将async/await作为简单的Promise().then().then()使用，将ejs模板引擎改为art-template，因为并不喜欢ejs的语法
  * promise控制，编写koa中间件，git版本管理，ci集成，mocha测试初步实践
  * 

* [music](https://github.com/xiedacon/music)

  仿网易云音乐
    * 继bar项目之后，觉得自己前端部分学得太差，特别是js部分，于是学习了大概２个月的es6(ECMAScript 2015)，使用html5+css3+es6的新特性，不在乎兼容性问题，做的一个音乐类网站
    * 开发时使用前后端分离的开发模式，前端位于nginx服务器，后端位于tomcat服务器，先写前端页面，弄一些原始数据，将前端页面跑起来后，写后端接口，并一步步将原始数据替换为后端接口，具有音乐网站基本功能，用户，歌曲，歌手，专辑，歌单，榜单，专辑分类，歌手分类CRUD，后台以excel格式批量上传／下载数据，github第三方登录
    * chrome的安全策略，不能加载本地js文件，所以起了一个nginx做静态服务器
    * 巩固CRUD? 了解Oauth 2.0，git,ci初步实践，
    * 改为SPA应用，自己写的前端路由，思路很简单，等待html/css/js加载完毕后，再渲染展示页面，监听hash，前端路由资源位于主页面，将dom操作包装为一个小工具，类似jquery，并尝试在项目中替代jquery

* bar

  仿百度贴吧。有两个版本: 
  * jsp+ssh: 基础版本，
    * 刚学完javaweb基础，想做一个专属于自己的javaweb项目，由于那时候贴吧逛得比较多，就有了该项目
    * 集成了ueditor,jsp+ssh，具有贴吧基本功能: 创建修改删除账号，删发贴，删发评论，后台管理，帖子评论记录，禁言用户等
    * 
    * 第一次独立动手做项目，从前端页面到后端数据库
  * html+jquery+ssh: 初次前后端分离实践。前端使用jquery请求处理数据，生成dom。后端接口服务化
    * 接触了许多前后端分离相关的思想，决定将项目前后端分离，前端处理和生成页面，后端只提供接口(从此以后再也没有写过jsp页面)
    * 后端功能与基础版本相同，前端使用jquery请求处理数据，生成页面
    * 这段时间主要是熟悉 jquery api
    * 第一次尝试前后端分离

star原则
  * s 场景 
  * task 任务
  * active 行动
  * result 结果

* 为什么有这个项目
* 这个项目能做什么
* 做项目时遇到了什么
* 从这个项目得到了什么

成就　==> 案例 ==> 心得

将面试官带入自己的角色

# 技能清单

* 熟悉 ``node/java``
* 熟悉 ``linux`` 基本使用，曾使用 ``Raspberry Pi`` 搭建 ``web`` 服务器
* 熟悉 ``mysql/mongodb/redis`` 基本使用
* 熟悉 ``html/css/js``
* 熟悉 ``koa`` 基本使用与中间件编写
* 熟练使用 ``git`` 作为版本控制
* 了解持续集成、单元测试
* 了解 ``async/await/promise/callback`` 之间的关系 - 可变心得
