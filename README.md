# github-example-repo: giving some advices on how to better manage github

本文记录了我对于Github使用的一些技巧，并针对以下几个方面:

- 一、提交问题；
- 二、提交(commit)的注释信息；
- 三、README形式的Github文档撰写。

给出了自己的一些建议，不足之处欢迎各位指出，欢迎补充、提问和PR ：）。

## 一、提交问题

**在提问之前，请确认你的问题是否能够通过以下方式解决：(1)百度；(2)bing；(3)Google；(4)Stackoverflow。**

一个参考的主要提问步骤分为：

- (1)标题：出现bug的概要，例："在根目录下，某某文件无法找到"
- (2)背景介绍(可选)：介绍你大概的目的是什么；例："为了测试数独，我做了这个实验，遇到了这个问题。"
- (3)实验环境：你的系统环境、安装的依赖，选择性给出；例："我的操作系统为Ubuntu 14.04，64位。"
- (4)**重要**：重现bug的步骤，尽量条理清晰、简明；
- (5)期待出现的行为(可选)：如果没有遇到这个bug，你希望得到的结果是什么；
- (6)结果出现的行为：较为全面的bug信息，或者错误日志，或者二者兼具；
- (7)额外信息：一些附加的信息，如代码(简短的骨架，或者以站外链接的形式贴出)，或者你对于该错误的认识；
- (8)礼貌用语。

错误示范：[WTF the bug is?](https://github.com/Wasdns/github-example-repo/issues/1)

参考样例：["error: HashAlgorithm.csum16: Invalid enum tag"](https://github.com/Wasdns/github-example-repo/issues/2)

## 二、提交(commit)的注释信息

- 多处改动：划分为多个明确的改动类。
- 小改动：是否必要？是否能够和其他改动合并一起提交？

对于一个commit来说，一个完备的注释信息有助于让其他人了解你的这次提交做了什么工作。例如，项目管理员对PR进行code review时需要对于该PR的每一次提交进行审核，如果每次提交的注释信息都非常简单/杂乱，那么对于code reviewer来说是非常不友好的：他需要翻看你每一次文件的修改记录来判断你的这次提交做了什么工作。

一个规范的commit有这样的几个特点：

- 1.注释信息的标题有一句清晰的概述；
- 2.注释信息简洁明了，同时保留必要信息；
- 3.注释信息的拓展描述中，对于每一处的修改都有清晰的记录；
- 4.必要性；

**1.注释信息的标题有一句清晰的概述：**

标题至少需要有一句完整的句子来说明本次提交做了哪些工作。在大部分同学的github中，每次提交的注释信息通常只有"更新"、"修改"几个单词，其他开发者自然很困惑：到底你更新了什么、修改了什么？只能通过查阅详细信息来查看这次commit的具体修改。一个参考的规范注释信息标题的格式为`文件名：简述改动信息`。

错误示例：`提交`，`更新`，`发布`；

参考示例：`文件名：简述改动信息`，如：`README.md: 更新第三章，加入了对commit注释信息的描述`。

**2.注释信息简洁明了，同时保留必要信息：**

第二点要求注释信息尽量简洁明了，不加入过多的不必要信息；此外要体现出注释信息的目的，并且保留必要信息。

错误示例1：`我把第二段中女神的代码给删除了。` 其中`女神的代码`是不明确且不必要的，而且没有体现出本次提交的目的。

参考示例2：`修改"你今天真好看"功能的API：删除了文件hello.c的第40、56、78行，修改了函数hello()的返回参数类型。`

错误示例2：`今天客户A那货提出了一个需求叫做"你今天真好看"，后面的同学注意了，我把原来文件hello.c中的一些功能做了适配，来支持这个新功能。`

参考示例2：`增加"你今天真好看"功能：修改hello.c中函数hello()的返回参数类型。`

**3.注释信息的拓展描述中，对于每一处的修改都有清晰的记录：**

如果一个提交修改了项目中的多个文件/模块，可以将这些修改的共同点，如`加入新功能"你今天真好看"`，作为提交注释信息的标题，并将这些修改的具体信息在注释信息的文本栏中分点列出。

错误示例：

```
Title:   
         按今天客户A的需求加了一个新功能
Content: 
         修改了文件hello.c, beauty.c, stupidClient.c。
```

参考示例：

```
Title:   
         2017/10/1：加入新功能"你今天真好看"
Content: 
         1.修改文件hello.c中的第101行：hello函数返回参数类型；
         2.修改文件beauty.c中的第20行：将hello函数结果进行输出；
         3.增加2017/10/1的客户需求到文件stupidClient.c中。
```

**4.必要性：**

有一些commit完全没有必要，或者对于该项目毫无意义，比如：

错误实例1：小陈是个强迫症，他将文件A中所有换行的左括号改为了不换行，提交了上去，同时刷了一下KPI，心里美滋滋的。

错误实例2：负责在Github上进行某个项目开发的小李被开除了，被迫离开了现在的公司；在离开前，她将本地仓库中所有的内容删除，并将这些修改提交到了项目中，以此宣泄心中的愤恨。

不提交没有必要、毫无意义的commit是每一个项目成员应该遵守的规范。

## 三、README形式的Github文档撰写

一个规范化、详细的文档是一个优秀项目必不可少的内容。在Github上有两种撰写文档的方式，一种是"README"，另一种是wiki，本节主要介绍笔者在使用README进行文档记录的一些经验，主要包括：

- 1.如何创建README文档；
- 2.使用markdown语法记录、修改文档；
- 3.通用的README文档格式；
- 4.实验室Github项目，README文档参考示例；
- 5.现有大型商用项目README文档参考示例。

### 1.如何创建README文档

**方法一：**

在创建一个新的项目时，有一个名为"Initialize this repository with a README"的选项，勾选即可为该项目创建一个README文档：

![](https://cloud.githubusercontent.com/assets/4122993/16925080/64863a10-4cd7-11e6-8da7-b31a29b769f2.png)

在项目目录中，该文件是"README.md"，`.md`后缀表明该文件是Markdown文件，使用Markdown文本编辑语言进行文件编辑。

**方法二：**

在项目主页中，有一个名为"Create new file"的按钮，如图红色阴影部分所示：

![](https://github.com/Wasdns/github-example-repo/blob/master/figures/create-readme.png)

点击进入创建界面，在"Name your file"一栏中，填入以`.md`后缀名结尾的文件名，如"README.md"：

![](https://github.com/Wasdns/github-example-repo/blob/master/figures/name-your-file.png)

Github默认在页面中显示使用"README.md", "readme.md", "README", "readme"作为名字的文件内容；其中在显示"README.md"和"readme.md"文档时，Github基于Markdown语法对其进行显示，比如将文件的内容：`# [标题名称]` 以一级标题的形式显示出来。

紧接着就可以在下方的文本框中开始文档的撰写了。此外，Github支持在线的文档视图，点击如图红色方框 "Preview"(创建文件时显示)/"Preview changes"(修改文件时显示) 所示：

![](https://github.com/Wasdns/github-example-repo/blob/master/figures/preview-readme-1.png)

即可将刚才新增/修改的内容以可视化的形式呈现：

![](https://github.com/Wasdns/github-example-repo/blob/master/figures/preview-readme-2.png)

最后，合理在commit中描述该文档，并将该文档提交到你的项目中：

![](https://github.com/Wasdns/github-example-repo/blob/master/figures/commit-readme.png)

**方法三：**

在主机的仓库中创建README文档，并提交至Github上。该方法不再具体阐释。

注：上文中创建的README文档即项目中的[simple-README.md](https://github.com/Wasdns/github-example-repo/blob/master/simple-README.md)。

### 2.使用Markdown语法记录、修改文档

这里为读者提供了一些用于掌握基本的Markdown语法的参考资料，包括：

- [Markdown快速入门](http://wowubuntu.com/markdown/basic.html)
- [Marstering Markdown](https://guides.github.com/features/mastering-markdown/)

Github上README文档的记录、修改与普通的Markdown文档的记录、修改无异。

### 3.通用的README文档格式

Github官方给出了[一种通用的README文档格式](https://guides.github.com/features/wikis/):

- 项目名：在人们往下浏览你的仓库之前，首先会看到你的项目名称；项目名称应在README文件的首部。
- 描述：对于接下来README内容的一个描述；一个好的描述是非常清晰、简洁、切合主题的；用于描述该项目的重要性以及作用。
- 内容表格：可选；引入内容表格的目的在于为人们提供一个快捷的导航，尤其是在README文档内容多且详细的时候。
- 安装：接着，安装教程告诉用户如何快速、正确安装你的项目；可以考虑的是，做一个gif描述安装过程，使其他人对整个过程更加清楚。
- 使用说明：下一个阶段是使用说明，用于告诉已经安装好项目的用户如何使用你的项目；该处适合增加一些项目的截屏。
- 贡献：一个大型商用项目通常有一个独立的章节，用于描述如何为这个项目作出贡献(如文件命名、编码规范等)，有时可能是一个独立的描述文件；如果你有特殊的要求，详细地解释你的要求有助于其他开发者更好地为你的项目做出贡献。深入阅读：[setting guidelines for repository contributors](https://help.github.com/articles/setting-guidelines-for-repository-contributors/)
- 荣誉：增加一个章节用于列举出项目的作者和做出贡献的开发者们。
- 许可证：加入一个章节用于描述该项目的许可证。如何选择一个合适的许可证：[licensing guide](https://choosealicense.com/)，也可以参考阮一峰老师的教程：[如何选择开源许可证？](http://www.ruanyifeng.com/blog/2011/05/how_to_choose_free_software_licenses.html)

### 4.实验室Github项目，README文档的参考示例

标准语言：English。

一个实验室Github项目，README文档参考示例由以下几个部分组成：

- Chapter1: 项目名称(一级标题)+项目贡献描述(内容，以点列出)；
- Chapter2: 安装所需的软件依赖，贴上对应的Installation Guide链接；
- Chapter3: "Getting Start" 项目，即入门级项目，一个帮助用户快速上手的demo；
- Chapter4: README主体部分，以项目贡献点列章节，每个章节阐述项目中对应于该贡献点的文件和子模块；
- Chapter5: 相关工作，相关的论文或者Github项目，给出链接；
- Chapter6: 问题向导，当用户遇到问题时解决问题的方法，包括给出社区链接、相关issues、联系邮件地址等等；
- Chapter7: 引用的参考文献，作者信息。

### 5.现有大型商用项目README文档参考示例

- [Baidu, brpc](https://github.com/brpc/brpc)
- [Barefoot, behavioral-model](https://github.com/p4lang/behavioral-model)
- [Google, protobuf](https://github.com/google/protobuf)
- [DeepMind, pysc2](https://github.com/deepmind/pysc2)

## 四、参考资料

- [CloudLab Coding Style Guide, George Washington University](https://github.com/sdnfv/openNetVM/blob/master/style/styleguide.md#cloudlab-coding-style-guide)
- [Github Guides](https://guides.github.com/)
- [Documenting your projects on GitHub](https://guides.github.com/features/wikis/)
- [Mastering Issues](https://guides.github.com/features/issues/)
- [Markdown快速入门](http://wowubuntu.com/markdown/basic.html)
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [setting guidelines for repository contributors](https://help.github.com/articles/setting-guidelines-for-repository-contributors/)
- [licensing guide](https://choosealicense.com/)
- [如何选择开源许可证？](http://www.ruanyifeng.com/blog/2011/05/how_to_choose_free_software_licenses.html)
- [Composite Style Guide](https://github.com/gparmer/Composite/blob/master/doc/style_guide/composite_coding_style.pdf?raw=true)
- [Google's C++ Style Guide](http://google-styleguide.googlecode.com/svn/trunk/cppguide.html#Header_Files)
