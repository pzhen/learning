---
title: Vim - 常用命令
toc: true
date: 2017-07-19 17:42:58
share: true
tags:
 - Vim
 - Linux
categories:
 - Linux
 - Vim
---

```
----------------------------光标移动-------------------------
h 向左移动一个字符
j 向下移动一行
k 向上移动一行
l 向右移动一个字符
 
control f 向下翻一页
control b 向上翻一页
control d 向下翻半页
control u 向上翻半页
 
+ 非空格下一行
- 非空格上一行
 
n + 空格  移动n个字符
0  移动到当前行第一个字符处
$  移动到当前行最后一个字符处
G  移动到最后一行
nG 跳到n行
gg 第一行
 
n 回车  向下n行
?keyword 向上查找 配合 n N 来上下查找
/keyword 向下查找 配合 n N 来上下查找
 
:n1,n2s/keyword1/keyword2/g  在n1到n2行之间，查找keyword1并且替换成keyword2
:1,$s/keyword1/keyword2/g  同上只不过是从1-最后一行
:n1,n2/keyword1/keyword2/gc 只不过要确认后才替换
 
-----------------------------粘贴复制------------------------
x 向后删除一个字符
X 向前删除一个字符
nx 连续向后删除n个字符
dd 删除当前行
ndd 删除向下n行
 
d1G 删除光标之前所有
dG  删除光标到最后
d$  删除光标到行末
d0  删除光标行首
 
yy 复制当前航
nyy 向下复制n行
y1G 复制光标到行首
yG  复制光标到最后一行
y0  复制光标到行首
y$  复制光标到行末
 
p 光标下一行粘贴
P 光标上一行粘贴
 
---------------------------------插入------------------------
i 光标位置插入
I 当前行非空第一个字符处插入
a 光标处下一个字符插入
A 当前行最后一个字符插入
o 下一行插入
o 上一行插入
 
:w filename 保存到另一个文件
:r filename 读取文件内容到当前
 
:! command  暂时离开vim 执行命令
---------------------区块选择-------------------------------
v 字符区块选择
V 行区块选择
y 复制区块
d 删除区块
contrl + v 范围区块
区块选择下 按 = 键 自动排版，代码会自动排版
--------------------多文件同时编辑--------------------------
vim filename1 filename2
:n 下一个文件
:N 上一个文件
:files 打开的文件列表
-------------------分屏---------------------
:sp filename
ctrl + w 来切换光标
```
