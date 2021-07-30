## 1.什么是Git Bash

 [Git Bash的确切含义是什么？ | 码农家园 (codenong.com)](https://www.codenong.com/17807485/#:~:text=GitBash是一个在Windows操作系统上安装bash、一些常见的bash实用程序和git的包。. 资料来源：https%3A%2F%2Fwww.atlassian.com%2Fgit%2Ftutorials%2Fgit-bash. 相关讨论.,"Git是一组命令行实用程序，旨在在UNIX风格的命令行环境中执行"...是的，也不足为奇，考虑到Git是由Linus Torvalds创建的 (en.wikipedia.org%2Fwiki%2FLinus_Torvalds) 如何使用MySQL中的命令行导入SQL文件？.) 我参考此文章

>  其中提到：Git Bash是一个shell

### 什么是shell?

 [Shell是什么？1分钟理解Shell的概念！ (biancheng.net)](http://c.biancheng.net/view/706.html) 

 真正能够控制计算机硬件（CPU、内存、显示器等）的只有操作系统内核（Kernel），图形界面以及命令行是帮助简介控制内核的一层“代理”。 在Linux下，这个命令行程序叫做 **Shell**。 

> Shell 是一个应用程序，它连接了用户和 Linux 内核，让用户能够更加高效、安全、低成本地使用 Linux 内核，这就是 Shell 的本质。
>
> Shell 本身并不是内核的一部分，它只是站在内核的基础上编写的一个应用程序，它和 QQ、迅雷、Firefox 等其它软件没有什么区别。然而 Shell 也有着它的特殊性，就是开机立马启动，并呈现在用户面前；用户通过 Shell 来使用 Linux，不启动 Shell 的话，用户就没办法使用 Linux。 

### Shell 是如何连接用户和内核的？

> 通过shell使用内核其实是在使用接口，接口其实是函数。

### Shell 还能连接其它程序

> 在 Shell 中输入的命令，有一部分是 Shell 本身自带的，这叫做[内置命令](http://c.biancheng.net/view/1136.html)；有一部分是其它的应用程序（一个程序就是一个命令），这叫做外部命令。
>
> Shell 本身支持的命令并不多，功能也有限，但是 Shell 可以调用其他的程序，每个程序就是一个命令，这使得 Shell 命令的数量可以无限扩展，其结果就是 Shell 的功能非常强大，完全能够胜任 Linux 的日常管理工作，如文本或字符串检索、文件的查找或创建、大规模软件的自动部署、更改系统设置、监控服务器性能、发送报警邮件、抓取网页内容、压缩文件等。 

 <img src="http://c.biancheng.net/uploads/allimg/190417/1-1Z41G31T3628.gif" alt="Shell在整个Linux系统中的地位示意图" style="zoom: 67%;" /> 

### Shell 也支持编程

> shell中可以像一般编程语言一样编程，使用循环、选项等
>
> Shell 主要用来开发一些实用的、自动化的小工具，而不是用来开发具有复杂业务逻辑的中大型软件，例如检测计算机的硬件参数、搭建 Web 运行环境、日志分析等，Shell 都非常合适。 

### Shell是一种脚本语言

> 有的编程语言，如 C/C++、Pascal、Go语言、汇编等，必须在程序运行之前将所有代码都翻译成二进制形式，也就是生成可执行文件，用户拿到的是最终生成的可执行文件，看不到源码。
>
> 这个过程叫做编译（Compile），这样的编程语言叫做编译型语言，完成编译过程的软件叫做编译器（Compiler）。
>
> 而有的编程语言，如 Shell、JavaScript、Python、PHP等，需要一边执行一边翻译，不会生成任何可执行文件，用户必须拿到源码才能运行程序。程序运行后会即时翻译，翻译完一部分执行一部分，不用等到所有代码都翻译完。 

汇编语言（编译型语言）：先编译成二进制形式（可执行文件），用户能用的是可执行文件，看不到源码。编译型语言的优点是执行速度快、对硬件要求低、保密性好，适合开发操作系统、大型应用程序、数据库等。 

脚本语言（解释型语言）：一边解释一边执行，不会生成任何可执行文件，用户必须拿到源码才能运行程序。  脚本语言的优点是使用灵活、部署容易、跨平台性好，非常适合 Web 开发以及小工具的制作。 

Shell 就是一种脚本语言，我们编写完源码后不用编译，直接运行源码即可。 

## 2.git、git bash和git shell有什么区别？

 [(27 封私信 / 28 条消息) git、git bash和git shell有什么区别？ - 知乎 (zhihu.com)](https://www.zhihu.com/question/34582452?sort=created) 

> Git是版本控制工具，最开始设计用于在Unix风格的命令行环境中执行。像Linux和macOS这样操作系统都包含内置的Unix命令行终端，所以在命令行中用git做版本控制就非常方便。
>
> 然而，Microsoft Windows使用Windows命令提示符，这是一个非unix终端环境，所以我们需要git bash
>
> 那么什么是Git Bash呢?
>
> Git Bash是一个适用于Microsoft Windows环境的应用程序，它为Git命令行体验提供了一个仿真层。相当于在window上通过git bash这个模拟的Unix命令行的终端出来，然后在这个终端里面做git相关的版本控制
>
> Git shell是一个通过SSH访问的Git服务器的程序，比如说你把一个主机作为git服务器，然后通过gitshell 进行SSH连接到服务器，并把服务器用作托管Git存储库。git shell一般只允许使用服务器Git相关，其他的行为是被限制的。

总结：git是unix环境中用于版本控制的工具，连接着内核。git bash是windows里的一个应用程序，模仿出unix的命令行终端(shell)，我们在windows里通过git bash做版本控制。

## 3.Git的下载与使用

 [Git的下载安装及配置 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/123195804) 参考知乎大佬

```shell
git --version # 查看git bas
```

![1627658337616](C:\Users\Jing Yilin\AppData\Roaming\Typora\typora-user-images\1627658337616.png)

我之前已经下载好了git。

### git和github的联系

> Git是一个分布式版本控制系统，而Github是一个集成了git的服务，它可以以网页或者客户端的形式，帮助用户把git本地的数据提交到远程的服务器里。 

#### 配置Github用户名和邮箱

打开Git bash，配置Github用户名和账号（需要先注册好Github账号）

```shell
# 配置用户名
git config --global user.name "username"    //（ "username"是自己的账户名）
# 配置邮箱
git config --global user.email "username@email.com"     //("username@email.com"注册账号时用的邮箱)
```

 Jing-yilin

1154896650@qq.com

```shell
git config --global user.name "Jing-yilin"
git config --global user.email "1154896650@qq.com" 
```

#### 生成ssh

在命令行输入以下指令并运行，后面连续敲三次回车，生成的ssh文件位置参照命令提示，默认是系统的用户文件夹

```shell
ssh-keygen -t rsa
#以下是结果
###################
C:\Users\Jing Yilin>ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (C:\Users\Jing Yilin/.ssh/id_rsa):
Created directory 'C:\Users\Jing Yilin/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in C:\Users\Jing Yilin/.ssh/id_rsa.
Your public key has been saved in C:\Users\Jing Yilin/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:WkN1Ffn0elFDXLKUDn/yw5vB9X+G2RaBZ6U/Pn/iepU jing yilin@LAPTOP-UKGAS8JC
The key's randomart image is:
+---[RSA 3072]----+
|          . ..B=o|
|         . ...o=+|
|        .    +o+=|
|       .     .===|
|        S     =**|
|       o .    .E*|
|      .       .*O|
|              ==B|
|            .+.+*|
+----[SHA256]-----+
```

![1627660059877](C:\Users\Jing Yilin\AppData\Roaming\Typora\typora-user-images\1627660059877.png)

#### 测试配置是否成功

在Git Bash中输入

```text
ssh -T git@github.com
```

 当我第一次使用Git的命令连接GitHub时，得到一个警告： 

![1627660118402](C:\Users\Jing Yilin\AppData\Roaming\Typora\typora-user-images\1627660118402.png)

> 这是因为Git使用SSH连接，而SSH连接在第一次验证GitHub服务器的Key时，需要你确认GitHub的Key的指纹信息是否真的来自GitHub的服务器，输入`yes`回车即可。 
>
>  Git会输出一个警告，告诉你已经把GitHub的Key添加到本机的一个信任列表里了： 

![1627660190569](C:\Users\Jing Yilin\AppData\Roaming\Typora\typora-user-images\1627660190569.png)

这表示我成功了！！！