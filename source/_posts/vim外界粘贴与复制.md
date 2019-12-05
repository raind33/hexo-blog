---
title: vim外界粘贴与复制
date: 2019-12-05 14:24:56
tags: 
  - vim
  - linux
categories:
  - linux
---

#### vim 里，粘贴复制是y/p,如何把vim 里面复制的内容粘贴到vim 外或者把vim 外复制的内容粘贴到vim 里？

##### vim 缓冲区和系统剪贴板
vim 里面粘贴复制实际上是在vim 缓冲区 存取数据,而系统的ctry+c ctry+v 是与系统剪贴板之间的交互

##### 两种解决方法

1. 则可以使用 "+y 将vim 里面的内容复制到系统剪贴板或者 "+p 将系统剪贴板里面的内容复制到vim 里面。如果不存在，则需要安装vim-gnome， 然后就可以用以上命令粘贴复制
2. .vimrc 里面设置 clipboard=unnamedplus 这样就可以直接使用 y p命令直接粘贴复制了