# Github issues 提交 bug 指南

## Issues 是什么
Github 的 issues 跟 Worktile 里面的任务类似，我来理解它可以是任何跟项目有关的「行动点」——
- 任务
- 待优化的地方
- bug
- 讨论
- ……

这些「行动点」可以在团队内分享、讨论，每完成（close）一个 issue 就相当于团队又进了一小步，而 github 能够把这些进度全都自动编号（#1~#N）、记录下来。

## 新建 Issues 
在任意库页面内点南 Issues 标签，再点击右侧绿色的 New Issuse 按钮进入新建 Issues 页面：
- Title——一句话描述主题，就像邮件标题一样，要直击要害
- Description——正文，如有必要围绕主题补充细节，自动以 Markdown 格式标记，不过主题已经足够清晰的话，这里留白也无妨
- Labels——标签方便日后分类管理内容和查找，比如标记 bug/docs/question/……设立标签要根据具体内容而定，比如阳老提到的文本类的 bug 要加个 content 标签，那么这个 issue 就需要 bug 和 content 两个标签（甚至更多）
- Milestone——重要的时间或进度节点，比如 Launch OpenMindClub v 2.0）
- Assignee——需要参与的成员，像 worktile 里的任务分配
- Comment——建好 issue 后会出现在内容框下方，项目成员可以回复讨论
- **重要原则：一次只说一件事，即一个 issue 对应一个主题**

填完以上内容这个 Issue 就建好了，项目成员还可以去修改（如果你看不到 Edit 按钮或是齿轮状的设置，可能是你没有这个权限，有需要可以让这个库的所有者为你开设权限），此时的 issue 状态为 open，接下来就等相关成员去讨论/解决。完成后 close issue，一个 issue 的使命就完成了，它的状态为 closed。

## 举个例子——提交开智的 bug
因为我第一次用 issue 所以提交 bug 很混乱。当时只提交了测试卡问题，还自以为这种分类能让工程师进来一次性解决。然而里面既有移动端的问题又有 Web 端的问题，既有工程师现阶段能解决的问题又有他们暂时不能解决的问题，于是我提交的 issue 变成了这样——

![](http://ww4.sinaimg.cn/large/6a2a5705gw1f1o4v8pzmxj21kw0y2gtx.jpg)

悬而未决，不能 close，需要工程师三番两次进来确认还有哪些问题。而且更可怕的时，如果一个 issue 包含多项问题，那么其他人不能从标题中获得这些信息，会导致同样的问题一而再再而三地被提及。所以一个好的 issue 至少应该：

- 一次只说一件事
- 主题、描述清晰
- 合理的标签索引

### 什么样的问题才算 bug？
- 至少要能重现的问题才是 bug
如果只是偶尔出现一次的，很可能提交了工程师也解决不了。

### Labels
以我们非程序员的身份提交 bug 的标签可以有以下几种：
- bug（如闪退/卡顿/视频不能播放/不能提交作业/……所有问题都可以加个 bug 的tag，宁杀错不放过嘛）
- enhancement（优化相关，如 4 寸屏幕下边框过宽/字过小/……）
- content（课程内容相关，如外链不能点击/图片显示不全/……）
- question（不确定的地方）
- ……

### Description
- 交待背景
	- 设备信息
	- 系统信息
	- 甚至有时候是路径，比如我从这儿进去的某个页面有这个情况，从那儿进去就没有

总之，一切努力就是减少工程师的认识负荷，能够快速地定位问题。

## 其它
- @——可以在正文里通过 @ 提醒某人/团队/组织，可以在 @ 符号前加 /cc （抄送）显得更礼貌一些，如
> /cc @young @old

- References——有时候 issues 并不是独立的，它可能跟项目的其它 issues 或内容有关，那么，可以直接在正文 reference 过去，如在正文输入
> 这个问题 @young 曾提到到过，可参考 #22

还可以 reference 其它库的问题或是 commits，暂且不提。

- Filters/Search——可以直接按 labels/milestones/assignee搜索，可以按 closed/open 状态搜索，还可以搜索关键词。比如提交 bug 的时候可以搜搜看是不是有人已经提过这个问题了呢。

参考文献：
[Mastering Issues · GitHub Guides](https://guides.github.com/features/issues/)

http://cnfeat.com/blog/2015/09/05/Mastering-issues/
