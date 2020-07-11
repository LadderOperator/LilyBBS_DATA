# LilyBBS_DATA
 南京大学小百合BBS（官方小百合）部分各类统计列表与记录（含原始数据和简单处理）

数据源：http://bbs.nju.edu.cn/bbsdoc?board=bbslists

 > 关于小百合的历史，可以参考[南京大学小百合BBS-Wikipedia](https://zh.wikipedia.org/wiki/%E5%8D%97%E4%BA%AC%E5%A4%A7%E5%AD%A6%E5%B0%8F%E7%99%BE%E5%90%88BBS)一文（小百合总体变迁历史），再结合[小百合站史](http://bbs.nju.edu.cn/bbs0an?path=/er030540162)（需要内网访问）内容进行一些了解。

## 说明

`original_data`包含了原始网页的内容；`processed_data`包含了处理后的部分数据。

### original_data

#### LilyBBS_Data

主要归档了部分帖子：

+ BBS运行情况统计

+ 每小时上站人数统计

+ 讨论区人气排行榜

+ 昨日十大热门话题

每小时在线人数统计由于早期并未统计所以暂未爬取。

+ 时间跨度：少量2006年4月之前的帖子，主要分布在2006年4月18日~2020年7月4日之间。

#### V_Suggestions

主要归档了所有的校长信箱主题帖子。

### processed_data

经过一些简单处理的数据，详细意义参考下方。

#### top10_history

十大热门帖子的数据，具体意义如下：

| 次序 | 信区 | 跟贴人数 | 发帖者 | 标题 |
| ---- | ---- | -------- | ------ | ---- |
|1 | Love | 142 | clcll | 终于走到这一步了|
|2 | NJUExpress | 84 | lalahu | 圣诞，元旦，春节，你更喜欢哪个？|
|3 | D_Astronomy | 79 | happyapple | 结婚大喜！|
|4 | Abroad | 55 | unorderly | 中国真的留不住你们吗？|
|5 | NJUExpress | 52 | hanson | 爱上一个不该爱的人|
|6 | Love | 46 | yetz | 曾进沧海难为水，对吗？|
|7 | S_Business | 36 | aces | 逸夫管理科学楼全貌:)商院就在12-20楼:)|
|8 | D_EE | 33 | pepsiy | 我到了|
|9 | NJUExpress | 22 | seemoon | 东大，真牛，^_^|
|10 | D_Information | 18 | ASE | 恩，最后一天的2001|

#### hot_boards

热门讨论区，具体意义如下：

| 次序 | 信区 | 中文名 | 人次（或人次比例） | 平均耗时（单位秒） |
| ---- | ---- | ------ | ---- | -------- |
|1 | NJUNews | 大学校园生活  | 2890 | 167|
|2 | News | 天下事大家关心  | 779 | 171|
|3 | Boys | 男生世界  | 670 | 80|
|4 | Girls | 女生天地  | 651 | 100|
|5 | Love | 情爱悠悠  | 642 | 163|

#### BBS_stat

BBS运行情况统计，撇开一些意义不大且发生过变化的项目，主要统计了如下几个数据：

| 新登帐号 | 发送信件 | 聊天次数 | 删除文章 | 发表文章 | 修改文章 | 转载文章 | 文章查询 |
| :------: | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
|    24    |   275    |    26    |    56    |   601    |    19    |    24    |    29    |

#### login_per_hour

一天内每小时登录的人数。

| 0    | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   | 11   | 12   | 13   | 14   | 15   | 16   | 17   | 18   | 19   | 20   | 21   | 22   | 23   |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 1346 | 1403 | 1406 | 1733 | 1819 | 1700 | 1749 | 1923 | 2890 | 3307 | 3174 | 2568 | 3279 | 2497 | 2775 | 2717 | 3152 | 2439 | 1963 | 2094 | 2245 | 2312 | 2253 | 2103 |

## 序言

### 这些数据可以拿来做什么？

可用于数据分析。至于怎么分析，全看你的想法了。

### 我为什么要做这一个工作？

很简单，因为**我对小百合上反复发生而又似曾相识的疑问和无视、对学校个别部门院系顽固不化地将“发送到小百合”当作完成信息传递任务的低效和落后、对一个丰富多彩的平台倒坍冷寂感到愤怒**。

众所周知，小百合曾经是高校论坛中的先锋，也是南大学子的情怀。然而数十年以来，兄弟高校的论坛与时俱进发生了改变，小百合却仍然固步自封，甚至中断了外网访问。

小百合，曾经百花齐放的网络天地，如今却急剧萎缩，靠着院系或单位发布通知公告和官方信息、校长信箱的问题沟通来维持最后的一丝气息。**无论是教职工还是学生，你必须要承认，小百合已然没落；如今的时代里，我们需要的是更加易用、更加活跃的论坛。**

有人说，论坛已死。我个人不认同这种说法，至于原因如何，有机会我会另外分享我的看法。

我将小百合的这部分数据爬取保存，并且做了些简单机械的粗活累活，主要目的有三。

1. 学会**记忆**，学会**记录**。对这些数据的挖掘，你或许可以发现这个学校里曾发生过什么。
2. 给未来所有关于“进化小百合”的建议以**数据事实支撑**。
3. 为未知而潜在的小百合数据丢失提前进行部分**备份归档**（主要为2020年7月5日以前）。

## 声明

由于帖子的内容与格式有时会出现无法预期的问题且数目较大，**本人不担保处理过的数据完全正确**（我做了几个抽样检查，目测没有大问题）。如果你发现自动处理的数据和原始的帖子有出入，请直接在`Issues`内反馈。