# 《linux-0.12 内核完全剖析》

![1528507608975.png](image/1528507608975.png)

赵炯，上海同济大学计算机通信专业毕业，多年从事操作系统，计算机网络和系统软件的研究工作，具有很高的学术水平。2004年编写的《Linux内核完全注释 -基于0.12内核》（**Linux 0.12版本发布于1992年1月15日**）一书，一年内印刷4次，在各大计算机排行榜始终名列前茅，并被《中华读书报》评为“2004年度十大电脑图书”之一。

![1528517709173.png](image/1528517709173.png)

## 本仓库内容

1. linux 0.12 源码
2. linux 0.12 各个章节笔记
3. 源码编译脚本及bochs启动运行脚本

```
Something I hope you know before go into the coding~
First, please watch or star this repo, I'll be more happy if you follow me.
Bug report, questions and discussion are welcome, you can post an issue or pull a request.
```

## 相关站点

* GitHub地址:<https://github.com/yifengyou/linux-0.12>

* GibBook地址:<https://yifengyou.gitbooks.io/linux-0-12/content/>

* 《Linux操作系统实现原理》资源:<http://oldlinux.org/Book-Lite/>

* 配套网站:<http://oldlinux.org/>

## 思维导图

![1530928925710.png](image/1530928925710.png)

![1530928941007.png](image/1530928941007.png)

![1530928957834.png](image/1530928957834.png)

![1530936626048.png](image/1530936626048.png)

![1530960311089.png](image/1530960311089.png)

## 一些个人看法

* 首先，读者如果是大佬，懂点Linux源码基础的可能会觉得这本书特么的废话注释真多~但身为菜鸡，读过一遍之后回过头来再看，个人觉得有些东西讲的细一点有好处，源码分析不能只讲理论，废话多的注释提供了很多信息，足够详细。但是缺点就是好比嚼烂了喂给你，你说恶心不恶心
* 因人而异吧，不少听到某某大佬直接间接批评国内内核书籍只是做注释，这本书，其实很到位，理论有了，注释有了。很适合菜鸡入门。大佬你就特么的闭嘴少说话，你要牛逼你也写一个。
* 读这本书需要掌握正确方法，论内核解析的正确打开姿势。首先，前面几章节基础，纯理论，必不可少的体系结构和基础汇编，如果掌握不了，或者看烦了，后面基本没啥玩头。如果你不知道体系结构，后面看的再透彻，你的瓶颈还是很明显的。反过来前面掌握透彻，后面，其实就是扩展补充
* 然后从第七章，第七章是个过渡，很重要的过渡，影响到你后面的阅读，第七章之前，引导程序和初始化程序有着很深刻的流程化节奏，你把握流程就ok了哟~
* 第八章开始，特么的就是一个一个文件的注释，谁看谁懵逼，谁看谁吐槽~四不四~
* 其实不然，你必须知道一点，内核其实就是一堆函数的集合，这对函数划分不同功能模块，但是内核要自举啊，自举肯定是流程化的，自举结束了呢？正常运行呗，然后接下来所有功能模块都只是在需要的时候调用，不需要的时候不去动，不过每个模块在使用之前都肯定要初始化，初始化干了些啥？无非就是占坑，预存一些数据结构，参数什么的，硬件呢就是设置寄存器，告诉硬件要工作在什么模式。。其实我个人感觉硬件最蛋疼，因为太规矩，你必须怎么滴怎么滴才能怎么滴。
* 画图理解 - 不画图学起来比较吃力~

## 总结

1. 基础永远值得花费90%的精力去学习加强。厚积而薄发~
2. 要理解一个软件系统的真正运行机制，一定要阅读其源代码~
