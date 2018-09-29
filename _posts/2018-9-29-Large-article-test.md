---
layout: base-post
title: "Large article"
categories: [blog]
---


中文维基百科Facebook粉丝专页正式上线，邀请大家一同关注。
[关闭]
Markdown
维基百科，自由的百科全书
跳到导航跳到搜索

本条目包含指南或教学内容。（2014年9月5日） 
请借由移除或重写指南段落来改善条目，或在讨论页提出讨论。

本条目包含过多行话或专业术语，可能需要简化或提出进一步解释。（2014年1月8日）
请在讨论页中发表对于本议题的看法，并移除或解释本条目中的行话。
Markdown
扩展名	.md, .markdown[1]
统一类型标识	net.daringfireball.markdown
开发者	John Gruber
初始版本	2004年3月19日，​14年前[2][3]
最新版本	
1.0.1
(2004年12月17日，​13年前[4])
格式类型	标记语言
自由格式？	是[5]
网站	daringfireball.net/projects/markdown/
Markdown是一种轻量级标记语言，创始人为约翰·格鲁伯（英语：John Gruber）。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML（或者HTML）文档”。[4]这种语言吸收了很多在电子邮件中已有的纯文本标记的特性。

John Gruber 在 2004 年创造了 Markdown 语言，在语法上有很大一部分是跟亚伦·斯沃茨（Aaron Swartz）共同合作的。这个语言的目的是希望大家使用“易于阅读、易于撰写的纯文字格式，并选择性的转换成有效的XHTML（或是HTML）”。 其中最重要的设计是可读性，也就是说这个语言应该要能直接在字面上的被阅读，而不用被一些格式化指令标记（像是RTF与HTML）。 因此，它是现行电子邮件标记格式的惯例，虽然它也借鉴了很多早期的标记语言，如：Setext、Texile、reStructuredText。Gruber也编写了的Perl脚本：Markdown.pl，用于把markdown语法编写的内容转换成有效的、结构良好的XHTML或HTML内容，并将左尖括号<和&号替换成它们各自的字符实体引用。它可以用作单独的脚本，Blosxom和Movable Type的插件又或者BBEdit的文本过滤器[4]。Markdown也已经被其他人用Perl和别的编程语言重新实现，其中一个Perl模块放在了CPAN(Text::Markdown)上。它基于一个BSD风格的许可证分发并可以作为几个内容管理系统的插件[6][7]。

由于Markdown的轻量化、易读易写特性，并且对于图片，图表、数学式都有支持，目前许多网站都广泛使用 Markdown 来撰写帮助文档或是用于论坛上发表消息。例如：GitHub、reddit、Diaspora、Stack Exchange、OpenStreetMap 、SourceForge等。甚至Markdown能被使用来撰写电子书。


