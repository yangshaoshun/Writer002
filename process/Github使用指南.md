# Github使用指南

+ 使用 github-pages 服务 by `大妈`
+ [github工具 by `大妈`](https://github.com/OpenMindClub/Writer002/issues/81#issuecomment-202125714)
+ 快速查看笔记和作业 by `阳老`
+ github Repository Graphs -- network graph visualiser

## 使用 github-pages 服务 by `大妈`

安心了,,,只要 github 的仓库还在,
你的还是你的,,,,
内容永远不可能丢失的了,无论你本地仓库还是远程的...

现在你的问题只是 gitbook 系统有问题,
那么为什么这么纠结 gitbook 官网服务呢!?

- gitbook 本身只是一个 node.js 的工具,可以帮助我们快速从 md 变成图书网站
- gitbook.io 是基于 gitbook 工具发布的一个自动编译发布图书的服务
- 我们的目标是什么?! 可以实时的发布自个儿的写作成果
- 那么,使用 gitbook 并不一定只能通过 gitbook.io 哪?!

最简单的:
- 使用 github-pages 服务
- 在本地使用 gitbook 完成网站的编译
- 将编译成果通过 git 推送到 github-pages 空间
- 就完成了 github.io 托管的 gitbook 图书发布!
- 依然免费,依然全 git 打通
- 唯一的变化是 gitbook 是自个儿编译了而已...

以上,,,嘦明确目标,方法总是很多的,,,

程序猿的工程师习惯,就是不能将所有希望寄托在别人的服务品质上
一定要尽可能多的掌握在自个儿手里!

---

技术提问时请按照以下格式来描述你的问题，并截图说明状况，以便他人理解、复现你遇到的情况。

![](https://ci3.googleusercontent.com/proxy/EYAca1SNqJUsc3inBZhvZpjRii28WUG_O7HP6ilmS1Fz2OZwQHvkXgNPRlOJlmzd-iPD1RaoK1G7kvQ05Iq3zxAzKM8Kd2QW0D6ZJ5oe4ttr-E1J98xabYGWT4MDiV4FBWf5KFpx-mk_LGyCPq3HycOt1uj9giGLUHEeqPPVwonZia7V3vtyuRrgK5mKsTeEVGi6AwceVo-cFS4beJICh1w6bkNjMhaWWH8CpE-cQT0RwZFeGaQ03FQQ2T49EH-riBWiB5Yini2VG5I=s0-d-e1-ft#https://camo.githubusercontent.com/4c9a5eefab71914dfa84a3a15c69a6e44b24366b/687474703a2f2f6f70656e6d696e64636c75622e71696e6975646e2e636f6d2f73686172652f546570464151546563682e706e67)

（原文见[3w]任务 讨论/交付/展示 · Issue #57 · OpenMindClub/OMOOC2py）


## github工具 by `大妈`

>2016-03-27 3:37 GMT-05:00 tigersword <notifications@github.com>:
Github 对我这个文科生实在是有点烧脑，本来想放弃，直接进入课程学习。后来发现Github在写作课里面确实用处挺大，所以今天花了半天时间研究，稍微弄懂了一点，把我的理解发出来，请同学们指点。

有思考, 有输出, 有讨论
才有真正而不是想象的进步!

github 本质上只是个 git 的 themes,
只是没想到被程序猿们玩成了世界上最大的同性交友网站而已,
对于文科生, 应该从自个儿习惯的信息控制角度来理想:

- github 就是个比较任性的 BBS
- 和传统的 BBS 比较,多了个 git 工具远程操作的渠道而已

> #我的理解
 1.fork 某个库就是从这个库建立一个子库，我们提交的笔记和作业就是在子库里面呈现。比如xxx/Writer0022。

- 不是 子库
- 所谓 父子关系,前提是这两个仓库有持续的数据交流关系
- 但是,现在明确的, 课程仓库 fork 后,永远不必合并回数据
- 即, 只是起了两个作用:
    + 作为模板, 快速为大家建立相同结构的课程仓库
    + 利用 github 的内置功能, 从
        * https://github.com/OpenMindClub/BookWriter002/network 可以观察到所有学员的动态进展情况
        * 从 https://github.com/OpenMindClub/BookWriter002/network/members
链接到所有合法同学
        * ...

> 2.issue 是用来讨论问题的，相当于另开一个话题。issue 和 库里面的正文似乎没有太大联系？

- github 本质上又一个通过 G.F.M 惯通了的 wiki !
- 相同的增强语法可以在 github 的一切场所使用:
    + 仓库
    + issue
    + wiki
    + commit log
    + diff. review
    + pull request log
    + ...
- 而所有场景中文字的关联点只有两种:
    + commits id (git 全球版本指纹)
    + url link (包含 issue/wiki/外部任意链接)
- 所以, 任何github 中的信息本质上是关联的
- 但是, 我们可以不关联,也可以关联
- 关键在我们在怎么用 github !
    + 如果是个文学作品的撰写,融入到 github 中的话
    + 俺推荐:
        * wiki 积累素材
        * issue 追踪卡片写作
        * 仓库追踪成品写作
而相互作用图谱:

```
    git +-> wiki
        ^   \
        +~>  +-> repo.
        | (linked)
      issue
```

- 用 git 来远程管理 wiki/repo 中大块的有结构的文字/资料
- 用 web 在 issue 中进行快速卡片写作和讨论
    + 用链接关联对应 wiki/repo 页面
    + 完成阶段整理/迭代后, 关闭 issue
    + 将成果嵌入到对应 wiki/repo 文章中
    + 最好, 在对应文章中,注上 issue 的来源链接
- 这样,一个持续的写作过程,就被合理分解为:
    + 积累
    + 试写
    + 改进
    + 组合
    + 编辑
    + ...
    + 等不同的行为模式,都有最合理的容器来管理,永久追踪

> 3.writer002 和 bookwriter002 相当于两个内容，前者是发布课程相关信息，后者是用来提交笔记和作业？

- 对于写作,只有最终交付形式的不同
- 内容上应该都是一脉相传的...
- 所以, 两个仓库,或是多种发布形式不重要,
- 重要的是,我们是否能有意识的利用 github 提供的最小工具集来管理写作这一复杂过程的所有环节!?
- ...

> #几个问题
> 1.Github 学习开始看的是廖雪峰的教材，我觉得有点误导我了。不过把疑惑提出来：既然Github 是个在线写作工具，如果所有子库将来merge（或者说是 pull request，这两个术语还有点没弄清），内容岂不是会变得很乱？还是说永远不会进行这样的处理？另外一点，为了保证能够merge，提交的文件对文件名、格式什么的是不是得有一定要求？

- github 从来不是在线写作工具
- 人家目标是唯一的: 最好用的 开源项目托管空间
- 只是, github 提供的基础功能,好象可以用以任何种类的项目
    + 写作项目也是一种项目
    + 只是没有代码而已...
- 对于作者只有一个的写作项目, 当然永远没有必要合并
- 除非是类似 众筹小说 这种项目
    + 但是, 这时的内容合并,也和代码合并一样
    + reveiw/test 什么的都不能少...
- 但是, 开智写作班, 强调使用 github 来管理写作,并不是真的只是为了写作
    + 为了过滤出未来的 CEO 们
    + 那么就必须能理解未来无论什么创业项目,都不能少的程序猿这一异种生物的思想和行为
    + 所以, 先体验好 github 的生态环境
    + 以便, 将来面试程序猿时,能有共鸣...
> 2.要看到大家提交的笔记和作业，除了课程方推荐，是不是得自己到各个同学的子库里面一个个点开才能看到？

- 嗯哼,这是个麻烦
- 同时,也是个具体需求
- 当然, 有3种以上的解决方案
- PS: 之前课程同学们,都找到了自个儿的解决方案, 请 show 出你的...

> 3.客户端或者终端能发issue吗？如何发？找了半天没找到……

- 嗯哼,提醒 提问的智慧!
- 你怎么找的, 什么关键词? 什么预期?
- 嗯哼,俺一次搜索就搜索出两个以上的对应工具来....

## 快速查看笔记和作业 by `阳老`

> 1.fork 某个库就是从这个库建立一个子库，我们提交的笔记和作业就是在子库里面呈现。比如xxx/Writer0022。

是的。这个子库是你自己拥有一切权限。

> 2.issue 是用来讨论问题的，相当于另开一个话题。issue 和 库里面的正文似乎没有太大联系？

是的。它就是一个小型的BBS、小型的任务管理系统。

> 3.writer002 和 bookwriter002 相当于两个内容，前者是发布课程相关信息，后者是用来提交笔记和作业？

是的。正是如此。

> 2.要看到大家提交的笔记和作业，除了课程方推荐，是不是得自己到各个同学的子库里面一个个点开才能看到？

有很多简便操作喽。

### 方法1：直接通过排行榜访问

你可以通过手机端、Web端的排行榜，点击进去，然后查看同学的Github 笔记。

例如：

![](https://camo.githubusercontent.com/761a1f246cba9a0098bc308a0f06f42c0f70d898/687474703a2f2f6f70656e6d696e64636c75622e71696e6975646e2e636f6d2f6f7579616e672f6f70656e6d696e64636c75622e706e67)

### 方法2：直接查看同学的提交情况

所有同学的笔记在这里：[Network Members · OpenMindClub/BookWriter002](https://github.com/OpenMindClub/BookWriter002/network/members)

方法3：通过每周作业笔记交付展示 Issue 查看

比如 [#82](https://github.com/OpenMindClub/Writer002/issues/82) [#55](https://github.com/OpenMindClub/Writer002/issues/55) [#41](https://github.com/OpenMindClub/Writer002/issues/41)

## github Repository Graphs -- network graph visualiser

- [Say hello to the Network Graph Visualizer](https://github.com/blog/39-say-hello-to-the-network-graph-visualizer)
- [About Repository Graphs](https://help.github.com/articles/about-repository-graphs/)

> The Network graph shows the branch history of the entire repository network, including branches of the root repository and branches of forks that contain commits unique to the network.

> To see older branches, click and drag within the graph.

GitHub网络(Network)是一个非常强大的工具，让我们能看到每一个贡献者的代码提交，以及这些提交与其他的提交有什么关联。当我们作为一个整体观看这个网络的可视化展现时，我们能看到每一个库，每一个分支，和每一个提交.

![](https://help.github.com/assets/images/help/graphs/repo_network_graph.png)

- 查看主库的分支, 即各个成员 fork 的库
- 查看各个fork库的动态,包括每一次提交 / merge状态
- 按照 commit 时间线展示, 即可以方便的时间倒序查看成员的动态