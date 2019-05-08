### 前言
Nodejs开发多了的时候，就会发现有好多常用的软件包值得推荐出来，如果你也有好的软件包，在后台使用，欢迎提PR。该文章同步在我的[github](https://github.com/linxiaowu66/nodejs-useful-packages)上。我将这些包按照功能简单分类一下，如果你觉得分类不合理，也欢迎一起讨论。

### 1、日志

* [pino](https://github.com/pinojs/pino): 性能极好的nodejs日志器。它还包括一个shell界面以更好地打印它的日志文件
* [winston](https://github.com/winstonjs/winston): 一款多传送异步日志库。Winston被设计成一款简单并且通用的日志库以支持多重传送。传送指的是你日志存储的设备。一个winston日志器的实例可以配置成多个日志等级使用不同的传送。比如你的错误日志可能需要存储到远程存储器(比如数据库)，但是其他的日志等级都保存到本地文件或者直接输出到控制台
* [winston-daily-rotate-file](https://github.com/winstonjs/winston-daily-rotate-file): 配合winston使用，能够每天记录日志到循环的文件中去。
* [sentry](https://github.com/getsentry/sentry): Sentry 是一个实时的事件日志和聚合平台，基于 Django 构建。Sentry 可以帮助你将各种主流语言的所有 exception 自动记录下来，然后在一个好用的 UI 上呈现和搜索。处理 exception 是每个程序的必要部分，所以 Sentry 也几乎可以说是所有项目的必备组件。

### 2、基础包

* [lodash](https://github.com/lodash/lodash): 一款JS库，封装了很多有用的JS API
* [ramda](https://github.com/ramda/ramda): lodash的替代库，函数式编程实践的极佳工具库
* [co](https://github.com/tj/co): 是一个能够接受一个generator，并且自动执行generator内部的逻辑的软件库。
* [moment](https://github.com/moment/moment): 一个重量级的JS日期库，用于分析、校验、操作和格式化日期
* [date-fns](https://github.com/date-fns/date-fns): moment替代的绝佳工具库，体积比moment较少了将近4倍，如果功能用的更少的话，可以试试dayjs(6.6K)
* [chokidar](https://github.com/paulmillr/chokidar): 一款软件包优雅地封装了Nodejs的`fs.watch` / `fs.watchFile` / `fsevents`方法
* [bluebird](https://github.com/petkaantonov/bluebird): bluebird是一个功能齐全的promise库, 它专注于创新的特性和性能
* [through2](https://github.com/rvagg/through2): 一款对Node streams.Transform (Streams2)封装的软件包，方便创建transform流。
* [split2](https://github.com/mcollina/split2): 可以打断stream然后重组，这样每一行都是一个chunk。
* [readable-stream](https://github.com/nodejs/readable-stream): 该包是NodeCore的Stream2和Stream3的镜像包实现。背景知识：[Why I don't use Node's core 'stream' module](https://r.va.gg/2014/06/why-i-dont-use-nodes-core-stream-module.html)
* [path-to-regexp](https://github.com/pillarjs/path-to-regexp): 该工具可以将诸如`/user/:name`的路径字符串转换为正则表达式
* [request-ip](https://github.com/pbojinov/request-ip): 该nodejs包可以获取nodejs服务器中一条请求的IP地址


### 3、Express

* [express-session](https://github.com/expressjs/session): Express下session中间件
* [multer](https://github.com/expressjs/multer): Multer 是一个 node.js 中间件，用于处理 multipart/form-data 类型的表单数据, 它主要用于上传文件. 它是写在 busboy 之上非常高效。**注意: Multer 不会处理任何非 multipart/form-data 类型的表单数据.**
* [morgan](https://github.com/expressjs/morgan): Nodejs下HTTP请求日志中间件
* [csurf](https://github.com/expressjs/csurf): Nodejs下CSRF保护中间件
* [connect-flash](https://github.com/jaredhanson/connect-flash): flash 是 session 中一个用于存储信息的特殊区域。消息写入到 flash 中，在跳转目标页中显示该消息。flash 是配置 redirect 一同使用的，以确保消息在目标页面中可用。参考[connect-flash 用法详解](http://yunkus.com/connect-flash-usage/)
* [cookie-parser](https://github.com/expressjs/cookie-parser): cookie分析中间件
* [serve-favicon](https://github.com/expressjs/serve-favicon): favicon显示中间件
* [Helmet](https://github.com/helmetjs/helmet): Helmet可以通过设置各种头部来让你的Express服务器更加安全，抵御大部分的攻击。
* [cors](https://github.com/expressjs/cors): express的CORS中间件
* [express-rate-limit](https://github.com/nfriedly/express-rate-limit): Express基本的限速中间件。**注意这个中间件默认不能和别的进程/服务器共享状态，如果需要更加健壮的解决方案，推荐添加[Redis Store](https://github.com/nfriedly/express-rate-limit/blob/HEAD/%5BRedis%5D(http:/redis.io/)-backed%20store,%20more%20suitable%20for%20large%20or%20demanding%20deployments.)。或者使用[strict-rate-limiter](https://www.npmjs.com/package/strict-rate-limiter),[express-brute](https://www.npmjs.com/package/express-brute),[rate-limiter](https://www.npmjs.com/package/express-limiter)**

### 4、Koa
* [koa-bodyparser](https://github.com/koajs/bodyparser): Koa的报文body分析中间件，支持`json`、`form `、`text`类型的Body
* [koa-cors](https://github.com/koajs/cors): koa的CORS中间件
* [koa-generic-session](https://github.com/koajs/generic-session): Koa通用的session中间件
* [koa-multer](https://github.com/koa-modules/multer): Koa处理 multipart/form-data 类型的表单数据的中间件
* [koa-router](https://github.com/alexmingoia/koa-router): Koa的路由中间件
* [koa-static](https://github.com/koajs/static): Koa静态文件传输中间件

### 5、存储
* [ioredis](https://github.com/luin/ioredis): 一款功能齐全性能优越的redis客户端
* [mongoose](https://github.com/Automattic/mongoose): Mongoose是一款[MongoDB](https://www.mongodb.org/)对象模型工具，被设计成运行在一个异步的环境下。
* [connect-redis](https://github.com/tj/connect-redis): 这是一款Redis的session存储器。
* [Sequelize](https://github.com/sequelize/sequelize): Sequelize是一个基于promise的关系型数据库ORM框架，这个库完全采用JavaScript开发并且能够用在Node.JS环境中，易于使用，支持`Postgres`, `MySQL`, `SQLite` 和 `Microsoft SQL Server`数据库(感谢[CW木子](https://juejin.im/user/57a358dc8ac247005f16735b)提供)
* [lru-cache](https://github.com/isaacs/node-lru-cache): 一款可以快速删除最近使用过的条目的cache工具包(LRU Cache是一个Cache置换算法，含义是“最近最少使用”，当Cache满（没有空闲的cache块）时，把满足“最近最少使用”的数据从Cache中置换出去，并且保证Cache中第一个数据是最近刚刚访问的。由“局部性原理”，这样的数据更有可能被接下来的程序访问)。
* [levelup](https://github.com/level/levelup): 这是一款简单的key-value存储器。由Google开发。
* [node-cache](https://github.com/ptarjan/node-cache/): 内存缓存数据的工具库，适合单台机器部署的数据共享

### 6、辅助
* [Chance](https://github.com/chancejs/chancejs): Javascript的随机生成器辅助工具
* [js-to-java](https://github.com/node-modules/js-to-java): 提供一种简单地方式去包裹JS对象为java对象。在[hessian.js](https://github.com/node-modules/hessian.js)我们需要使用js对象来写java的类名，所以我们就使用这个库来自动编码，将js的对象转为java的对象。
* [xml2js](https://github.com/Leonidas-from-XIV/node-xml2js): 一款可以将XML文件转为JS对象的转换器
* [colors](https://github.com/Marak/colors.js): 让打印的字体颜色更加丰富多彩
* [joi](https://github.com/hapijs/joi): 对象语法描述语言以及对象校验，可以用于定义nodejs的路由传参的对象内部成员的类型并做校验
* [serialize-javascript](https://github.com/yahoo/serialize-javascript): 序列化JS为JSON的超子集，包含正则表达式以及函数都会被JSON掉。
* [js-yaml](https://github.com/nodeca/js-yaml): YAML文件的解析器。
* [uuid](https://github.com/kelektiv/node-uuid): 可以快速生成符合[RFC4122](http://www.ietf.org/rfc/rfc4122.txt)标准的UUID库。常用于追溯nodejs下的请求。
* [session-file-store](https://github.com/valery-barysok/session-file-store): 能够存储session到指定文件中，可以用在Express和Koa中
* [node-fs-extra](https://github.com/jprichardson/node-fs-extra): `fs-extra`添加了原生`fs`模块中没有的文件系统方法，包括`mkdirp`， `rimraf`， 和`ncp`等
* [node-glob](https://github.com/isaacs/node-glob): node的glob模块允许你使用*等符号, 来写一个glob规则,像在shell里一样,获取匹配对应规则的文件,这个glob工具基于javascript.它使用了 minimatch 库来进行匹配
* [reflect-metadata](https://github.com/rbuckton/reflect-metadata): 可以使用反射和修饰器的方式为你的类和方法注入元数据，并操作元数据。
* [inversify](https://github.com/inversify/InversifyJS): 一款轻量级的但是强大的控制反转容器，用于JS或者Nodejs，使用TS写的哦！
* [concurrently](https://github.com/kimmobrunfeldt/concurrently): 一款可以让你同时运行多个命令的工具包
* [cpx](https://github.com/mysticatea/cpx): 一款可以使用通配符复制文件并且能够监控文件改动的工具包
* [Husky](https://github.com/typicode/husky): ghooks的升级版，可以为你的git添加各种钩子。
* [minimist](https://github.com/substack/minimist/): 该工具包用来解析命令行参数，比如会把下面的命令解析成如下样子：
```
$ node example/parse.js -x 3 -y 4 -n5 -abc --beep=boop foo bar baz
{ _: [ 'foo', 'bar', 'baz' ],
  x: 3,
  y: 4,
  n: 5,
  a: true,
  b: true,
  c: true,
  beep: 'boop' }
```
* [yeast](https://github.com/unshiftio/yeast): 该工具包用来生成一个唯一的ID，与uuid不大一样。socket.io使用它来将时间戳生成唯一的字符串。
* [rc](https://github.com/dominictarr/rc): 该工具包可以为你的项目加载对应的配置，如果按照他们的规则来的话。查找比如eslintrc这种类似的文件
* [rimraf](https://github.com/isaacs/rimraf): nodejs下执行命令`rm -rf`的工具库
* [nodemailer](https://github.com/nodemailer/nodemailer): nodejs下发邮件客户端
* [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken): nodejs下JsonWebToken实现的工具库

### 7、HTTP客户端
* [axios](https://github.com/mzabriskie/axios)：一款基于Promise API 的HTTP客户端
* [request](https://github.com/request/request): 一款简化版的HTTP客户端(作者已经弃用)
* [r2](https://github.com/mikeal/r2): request作者打造的另外一个轻量级，Es6语法的HTTP客户端（66KB）
* [request-promise](https://github.com/request/request-promise): 一款基于Bluebird的Promise API的HTTP客户端，对`request`的再封装。
