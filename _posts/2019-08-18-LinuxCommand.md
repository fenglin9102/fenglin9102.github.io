---
layout:     post
title:      Linux 常用命令
subtitle:   ln链接 grep搜索内容 find查找文件
date:       2019-08-18
author:     枫林
header-img: img/hua_shan.jpg
catalog:    true
tags:
    - Linux
---



### ln  链接 ln -s 软链接(可以给目录创建)

1. 创建软链接,只记录名称, 和Windows的快捷方式类似

   ```shell
   ln -s a.txt a_soft_link
   ```

2. 在其他的目录下创建软链接，源文件要写绝对路径

   ```shell
   ln -s ~/Desktop/pic1/b.txt ~/Desktop/b_soft_link
   ```

   

3. 创建硬链接，不可以给目录创建硬链接，相当于给源文件复制一份，与源文件内容同步发生变化，删除源文件不影响硬链接。

   ```shell
   ln a.txt ab_hard_link  
   ```

   

### grep 搜索内容

1. 显示包含匹配文本ask的所有行 -n 显示第几行 -i 不区分大小写 

   ```sh
   grep -ni ask c.txt
   ```

2. 显示不包括匹配文本的所有行（相当于求反）

   ```sh
   grep -v ask c.txt
   ```

3. 搜索以h开头的行

   ```sh
   grep -n ^h c.txt
   ```

4. 搜索以s结尾的行

   ```sh
   grep -n s$ c.txt
   ```

5. 查找目录中的所有文件匹配文本“今天”的内容

   ```shell
   grep -nr 今天 ~/Desktop/pic1 
   ```

   

### find 查找文件

1. 查找当前目录及其子目录下的a.txt

   ```shell
   find . -name a.txt
   ```

2. 查找家目录下所有的以txt结尾的文件

   ```sh
   find ~ -name '*txt' 
   ```

   