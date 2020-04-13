## 谢达 / Xie Da

* 男 / 1995 / 本科 / 华中农业大学

## 个人信息

* 手机：15271883834
* 微信：xiedacon
* Email：xiedacon@qq.com
* GitHub：[https://github.com/xiedacon](https://github.com/xiedacon)
* Blog：[http://www.xiedacon.com](http://www.xiedacon.com)
* 期望职位：Node.js 程序员

## 在校学习经历

### Java

* 2015.6~2016.1：自学 javaweb 基础
* 2016.3~2016.5：bar 1.0 项目
* 2016.5~2016.6：bar 2.0 项目
* 2016.7~2016.10：music 项目
* 2017.1~2017.2：深入 Java ( 深入理解 Java 虚拟机、jdk 集合、并发包源码 )

### Node.js / 前端

* 2016.1~2016.2：自学前端 ( HTML、CSS、JS )
* 2016.6-2016.7：基于 MDN 重构前端知识
* 2017.3~今：自学 Node.js ( 官网 api、深入浅出 Node.js、... )
* 2017.4~2017.5：nodeclub-koa 项目

### 其他

* 2016.10~今：学习 Linux
* 2017.2~2017.3：[LeetCode 刷题](https://github.com/xiedacon/leetcode)
* 2018.1~2018.3：阅读 GitHub 开源项目 ( 143 个 )

## 实习经历

### 大卖科技 ( 2017 年 9 月 ~ 2018 年 1 月 )

#### 买家秀项目

* 项目概况：基于 Node.js 的电商项目，总用户量 10w+，日活约 3w，并发连接峰值约 2w。当系统请求量较大时，通过业务节点负载均衡，实现快速扩容，提高请求处理能力。通过 MySQL 读写分离提高数据库读取性能
* [运行地址](http://www.maijiaxiuwang.com/visitor/index)
* 运行环境：Node.js 6.2 ( 2018 年 3 月份左右升级为 Node.js 8 LST )
* 基础技术栈：nginx + koa1 + Redis + co ( yield ) + knex
* 测试技术栈：ava + rewire
* 主要工作内容
  * 优化匹配接口：系统后端压力主要集中于整点的匹配接口，在成交量达到 8k 单 / 天时，原有的匹配接口达到瓶颈。通过优化核心匹配代码，node-cron 库定时预匹配，减少匹配接口处理时间。再加入 Redis 作为缓存层，缓解整点数据库压力。优化后，系统成交量最高达到 3w 单 / 天，预计瓶颈为 4 ~ 5w 单 / 天
  * 优化数据记录导出：通过将导出文件修改为 csv 格式并使用 stream 模式处理，使导出文件大小减少 60 ~ 70%，时间减少 50% 左右，并且可以通过参数决定导出类型
  * 开发模板工具类库：原有模板工具类库 [handlebars-helpers](https://github.com/helpers/handlebars-helpers) 使用繁琐、扩展性差。开发了 [hbs-helpers](https://github.com/xiedacon/hbs-helpers)，使 helper 可以在块级和行级中混合使用，减少了模板文件的代码量，并且易于根据技术需求和业务逻辑进行自定义

## 开源项目

* [hbs-helpers](https://github.com/xiedacon/hbs-helpers)：用于 Handlebars 模板引擎的 helper 集，helper 可以在块级或行级混合使用，且易于自定义
* [coding_robot](https://github.com/xiedacon/coding_robot)：钉钉的 Coding 机器人，用于将 Coding 的各种动态同步到钉钉，支持自定义消息模板、多机器人配置
  * 测试技术栈：ava + rewire ( 测试覆盖率 98% )
* [generate](https://github.com/xiedacon/generate)：项目生成手脚架，支持自定义项目模板、插件系统 ( 例如：项目初始化时 git init、npm install 等命令 )
* [small-server](https://github.com/xiedacon/small-server)：简易静态服务器实现，支持 gzip 压缩、断点续传功能
* [nodeclub-koa](https://github.com/xiedacon/nodeclub-koa)：使用 koa2 重写的 [nodeclub](https://github.com/cnodejs/nodeclub)
  * 基础技术栈：koa2 + mongoose ( MongoDB ) + Redis + async / await
  * 测试技术栈：mocha + power-assert ( 测试覆盖率 82% )
* [music](https://github.com/xiedacon/music)：一个前端页面仿网易云音乐的音乐类网站，初次使用 git 版本管理、ci 集成，后期改为 SPA 项目
* bar：一个前端页面仿百度贴吧的论坛类网站，在 2.0 版本中，初次尝试前后端分离

## 技能清单

* 熟悉 Node.js / Java
* 熟悉 Linux 基本使用，并使用 Linux 作为主力操作系统
* 熟悉 MySQL / MongoDB / Redis 相关类库的使用
* 熟悉前端基本技能 ( HTML / CSS / JS )
* 熟练使用 Git
* 了解持续集成、单元测试、Docker

## 致谢

感谢您花时间阅读我的简历，期待能有机会和您共事
