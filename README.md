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

# 学习经历

* 2015.6~2016.1 自学 javaweb 基础
* 2016.1~2016.2 自学前端html css js
* 2016.3~2016.5 bar 1.0
* 2016.5~2016.6 bar 2.0
* 2016.6-2016.7 es6 MDN html5 css3
* 2016.7~2016.10 music
* 2016.11~2017.3 重构music
* 2016.10~今天 linux
* 2017.1~2017.2 深入java: jvm/jdk源码(集合、并发)
* 2017.2~2017.3 leetcode
* 2017.3~今天 node
* 2017.4~2017.5 nodeclue-koa
* 2017.6~今天 spider-trending

# 自我评价

* 定位: 主攻node、其他方面可以打打辅助 node node node只想做node，当然别的方面可以打打辅助
* 态度: Talk is cheep, show me the code
* 学习策略: 官方文档/书籍 => 技术博客 => google ==> bing(梯子不好用的时候)
* 优势: 学习能力强、自制力强、性格友善、爱钻研原理、轻度代码洁癖
* 劣势: 非科班出身
  * 读书 [书单]()
  * leetcode刷题 [项目地址](https://github.com/xiedacon/leetcode)

# 开源项目

* [spider-trending](https://github.com/xiedacon/spider-trending)

  专门用于爬取 github trending 的爬虫，数据分析部分尚未完成

  * 做完nodeclub-koa后，对做web应用有些厌倦，闲了一段时间，想起以前一直想做的爬虫项目，燃起了对爬虫的兴趣，就有了这个项目，至于为什么目标是github trending而不是像别的爬虫爬妹子图啥的，因为个人觉得，爬虫其本身的技术是很简单的，无非是获取解析html页面，有趣的是爬虫爬到数据之后的分析与总结，github trending的数据有这个特性，比如说把项目根据一年star数之和排序，哪一月／周／天的star数最多／最少（程序员的开源热点时间..），一个项目的star趋势怎样，是突然增加然后消失不见，还是保持稳定的增长曲线..
  * 爬虫根据功能分为控制器、下载器、解析器、储存器分别对应项目根目录的spider.js+cron、downloader、parser、store，目前只完成了从html到json部分，还没有做数据分析，因为数据量不够
  * 目前的难点在于执行周期的控制，普适的解决方案有：timer(setTimeout)、调用linux协程、redis键空间通知、mq等、还有一些混合方案，相关的库有node-schedule、node-cron，略微看了一下它们的源码，主要以js的timer为主，个人觉得，js做这种事情不大靠谱，主要是万一node挂了怎么办，所以用的redis键空间通知的方案，这样除非node挂的时候正好有一个键到期，周期控制还是比较准确的，退一步讲，就算这种情况发生，还可以通过执行日志等弥补，而且还能加深对redis的了解，何乐而不为呢

* [nodeclub-koa](https://github.com/xiedacon/nodeclub-koa)

  nodeclue-koa 是 nodeclue 的 koa 版本，采用 es6 语法重写，功能与 nodeclub 社区基本相同，详情请看项目 [README](https://github.com/xiedacon/nodeclub-koa/blob/master/README.md)

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
