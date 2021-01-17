---
title: '大三上 and 2020 总结'
date: 2021-01-13
published: false
slug: 16-summary
tags: ['总结']
cover_image: "./images/p16.jpg"
canonical_url: false
description: '不知所云。'
---

:::tip
这篇文章该怎么写？如何面对自己？

本来打算在元旦的时候写一篇记录一下 2020 发生的一系列事情，但因为期末考试太忙就没动笔。而且直接写的话前九个月一笔就带过了，还不如直接写大三上的总结，当然这也是标题的由来。

后来因为疫情不用考试，直接放假了。回到家里我一直在思考这学期干了什么，好像每天都很忙，好像什么都没学到，但是这学期却是我成长最快的一个学期了。

本来不打算写的，其中有一些温暖的回忆，也有一些痛苦的不堪，甚至有一些东西敏感就没法记下来分享，但是我觉得有必要记下来，可能这个页面以后都不会公开，而是保留在 git 的提交历史中。

这里面的记录的很多事情有一些在跑步时突然想起来的，也有很多已经忘记了来不及记了。趁现在还记得，记一些东西叭，一些细节以后可能就忘记了。
:::

# 开学



# 数学建模

> 本来数据建模这件事情我打算单独写一篇文章来记录的，但是因为很多东西没法写，所以一下内容均为自身经历和感受，负面情绪都会略去。

来到学校后首先面对的是数学建模，花了几天时间装了 Matlab 2020Ra ，正版真是太棒了，之前都是能破解就破解，而这次是第一次体会到名正言顺的感觉。紧接着把官网的语法教程敲了一遍就开始了。虽然我之前学过 Matlab 但是因为网课，以及没有频繁使用该工具来解决问题，所以心里是没底的。除此之外，据我观察大多人仅仅是刚接触。

在此之前我对自己的定位是侧重于写论文，其次是作为写代码的辅助，因为三个方面（代码，论文，建模）一个人至少担任一个方面，熟悉另外一个方面。熟悉另外一个方面是为了出问题后两个人方便交流排错。可能是因为前期没有过多的交流，最终结果是我来写代码，辅助建模。而对于认为自己擅长的论文方面没有参与太多。

紧接着是选题，因为专业（大数据）最终选择了 C 题，该题是做一个企业贷款风险的评估预测，根据企业各方面的特征数据来判断贷款额度。我们都认为该题是比较好上手的，而且本质上就是一道数据科学方面的比赛题目。但是和我们同一个导师的另一支队伍选择的是 B 题，该题是一道图论方面的题目。这算是一个插曲吧，因为这样老师需要思考两道问题。


分析完题目后首要工作是将特征工程做好，将特征数据提取出来。虽然接下来的工作存在分歧等待和老师探讨，但是目前该做的工作是明确的，因为晚上 6：00 发题，确定好题目和思路后就去睡觉了。

第二天一开始我本来打算用 python 来做进行数据清洗和提取特征数据，但是我和 WHJ 开始写的时候存在很多分歧，其实应当把问题分解，两个人做不同的工作，而此时是两个人在解决同一个问题也就是所谓的结对编程。这种模式确实是存在优秀的地方，但是我们之间的交流无法做到心平气和，而且 WHJ 不喜欢 Python ，所以让我来主导写代码，最后我就变成了写代码的。其实我是认为他写代码要优于我的。

最初没有思考太多，写的时候出现了很多问题，当时没有考虑到 pandas 的存在，这是视野问题。经过一番挣扎后我换了 Matlab 来做，但做到一半后出现了两个问题，首先是 Matlab 写的函数太多，我感觉自己控制不住了，切实体会到了面向过程的复杂。其次是清洗一批数据实在是太慢了，这个问题我没有复查过，现在看来应该是我写的冗余代码多了。以上的两个问题都没有很好的解决，而且我当时觉得即使写出来跑一遍也要花费很久的时间。最终和队友讨论后又换工具了，因为老师说数据库加索引很快就能搞定。

