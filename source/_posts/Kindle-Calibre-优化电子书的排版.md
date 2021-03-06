---
title: Kindle - Calibre 优化电子书的排版
toc: true
comments: true
share: true
date: 2017-08-15 15:33:12
tags:
 - Kindle
 - Calibre
 - Ubuntu
categories:
 - Kindle
---

不论是在亚马逊 Kindle 电子书商店购买的电子书还是从其它渠道下载到的电子书，总免不了会遇到排版不如人意的情况，这时就可以使用 Calibre 简单优化一下，使之更符合自己阅读习惯。<!-- more -->

组成 Kindle 电子书的主要成分是 HTML 和 CSS，因为 KF8 标准支持大部分 HTML 标签以及 CSS 属性，如果你有点儿写网页代码的基础，完全可以制作出排版精良的电子书，就算没有也没关系，只需要在使用 Calibre 转换电子书的时候，修改几个参数就能达到较好的效果。

对电子书排版的修改优化是在转换的过程中进行的，一般电子书的排版涉及到以下几个要素：

 - 行间距，即段落内的两行文字基线之间的高度。
 - 首行缩进，即把段落的第一行从左向右缩进一定的距离。
 - 段落间距，即两个段落之间的距离。
 
在转换电子书时，建议先把“输出格式”设置为“AZW3”（如果您想要试用 mobi 格式，则需要在“MOBI 输出”中设置一下“MOBI 文件类型”为 both）。然后切换到“界面外观”，分别对和上面提到的几个要素对应的设置项的数值进行修改。下面给出的数值都是建议数值，具体可根据自己的喜好调整。

![](http://static.golangtab.com/images/2017-08/calibre-type-setting.jpg)


 - 行间距：设置“最小行高”数值，如“140%”。
 - 首行缩进：先勾选“删除段间空行”，再设置“缩进尺寸”的值，如“2.0em”。
 - 段落间距：先勾选“在段落间插入空白行”，再设置“行间距”的数值，如“1em”。

>-注意，“最小行高”的单位是百分比，“缩进尺寸”和“行间距”的单位为 em，两者都是相对单位，它们都是以当前字体垂直高度为基准。比如 150% 和 1.5em 都等于一个半垂直字高的高度。

设置完毕后点击【确定按钮】开始转换，转换完毕后，鼠标右键点击电子书，在弹出的菜单中点击“打开所在目录”，把生成好的 AZW3 格式（或 MOBI 格式）的电子书拷贝到 Kindle 中阅读即可。

>-提示：如果你想把电子书推送到云端并保持设置好的排版，还需要做额外的处理。因为目前亚马逊个人文档服务不支持直接推送 AZW3 格式，对于 Calibre 转换的 both 模式的 mobi 格式，也经常出现无法推送成功的情况，所以推送之前，可以先把电子书先转换成 epub 格式，再用最新版本的 KindleGen 转换成 mobi 格式，然后再用邮箱进行推送即可。具体步骤请移步这里查看。


## 参考资料
> - [Calibre 使用教程之优化电子书的排版](https://bookfere.com/post/260.html)
