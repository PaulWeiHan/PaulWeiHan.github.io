---
title: Markdown tutorial
layout: post
---

**声明：创建本文档的目的是出于个人学习，在使用中学习Markdown语法。**

**参考：[Markdown 语法说明 (简体中文版)][rikuGithub]**

[rikuGithub]: https://github.com/riku/Markdown-Syntax-CN "riku_github"


*   [概述](#overview)
    *   [宗旨](#philosophy)
    *   [兼容 HTML](#html)
    *   [特殊字符自动转换](#autoescape)
*   [区块元素](#block)
    *   [段落和换行](#p)
    *   [标题](#header)
    *   [区块引用](#blockquote)
    *   [列表](#list)
    *   [代码区块](#precode)
    *   [分隔线](#hr)
*   [区段元素](#span)
    *   [链接](#link)
    *   [强调](#em)
    *   [代码](#code)
    *   [图片](#img)
*   [其它](#misc)
    *   [反斜杠](#backslash)
    *   [自动链接](#autolink)
*   [感谢](#acknowledgement)
*   [Markdown 免费编辑器](#editor)

#overview

Markdown 的目标是实现「易读易写」。

可读性，无论如何，都是最重要的。一份使用 Markdown 格式撰写的文件应该可以直接以纯文本发布，并且看起来不会像是由许多标签或是格式指令所构成。Markdown 语法受到一些既有 text-to-HTML 格式的影响，包括 [Setext] [1]、[atx] [2]、[Textile] [3]、[reStructuredText] [4]、[Grutatext] [5] 和 [EtText] [6]，而最大灵感来源其实是纯文本电子邮件的格式。

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

总之， Markdown 的语法全由一些符号所组成，这些符号经过精挑细选，其作用一目了然。比如：在文字两旁加上星号，看起来就像\*强调\*。Markdown 的列表看起来，嗯，就是列表。Markdown 的区块引用看起来就真的像是引用一段文字，就像你曾在电子邮件中见过的那样。