此时已经到了晚上，第一天等于什么工作都没有推进，特征工程做不完后续的所有工作都无法推进。此时已经有一些压力了。于是我们三个人开始做在那里盯着我的电脑研究 Mysql，因为我的电脑是三个人中性能最强的，加上之前折腾（安装过😂）过 Mysql  。但是问题也很大，虽然速度问题解决了，Mysql 确实非常快，几毫秒就能跑完。但是几个查询语句不会写，这个逻辑确实比较复杂，我们仨面面相觑。整个过程就是一会我座中间，一会 WHJ 座中间，一会 ZFM 座中间，然后另外俩人在旁边指手画脚，反正就是循环，折腾一番后也没有搞定，此时已经夜里三点了。从夜里十一点后改换 Mysql 后，这中间四个小时什么都没有推进！最初的打算是把特征工程做完后，一点去睡觉，而此时压力已经很大了。其实问题的根源在于 sql 语法部分存在盲区，不知道哪里不会。其次是逻辑没有有点复杂。

三点后两个队友撑不住于是去睡觉了，而我则幻想着明天在他们起来之前我能解决这个问题。

由于当时喝了咖啡，加上压力有点大没有一丝困意。到了四点我有点绝望，此时依旧没有丝毫进展。我决定换回 Python ，因为此时我想到了 Pandas ，这个工具我之前学习过，而且相对比较熟悉。于是开始了在 Jupyter 上写代码，为什么是 Jupyter ？因为如果是 PyCharm ，每次运行一遍代码都需要从头运行，而 Jupyter 则可以以代码块的方式运行，保存进度，因为每次提取数据都要花费长时间，从头跑实在太费时间了。Jupyter 确实很方便，只不过没有代码提示。（这个问题可以用 VSCode 写 ipynb 文件来解决）

虽然写的过程中存在这样那样的问题，我也意识到了之前学的是多么的不扎实，但是因为我知道该怎么定位问题，所以都能够解决。从夜里四点一直写到七点，此时已经把第一个特征数据提取出来了。看着 201 窗外由黑暗转向光明，阳光逐渐照射进来，心里是很开心的，这个问题已经彻底解决了。但一直写到九点还不见队友来，我以为他俩放弃了😡，没想到是睡过了。队友来了后，接下来就是 WHJ 分析问题，需要哪些特征数据，怎么计算，给我提需求，然后我来代码实现，一些都步入了正轨。上午已经把所有的特征数据提取完毕了。吃完饭回来后面对的最后一个问题则是将数据存到 csv 文件中，我已经很久都没睡了，所以交给了 WHJ，一点去睡觉了。直到两点我被 WHJ 叫醒，存数据也遇到了问题。这个问题我又花了将近一个小时的时间来解决，本质上还是一些细碎的问题，需要耐心看文档。

特征工程做完了，接下来迷茫了，不知道该做什么了。

老师建议采用 PCA 来提取比较重要的特征，正好 ZFM 查到了 R 中有比较方便的 PCA 处理方式，我把特征数据发给他，这个很快就搞定了！

接下来就更迷茫了，因为做这一题的每个老师对于该题的理解都不太一样，WHJ 在不断的打听，同时他和老师之间的交流也出现了分歧。我们都迷茫了，接下来不知道该怎么办，到底是设计出来一个策略还是给出具体的贷款数额。

但是总得推进，我们最终采取的策略是用 Kmenas 做无监督学习，根据特征数据对聚类，分析出大致的贷款范围，给出贷款额度。第二问根据第一问的贷款额度（标签）做监督学习，采用决策树来分析在更多钱的条件下的贷款策略。

Kmenas 很快就完成了，但是因为没发可视化展示，结果到底合理不合理是一个问题。中间还请教了我们旁边队伍的指导老师，后来发现这家伙是我们数字图像处理的老师，好家伙。但是这个问题没有解决，因为高维数据确实难以展示。不过他后来给我们提供了决策树包的一个建议，非常感谢！决策树那一块我本来打算写一个决策树😭，但是在看西瓜书数据离散化的公式之时就卡住了。然后去 Python 里面找决策树的包来解决这个问题，但是存在很多问题。正好老师说 Matlab 2020Ra 刚好加上决策树的包。知道这个信息后，经过我的一番折腾决策树部分搞定！

接下来就是第三天了，这一天的重点该是论文了，但是第三问还没有写。我本来打算加点东西上去，但是真的是没有时间了。我给论文补了点图，提供了一些数据。因为第一天没有明确的分工导致了第三天论文的紧张。

