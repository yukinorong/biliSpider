## bilibili data analyse

看b站很久了，想关注一些新的up主，但茫茫大海又不知道怎么找到自己喜欢的，于是想要做一个up主推荐系统，基于算法协同过滤。

#### 结果展示

数据结构：
![在这里插入图片描述](/img/data.png)

up主推荐结果：
![在这里插入图片描述](/img/up_predict.png)

**数据分析：**
等级分布：
![在这里插入图片描述](/img/img1.png)

等级和关注数的相关性：
![在这里插入图片描述](/img/img2.png)

算法部分借鉴博客
1. https://blog.csdn.net/hlang8160/article/details/81433356
2. https://blog.csdn.net/pipisorry/article/details/51788955

#### todolist

已完成 :smile: 未完成 :scream:  不必要 :dash:
1. :smile: 爬取每个用户个人信息，uuid，性别，等级，关注数，粉丝数
1. :dash: 绕过bilibili反爬虫策略，利用webdriver模仿浏览器登录，再添加header头。  （在脚本读取页面时候，有时并不能获得完整信息，暂时认为是部分核心代码是利用js获取，而程序的get请求不能想浏览器一样运行js脚本。所以失去内容） （可能并不是bili的反爬虫策略）（废弃）
1. :smile: 曾经的我以为b站具有很强的反爬虫策略，现在发现是我太弱，原来仅仅使用api来获取数据。
    ————目前bili的反爬虫策略为，1.访问量过大会封禁ip半小时，2.关注和粉丝列表只能查看前五页。
    ————理论讲可以用代理ip池绕过，需要有更高的爬虫知识，我还需要多学习。 
1. :dash: 切记回收资源，（及时关闭webdrier,在不断地测试中，我曾开启了四十个不必要的webdrier程序）， （后来意识到不需要webdriver， 废弃）
1. :dash: 从selenium迁移到puppeteer （废弃）
1. :dash: 找到了第三方api ,利用api直接获取信息。（早期用过一段时间，后来觉得不如官方api，废弃） 
1. :smile: 获得了追番信息，每个用户和它的追番 
1. :smile: 进入关注页面，记录它所有关注的人的id。 （生成关注列表，协同过滤的数据基础）
1. :dash: 计算等级，关注数，粉丝数，播放数排行，分布统计，计算大会员比例。( 简单的数据分析，推迟）
1. :smile: up主推荐  （200615 up主推荐v1.0）
2. :scream: 做番剧推荐 
1. :scream: 更高效的爬虫方式，并且解决封ip，只能爬取5页的问题现状。 

#### contact
csdn : https://blog.csdn.net/yukinorong

