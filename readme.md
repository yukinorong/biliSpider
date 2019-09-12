## bili data analyse

看b站很久了，想关注一些新的up主，但茫茫大海又不知道怎么找到自己喜欢的，于是想要做一个up主推荐系统，基于算法协同过滤。

算法部分借鉴博客

https://blog.csdn.net/hlang8160/article/details/81433356

https://blog.csdn.net/pipisorry/article/details/51788955

#### todolist

已完成 :smile: 未完成 :scream:  不必要 :dash:
1. 爬取每个用户个人信息，uuid，等级，是否大会员，关注数，粉丝数， :smile:  播放数。 是否大会员 :scream: 
1. 绕过bilibili反爬虫策略，利用webdriver模仿浏览器登录，再添加header头。 :dash: （在脚本读取页面时候，有时并不能获得完整信息，暂时认为是部分核心代码是利用js获取，而程序的get请求不能想浏览器一样运行js脚本。所以失去内容） （可能并不是bili的反爬虫策略）
1. 切记回收资源，（及时关闭webdrier,在不断地测试中，我曾开启了四十个不必要的webdrier程序）， :dash:
1. 从selenium迁移到puppeteer :dash:
1. 找到了第三方api ,利用api直接获取信息。 :smile:
1. 获得了追番信息，每个用户和它的追番 :smile: 
1. 进入关注页面，记录它所有关注的人的id。 :scream:
1. 计算等级，关注数，粉丝数，播放数排行，分布统计，:smile: 计算大会员比例。 :scream:
1. 做番剧推荐，和up主推荐（算法协同过滤）:scream:
