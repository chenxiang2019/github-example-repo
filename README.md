# github-example-repo: giving some advices on how to better manage github

本文记录了我对于Github使用的一些技巧，并针对以下几个方面:

- 一、提交问题；
- 二、提交和PR的注释信息；
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

一个错误示范：[WTF the bug is?](https://github.com/Wasdns/github-example-repo/issues/1)
一个参考样例：["error: HashAlgorithm.csum16: Invalid enum tag"](https://github.com/Wasdns/github-example-repo/issues/2)

## 二、提交和PR的注释信息

- 多处改动：划分为多个明确的改动类。
- 小改动：是否必要？是否能够和其他改动合并一起提交？

## 三、README形式的Github文档撰写

一个规范化、详细的文档是一个优秀项目必不可少的内容。在Github上有两种撰写文档的方式，一种是"README"，另一种是wiki，本节主要介绍笔者在使用README进行文档记录的一些经验，主要包括：

- 1.如何创建README文档；
- 2.使用markdown语法记录、修改文档；
- 3.通用的README文档格式；
- 4.实验室Github项目，README文档参考规范及示例；
- 5.现有大型商用项目README文档参考示例。

### 1.如何创建README文档

**方法一：**

在创建一个新的项目时，有一个名为"Initialize this repository with a README"的选项，勾选即可为该项目创建一个README文档：

![](https://cloud.githubusercontent.com/assets/4122993/16925080/64863a10-4cd7-11e6-8da7-b31a29b769f2.png)

在项目目录中，该文件是"README.md"，`.md`后缀表明该文件是Markdown文件，使用Markdown文本编辑语言进行文件编辑。

**方法二：**

在项目主页中，有一个名为"Create new file"的按钮，如图红色阴影部分所示：

Figure: Create README

点击进入创建界面，在"Name your file"一栏中，填入以`.md`后缀名结尾的文件名，如"README.md"：

Figure: Name your file

Github默认在页面中显示使用"README.md", "readme.md", "README", "readme"作为名字的文件内容；其中在显示"README.md"和"readme.md"文档时，Github基于Markdown语法对其进行显示，比如将文件的内容：`# [标题名称]` 以一级标题的形式显示出来。

紧接着就可以在下方的文本框中开始文档的撰写了。此外，Github支持在线的文档视图，点击如图红色方框 "Preview"(创建文件时显示)/"Preview changes"(修改文件时显示) 所示：

Figure: Preview changes 1

即可将刚才新增/修改的内容以可视化的形式呈现：

Figure: Preview changes 2

最后，合理在commit中描述该文档，并将该文档提交到你的项目中：

Figure: Commit README

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

### 4.实验室Github项目，README文档参考规范及示例

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