目录
1	语法
1.1	图片
1.2	换行
1.3	强调
1.4	标题
1.5	断行
1.6	引用
1.7	链接
1.8	水平分区线
1.9	Markdown与html转换之例子
2	标题
2.1	二级标题
3	支持Markdown语法的软件或网站
4	编辑器
5	实现版本
5.1	C
5.2	Java
5.3	Lua
5.4	PHP
5.5	Ruby
5.6	其它语言
6	注释
7	外部链接
语法
图片
![Foo](http://i.weather.com.cn/images/cn/life/2017/04/11/11141533DF572FBBA092E37E6E843C656C318272.jpg)
换行
在文本中输入的换行会从最终生成的结果中删除，浏览器会根据可用空间自动换行。如果想强迫换行，可以在行尾插入至少两个空格。

强调
*强调* 或者 _强调_（示例：斜体）

 
**加重强调** 或者 __加重强调__
又或者以制表符或至少四个空格缩进的行，例如：

    第一行代码
    第二行代码
    第三行代码
后面一种用法会让Markdown保留所有的空白字符——而与之相反，一般情况下，Markdown会删除所有换行和空格，打乱原有的缩进和排版。

标题
可以在标题内容前输入特定数量的井号#来实现对应级别的HTML样式的标题（HTML提供六级标题）。例如：

# 一级标题

#### 四级标题
一级和二级标题还有一种写法：

一级标题
===================

二级标题
--------------------
断行
如果你真的想在Markdown中插入换行标签<br/>，你可以在行尾输入两个或以上的空格，然后回车。 这样插入换行十分麻烦，而且“每个换行都转换为<br/>”在 Markdown中并不合适，所以只在你确定你需要时手动添加。

引用
引用只需要在被引用的内容段落开头加上右尖括号>即可。你可以选择只在开头加一个。也可以在每行前面都加一个，效果是一样的。

> 这一整段的内容都会作为一个HTML的引用元素。
引用元素是会自动优化排版的（reflowable，可回流）。
你可以任意地将引用的内容包含进来，然后所有这些都会
被解析成为单独一个引用元素。
上述内容会转换成以下HTML内容：

<blockquote><p>这一整段的内容都会作为一个HTML的引用元素。引用元素是会自动优化排版的（reflowable，可回流）。
你可以任意地将引用的内容包含进来，然后所有这些都会被解析成为单独一个引用元素。</p></blockquote>
引用可以嵌套。如果要在一个引用里插入一个引用，可以用两个>开头。依此类推，根据嵌套层次加相应数量的符号。

> 这是一个引用。这是第一行
这是第二行。
>> 这是一个嵌套的引用。这是第一行。
这是第二行
> 
> 外层引用的第三行。前面需要一个视觉上的空行表示内层嵌套的结束，空行前面的>可以有可以没有。
链接
链接可以在行内插入：

[链接文字](链接地址)
例子： [Markdown](http://zh.wikipedia.com/wiki/Markdown)
另一种选择是，链接地址可以放在段落后面的脚注，前面放上链接引用标签区分。举例说，先在内容行内插入以下内容：

[链接文字][链接引用标签]
然后在段落的后面（或者文档的结尾）放上以下内容，就可以生成一个链接：

[链接引用标签]: 链接地址 "链接标题"
水平分区线
要生成水平分区线，可以在单独一行里输入3个或以上的短横线、星号或者下划线实现。短横线和星号之间可以输入任意空格。以下每一行都产生一条水平分区线。

* * *
***
*****
- - -
---------------------------------------
Markdown与html转换之例子
Text using Markdown syntax	Corresponding HTML produced by a Markdown processor	Text viewed in a browser
# 標題

## 二級標題

Paragraphs are separated
by a blank line.

Two spaces at the end of a line  
produces a line break.

Text attributes _italic_, 
**bold**, `monospace`.

Horizontal rule:

---

Bullet list:

  * apples
  * oranges
  * pears

Numbered list:

  1. wash
  2. rinse
  3. repeat

A [link](http://example.com).

![Image](Image_icon.png)

> Markdown uses email-style > characters for blockquoting.

Inline <abbr title="Hypertext Markup Language">HTML</abbr> is supported.
<h1>標題</h1>

<h2>二級標題</h2>

<p>Paragraphs are separated
by a blank line.</p>

<p>Two spaces at the end of a line<br />
produces a line break.</p>

<p>Text attributes <em>italic</em>, 
<strong>bold</strong>, <code>monospace</code>.</p>

<p>Horizontal rule:</p>

<hr />

<p>Bullet list:</p>

<ul>
<li>apples</li>
<li>oranges</li>
<li>pears</li>
</ul>

<p>Numbered list:</p>

<ol>
<li>wash</li>
<li>rinse</li>
<li>repeat</li>
</ol>

<p>A <a href="http://example.com">link</a>.</p>

<p><img alt="Image" src="Image_icon.png" /></p>

<blockquote>
<p>Markdown uses email-style &gt; characters for blockquoting.</p>
</blockquote>

<p>Inline <abbr title="Hypertext Markup Language">HTML</abbr> is supported.</p>
标题
二级标题
Paragraphs are separated by a blank line.

Two spaces at the end of a line
produces a line break.

Text attributes italic, bold, monospace.

Horizontal rule:

Bullet list:

apples
oranges
pears
Numbered list:

wash
rinse
repeat
A link.

Image

Markdown uses email-style > characters for blockquoting.

Inline HTML is supported.

支持Markdown语法的软件或网站
Apollo 使用Markdown格式化[8]
Bitbucket 提供Markdown作为编写项目README文档的其中一种标记语言。[9]
DIASPORA* 使用Markdown格式化用户发送的消息、评论和对话。[10]
Drupal 是一个Markdown插件[11]，始创于2008年。截止2011年11月，已有8000个建站软件使用了该插件。
Ghost 使用Markdown的一个标准版本编辑器来格式化撰写的文章。[12]
GitHub 使用Markdown的一个分支版本（称为GitHub Flavored Markdown）来格式化评论、消息以及其它内容。[13][14] John Gruber has described this dialect as a "superior variant" for "situations like user-submitted comments".[15]
G+ Tweaks v1.1151，一个适用于 Google+ 的 Greasemonkey 用户脚本。[16]
Instiki uses a Markdown extension to wiki syntax. The extended syntax is called Maruku.[17]
Moodle 提供 Markdown 作为语法标记语言。[18]
Posterous 提供 Markdown 作为语法标记语言。[19]
Reddit 的编辑器使用了 Markdown 语法。[20]
Showoff 使用 Markdown 作为提交的语法。[21]
Squarespace 在博客界面下提供 Markdown 编辑器。[22]
Stack Overflow 以及其他 Stack Exchange Network 网站使用一种 Markdown 的分支作为它的文章格式化系统。[23][24]
Tumblr 允许在文章中使用 Markdown。[25]
Typecho 原生支持Markdown编辑器，实时预览. [26]
The WordPress plugin system utilizes a dialect of Markdown in "readme.txt" files submitted by developers, and has plugins for Markdown.[27]
Second Gear's Elements app for iPhone and iPad gained Markdown capability with its v2 around November of 2010.[28]
知乎允许用户使用markdown来整理自己的回复并发表
图灵社区 使用markdown语法供用户写作电子书.
简书 写作网站，支持 Markdown
为知笔记 是一种类似 印象笔记 的笔记软件，支持使用Markdown语法编辑笔记
HackMD是一个支持Markdown的线上语法编辑笔记网站，可即时切换源代码与成果查看。
纯纯写作 是一种支持使用Markdown语法编辑文本的轻量级文本编辑软件
有道云笔记在2016年也开始支持使用markdown来记录
编辑器
作为一种小型标记语言，Markdown很容易阅读，也很容易用普通的文本编辑器编辑。另外也有一些编辑器专为Markdown设计，可以直接预览文档的样式。下面有一些编辑器可供参考：

Cmd Markdown Cmd Markdown 编辑阅读器，支持实时同步预览，区分写作和阅读模式，支持在线存储，分享文稿网址。
Dillinger.io 一个在线Markdown编辑器，提供实时预览以及到 GitHub 和 Dropbox 的拓展连接。
notepag 另一个在线 Markdown 编辑器，支持实时预览，提供临时网址和和密码，可以分享给其他人。
简书 一个在线Markdown编辑器与阅读社区，支持实时预览，提供分享网址。
Mou 一个 macOS 上的Markdown编辑器。
MacDown macOS 上的 Markdown 开源编辑器，作者称其深受 Mou 启发。
MarkdownPad Windows上的全功能 Markdown 编辑器。
Typora macOS、Windows 及 Linux 上的 Markdown编辑器。
WMD a Javascript "WYSIWYM" editor for Markdown (from AttackLab)
PageDown 一个Javascript写的 "WYSIWYM"（所见即所得）Markdown编辑器（来自 StackOverflow）
IPython Notebook 以IPython为后台，利用浏览器做IDE，支持Markdown与LaTex公式。
Markdown extension pack for Visual Studio Code 在VS Code安装Markdown扩展后可支持Markdown语言读写。
实现版本
由于Markdown的易读易写，很多人用不同的编程语言实现了多个版本的解析器和生成器。下面是一个按编程语言分类的实现列表。

C
Sundown, 一个用C写的Markdown实现。
Discount, 一个Markdown标记语言的C语言实现版本。
peg-markdown, 一个用C写的，使用了PEG （parsing expression grammar）的Markdown实现。
Java
CommonMark-Java Java implementation of CommonMark, a specification of the Markdown format
MarkdownJ the pure Java port of Markdown.
pegdown, a pure-Java Markdown implementation based on a PEG parser
MarkdownPapers, Java implementation based on a JavaCC parser
Txtmark, another Markdown implementation written in Java
Lua
markdown.lua[永久失效链接], a Markdown implementation in Lua
Lunamark, a markdown to HTML and LaTeX converter written in Lua, using a PEG grammar
PHP
PHP Markdown and Markdown Extra
Markdown Viewer for PHP, allows the viewing of a Mardown doc via a local PHP server (a wrapper for PHP Markdown)
Ruby
kramdown yet-another-markdown-parser but fast, pure Ruby, using a strict syntax definition and supporting several common extensions.
Redcarpet The safe Markdown parser, reloaded.
BlueCloth[永久失效链接] A Ruby implementation of Markdown
RDiscount Discount (For Ruby) Implementation of John Gruber's Markdown
Maruku A pure-Ruby Markdown-superset interpreter
其它语言
MarkdownSharp, a slightly modified C# implementation of the Markdown markup language. Developed and used by Stack Overflow.
uedit, a Javascript "WYSIWYM" editor for Markdown
Markdownr.com, a simple website to preview markdown in real time
Knockoff, a Markdown implementation written in Scala using Parser Combinators
Actuarius, another Markdown implementation written in Scala using Parser Combinators
Pandoc, a universal document converter written in Haskell
Markdown in Python[永久失效链接], A Python implementation of Markdown
ReText, an implementation for Markdown and reStructuredText.
Blackfriday, another Markdown implementation written in Go
Misaka, a Python binding for Sundown.
注释
 Daring Fireball Statement by creator John Gruber
 Markdown. Aaron Swartz: The Weblog. March 19, 2004.
 Daring Fireball: Markdown. [April 25, 2014]. （原始内容存档于2004-04-02）.
 Markdown 1.0.1 readme source code Daring Fireball - Markdown. 17-Dec-2004.
 Markdown: License. Daring Fireball. [April 25, 2014].
 MarsEdit 2.3 ties the knot with Tumblr support - Ars Technica. [2009-08-11].
 Review: Practical Django Projects - Ars Technica. [2009-08-11].
 Writeboards support in Apollo!. [2011-11-21].
 Displaying README Text on your Bitbucket Source Tab. [2010-10-01]. （原始内容存档于2010-11-11）.
 Formatting Text - Diasporial. [2011-11-09]. （原始内容存档于2011-10-24）.
 Markdown add-on for Drupal. [2011-11-15].
 Markdown Guide - Ghost Support. [2015-03-29].
 Making GitHub More Open: Git-backed Wikis - GitHub. [2010-09-01].
 GitHub Flavored Markdown - Introduction. [2011-01-03].
 Daring Fireball Linked List: GitHub Flavored Markdown. [2011-01-03].
 G+ Tweaks v1.1151. [2011-11-08]. （原始内容存档于2011-07-09）.
 Markup Choices in Instiki. [2010-08-24].
 Formatting text - MoodleDocs. [2012-03-13].
 Markdown - Posterous Help. [2010-06-26]. （原始内容存档于2013-04-27）.
 Reddit's help document on Markdown. [2010-07-20].
 Showoff project on GitHub. [2011-10-24].
 Squarespace Mini-Reference. [2010-09-30]. （原始内容存档于2010-12-16）.
 Markdown Editing Help - Stack Overflow. [2010-04-29].
 Three Markdown Gotchas - Blog – Stack Overflow. [2010-04-29].
 Tumblr Preferences. [2011-01-03].
 Typecho 0.9 正式版发布. [2013-12-10].
 WordPress Plugins. [2011-02-14].
 Second Gear's Elements App v2. [2010-11-03].
外部链接
GitHub Flavored Markdown 语法规范
CommonMark 语法规范
Markdown 语法说明（繁体）
Markdown 语法说明（简体）
简单的Markdown指南（简体）
为什么Markdown+R有较大概率成为科技写作主流？
Official Markdown project at Daring Fireball
Markdown Wiki
Older Markdown Wiki
MultiMarkdown （引入更多标记特性和输出选项的改进版Markdown）
Markdown 工具补完. 小众软件.
Markdown在线编辑工具. Mahua.
分类：标记语言
导航菜单
没有登录讨论贡献创建账户登录条目讨论
大陆简体
汉漢阅读编辑查看历史搜索

搜索维基百科
首页
分类索引
特色内容
新闻动态
最近更改
随机条目
帮助
帮助
维基社群
方针与指引
互助客栈
知识问答
字词转换
IRC即时聊天
联络我们
关于维基百科
资助维基百科
在其他项目中
维基共享资源
打印/导出
下载为PDF
可打印版本
工具
链入页面
相关更改
上传文件
特殊页面
固定链接
页面信息
维基数据项
引用本页
左侧跳顶连接

其他语言
العربية
Deutsch
English
Español
Français
Bahasa Indonesia
日本語
Português
Русский
还有14种语言
编辑链接
本页面最后修订于2018年9月17日 (星期一) 04:37。
本站的全部文字在知识共享 署名-相同方式共享 3.0协议之条款下提供，附加条款亦可能应用。（请参阅使用条款）
Wikipedia®和维基百科标志是维基媒体基金会的注册商标；维基™是维基媒体基金会的商标。
维基媒体基金会是按美国国內税收法501(c)(3)登记的非营利慈善机构。
隐私政策关于维基百科免责声明开发者Cookie声明手机版视图Wikimedia Foundation Powered by MediaWiki