在提交论文之时我心里清楚顶多省二，最后结果果然是省二。虽然结果不尽如人意，对于我个人而言是尽力了，毕竟队友是自己选的，无话可说。

我觉得如果搭配合理一点，省一是很简单的。

# 大学生科研基金项目

我印象当时是快截至了我才知道的，因为当时没什么人报。

周三知道，周五要上报，申请书要写五千字左右。老师通知我的时候我感觉来不及了，正好同学也在弄于是我就开始写了。

这个灵感来源于在此之前评别人的贫困等级之时大家往往会受到人际关系好坏的影响。我觉得这个问题是难免的，人之常情。我在面对自己的熟悉的人则是不参与，毕竟好几个人一块讨论。虽然有时候也能感觉到有些顺序的不合理，自己也只能尽可能的保证相对的公平。

我觉得可以采用程序来判定，虽然解决了人情问题，保证相对的公平。但难点也很明显，没有统一的标准，国家虽然有贫困标准，但是家家有本难念的经，因为每家每户的实际情况都不同。

我的想法是用往届数据做训练集，往届的评价结果做标签，然后训练一个决策树模型，因为这个标准是以前人们所公认了，面对不合理的情况微调即可。

而数据是分为结构化和非结构化两种类型的数据，对于结构化的数据处理很简单，直接作为特征即可，对于非结构化的数据我认为可以采用 NLP 方面的一些情感打分模型，将其结果作为一个属性。

但是最大的问题是没有数据，😭这个问题目前也还没有解决，因为数据比较敏感！

# 洗数据&论文

这个工作我本来以为暑假就已经做完了，但是九月下旬的时候又有一批数据。

老师交给我之后，我一直在思考如何用程序来把噪点剔除，也就是这篇文章： https://blog.weijiew.com/2020/10/9-data-clean/

最终效果不是很好，主要还是人工辅助。国庆节大部分时间都在洗数据。正好此时经历了分手，每天都很痛苦。也正好借助这种重复性的工作来转移自己的注意力。分手后我感觉自己仿佛是一个窒息的人在水中猛然浮出水面的感觉，前所未有的自由，但随之而来的则是孤独。遇到开心或者伤心的事情后没有人分享。其次是分手后我觉得自己脸上的笑容变多了。hhhhh

# LDA 演讲

国庆节还做了另外一个工作，因为机器学习课程需要演讲，本来是可以选简单的 Kmeans ，但是说实话这个我讲过非常多次了，而且自己已经代码实现过。最后选了一个 LDA ，国庆节花了大概一天半的时间来准备。我感觉准备的还可以，而演讲则全凭激情。😑

现在看来自己的演讲是没有章法的，没有及时的吸引观众的注意力。需要用一个又一个的问题来引导，以后还需要磨练。毕竟我自己在听别人演讲之时很容易丧失注意力。

# 入党

我本来以为自己退出学生会后就不可能入党了，没想到最后竟然又有了入党资格，有点幸运。

除此之外班级民主评议时是五选四，我一度以为自己是选不上的，八成是出丑，也就没报什么希望。毕竟自己为班里没做过什么贡献，人际交往方面什么的也不活泼，没想到我竟然是唯一一个没有反对票的，这大概是这一年最令我开心的一件事情了。

我觉得应该是别人问问题之时，或者需要帮助的时候我没有推脱过吧，或者日常生活中与人为善态度。

入党申请的材料真是太多了，写了好多好多天，每天都是在疯狂的补材料。字还不能写错，有些字写错了可以重新打印重新填写，但是有些只能拿刀片或者胶带挂掉。

最后交材料的时候也是一堆的格式问题，太折磨人了。在此之前我一直认为的是发现问题解决问题，但是这个工作的问题是层出不穷！

其次交完材料是每周都得上的党课，老师讲的很好，很多老师都挺有魅力，能从中思考很多东西。因为纪律很严所以这大概是大一之后我最认真上的课了。

这个阶段我读到了王阳明传，这本书对我的影响

# 离开 509 



# 教资

教资这个太惨了，真是惨败。就是不提钱，时间也浪费了。最大的问题还是


# 数据库课程设计

# 四级

# 期末课程设计

* 数据库课程设计
* 机器学习
* 数字图像处理
* 大数据技术
* 软件工程


# 期末复习
