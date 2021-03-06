### <center>滴滴SP提前批Java123面
***
## 前言

前阵子还是在牛客网上发布的SP专场，看到里面有很多岗位，然后抱着试一试的态度投递了几个，没想到竟然能够被滴滴捞起来，给了一次面试的机会。不得不说，滴滴的效率也是非常高的，一下午的时候，就把三轮技术面都完成了，从下午的两点半，面到下午五点半~ 面完感觉身体被掏空...

面试中项目部分问题是围绕我的开源项目 [蘑菇博客](https://gitee.com/moxi159753/mogu_blog_v2) 展开的，还有就是我为了面试突击准备的 [学习笔记](https://gitee.com/moxi159753/LearningNotes)（二面面试官好像感兴趣.. 直接打开我笔记来问....），欢迎感兴趣的小伙伴能够star支持一下~

## 第一面

一面主要考察的是一些基础的，面试时间大概30分钟

- 自我介绍
- 前端和后端项目你都做过，你未来的职业规划是什么?
- 现在你投的是研发工程师，有初级、中级、高级，你觉得你是等级的？
- 看你都是偏向于JavaWeb开发这块，有学习和了解过什么书籍来提升自己么？
- 你觉得微服务架构能解决高并发问题呢？能解决哪一类？
- 假设现在你是一个单体应用程序，然后能够支撑200的QPS，然后如果我想要能够支撑起400的QPS，那么你会怎么做？说说你的思路和解决方法
- 按照你这样说的，通过Nginx的负载均衡，搭建出一个集群就能够解决并发的问题，为什么还要用微服务？
- 你平时做微服务相关的项目，一般面临的问题是哪方面的？
- 如何能够快速的发现，某个服务出现问题，然后进行定位？（回答了一下链路追踪技术zipkin）
- 那谈谈zipkin链路追踪技术的内部原理吧？
- 有没有更简单的方法，去判断某个服务宕机了（通过eureka的面板，看服务的状态是up还是down）
- 还是刚刚的场景，A调用B，B调用C，然后你发现这个链有问题，你是怎么一个排查流程（从Chrome浏览器的F12，查看Network，然后看到每个接口的耗时，发现出有问题的接口）
- 我看你用的都是SpringCloud，Dubbo有用过么? 能简单介绍下？（滴滴内部好像都是基于dubbo来做的）
- 你觉得自己有哪些优点和优势？
- 平时有看过哪些书籍呢？你对哪本书总结的比较深入？
- 你平时常用到的集合框架有哪些？
- ArrayList和LinkedList的区别？
- 讲讲ArrayList的扩容机制？
- 树形结构遍历的话有哪些方法？
- MySQL的索引有哪些？
- 按照算法来进行划分的话，索引能够分为哪几种？
- 主键索引和普通索引底层使用的算法是哪个算法？
- SQL分析有用过么？谈谈explain的用法，如果确定一条SQL走了那些索引？
- 你做[开源博客](https://gitee.com/moxi159753/mogu_blog_v2)的时候，有写过项目文档么？谈谈一份项目文档应该包含什么？
- 项目分为前端和后端，比如你在写后端的时候，前端的小伙伴都在等你么？（并不是，因为我们通过提前约定好具体的接口文档，以及返回值，然后通过swagger-ui进行交互，同时前端还可以使用mock框架，模拟出一些假数据来进行开发）
- 反问环节，问面试表现和建议。

技术栈要广，同时也要某一方面比较精的，广可以慢慢来，精的话最好从一开始就确定。

##  第二面

二面老哥主要就是考察的算法，上来就是手撕代码，二面老哥非常赞，幽默，问的问题也很有引导性，交互性很强~，面试时间大概1小时

- 自我介绍
- 二面老哥好像对我码云感兴趣，叫我给他发一下[码云地址](https://gitee.com/moxi159753)
- 我先去看看你的码云，然后给你道题先做着吧！（求求你问我，我不想做题了...）

```bash
某个富翁招收保镖，为了提高吸引力，设置了一个特殊的工资，第一天保镖能获取1元报酬，随后两天能获得2元，在随后三天能够获得3元...以此类推，给定一个天数，得出能够获得的报酬

输入 3， 返回5   1+2+2 = 5
输入 10，返回30  1+2+2+3+3+3+4+4+4+4 = 30

# 首先用一层for循环解决，然后后面面试官说能不能推导出公式来
```

- 假设你现在从前端请求某个接口，然后从前台到后端经历了什么，说的越详细越好（从hosts，DNS，filter，前端控制器，Spring MVC，ORM（mybatis），到前后端分离以及服务器渲染讲了一下）
- 假设在刚刚你说的，如果没有filter这一层的时候，会出现什么问题呢？
- 谈谈servlet的生命周期？
- HandlerMapping在里面的作用是什么，如果没有HandlerMapping会有什么问题？假设没有HandlerMapping的话，你能够自己实现一个么，说说你的思路？
- 谈谈Spring里用到的设计模式？
- 看你[学习笔记](https://gitee.com/moxi159753/LearningNotes)里面提到了 JDK动态代理 和 CGLib动态代理，谈谈他们是什么，以及应用场景？
- 那再来一题吧~！二面老哥安慰到，是不是一面没做题，二面突然写这么多，有点慌？？（说实话，我很方..）

```bash
近期末，让小东头疼的考试又即将到来了，而且是小东最不喜欢的科目，遗憾的事，
小东得知d天后他必须参加此次考试，小东的父亲对他非常严格，要求他立即开始复习
功课。为照顾她的情绪，父亲要求她每天该科目的学习时间在iminTime到imaxTime之间
，并计划在考试前检查小东是否按要求做了。若未能完成，小东将会受到惩罚。

现在小东的父亲要求检查小东的备考情况。遗憾的事，由于专注于备考，小东只是记录
了自己备考的总时间sumTime，并没有记录每天复习所用的时间，也不知道准备情况是否
符合父亲的要求。他想知道是否能够制作一个满足需求的时间表以应付父亲的检查

输入：
输入中有多组测试数据。每组测试数据的第一行包含两个整数d和sumTime，1<=d<=30,
0<=sumTime<=240,分别表示小东复习的天数及每天用于复习的时间之和。紧随其后的d行
中，每行包括两个空格分隔的整数，为小东父亲要求小东在这一天用于复习时间的范围
iminTime和imaxTime
0<=iminTime<=imaxTime<=8.

输出：
对每组测试数据，若能够做出一个满足小东父亲要求的时间表，则在单独的一行中输出Yes
，并在随后的一行中给出每天复习花费的时间。否则输出No。若满足要求的时间表不唯一，
小东希望给父亲留下比较用功的映像，开始时每天复习的时间比较长

样例输入：
1 48
5 7
2 5
0 1
3 5

样例输出：
No
Yes
1 4
```

第一次见到这个题，看题目都看了10多分钟....，后面因为时间不太够，大概讲了一些思路，没有叫实现代码

- 聊聊状态码吧？1XX，2XX，3XX，4XX，5XX
- 如何制造出4XX 或者 5XX的错误呢 ？
- 常见的中间件你都用过什么？
- 谈谈为什么你会用到消息队列？
- RabbitMQ，而不是Kafka、ActiveMQ或者RocketMQ呢，谈谈每个消息队列的场景，以及你当初的消息中间件的选型依据。
- 消息队列的底层实现是什么？
- 谈谈你对阻塞队列的理解？
- 反问环节

二面老哥给人感觉很不错，全程很幽默，在面试上引导性也很强，聊的还不错，最后给我的建议就是希望能够把写博客这件事情坚持下去~

## 第三面

三面主要考察的是项目这块，和老哥聊的也还不错，面试时间大概1小时

- 自我介绍
- 能详细介绍一下你的开源项目么？为什么想到做这个事情？
- 能介绍一下项目都有哪些的功能么？
- 你最近做的项目是银行的一个项目，主要职责是前端开发，那会为什么选型用Vue，而不是其它比如React 或者AngularJS呢，说说你的想法，以及这三门前端主流开发框架的区别？
- 谈谈nginx在你项目中的应用？
- 为什么要用nginx做静态资源映射，为什么要做静态资源映射的事情呢？nginx不能直接作为静态资源服务器么？
- 后台有做权限控制么？能谈谈RBAC权限模型么？
- 除了RBAC权限模型以外，你还有了解过其它的权限框架么？
- 谈谈你对SpringSecurity的理解？
- 项目中的服务都是通过什么端口进行暴露的，这样会有什么问题么？
- 了解过服务网关么？说说zuul 或者 gateway？
- 服务和服务之间调用是通过什么？（讲了一下RestTemplate 到 Feign 以及 OpenFeign）
- 知道nginx的反向代理么？后台暴露的服务，有用到nginx做反向代理么？
- 谈谈服务发现组件？eureka 以及 nacos的区别？
- 谈谈JVM的内存结构？
- 为什么方法区是线程共有的？它里面是主要存放了哪些东西呢？
- 堆也是线程共有的，那么怎么解决线程占用的问题？
- 有用过ThreadLocal么？谈谈ThreadLocal以及它的使用场景？
- 接口的幂等性有听过么？说说你的项目中有没有遇到接口幂等性的问题，以及如何解决？
- 如何解决接口的重复提交的问题？（IP+接口名，存放redis中设置过期时间）
- 堆的内存结构是什么？
- 为什么年轻代要使用 8:1:1 来进行划分成eden区、Survivor0，Survivor1区，这么做的好处是什么？
- 什么样的对象可能会进入老年代？如果一个对象进入到老年代后会怎么样？
- 老年代什么时候会触发major GC？还有其它的比如 Minor GC、Full GC 它们的触发条件又是什么？
- 有听过CMS 和 G1垃圾收集器么？谈谈这两个垃圾收集器
- 说说G1的垃圾收集过程？
- 说说CMS的垃圾收集过程？CMS存在Stop-The-World么？在哪一个阶段会存在呢？
- CMS和G1的区别是什么，什么时候用CMS，什么时候用G1呢？
- HashMap线程安全么，什么操作是不安全的呢？
- 谈谈HashMap的扩容机制？
- HashMap的头插法听过么，为什么后面JDK1.8又变成了尾插法？
- 谈谈CurrentHashMap？
- 为什么原来用的是分段锁，后面JDK1.8以后又不用分段锁了？而是采用Synchronized + CAS呢
- HashMap底层结构是什么，什么时候会用到红黑树？
- 为什么红黑树的时间复杂度是O(logN)？谈谈AVL树和红黑树的区别？
- 你刚刚提到了二叉树的查找，你可以写代码么？来写一个二叉树的遍历吧

  - 用非递归的方式写了二叉树的先序遍历（后面本来打算自己写一些测试样例测试，面试官打住了...）

- 计算机网络结构里面的TCP/IP协议里面的分层模型，具体有哪几层？以及每一层的作用能说一下么？
- TCP里面的三次握手能够详细的介绍一下么？
- 为什么是三次握手，而不是两次握手呢，或者四次握手？
- 在讲讲四次挥手的流程？
- 为什么断开连接需要四次挥手呢？
- 为什么坚持写这个[开源项目](https://gitee.com/moxi159753/mogu_blog_v2)这么久？
- 反问环节，咨询了一下面试表现，以及需要提高的地方。

和三面老哥聊了会，技术面到这里结束了，后续是HR来进行面试的流程跟进

## 后言

滴滴的面试流程快到惊人，一下午就把技术面完了，说实话在第一面的时候，面试官下线后，我本来打算收拾电脑马上准备去实验室了，刚把电脑关机，然后回头HR电话就来了，说准备马上二面.. ，然后二面结束马上三面又来了。后面想着会不会HR面也一起面呢？不过后面通过小伙伴说的，好像滴滴需要大概一到两周后才有结果，那就许愿HR面，许愿OC~

