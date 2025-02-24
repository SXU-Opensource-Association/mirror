# SXU-Mirror

本项目搜集整理搭建开源镜像站的相关信息，意在完成一份切实可行的项目策划书以向校方申请服务器等相关资源

## 项目背景

> 《中华人民共和国国民经济和社会发展第十四个五年规划和2035年远景目标纲要》,明确提出支持数字技术开源社区等创新联合体发展;国务院印发《“十四五”数字经济发展规划》,提出支持具有自主核心技术的开源社区、开源平台、开源项目发展,推动创新资源共建共享,促进创新模式开放化演进;工业和信息化部印发《“十四五”软件和信息技术服务业发展规划》,系统布局“十四五”开源生态发展。                	  																						                                                           --[中视时讯](https://www.thepaper.cn/user_5371878)

计算机行业的发展总是伴随着开源文化，从底层的GNU工具链到pytorch等深度学习框架，开源项目已成为技术生态的核心支柱；全球开发者通过GitHub等平台协作创新，形成了开放共享的技术生态。在教育领域，开源文化的影响也随处可见，国内诸多高校都有开源社团，比较知名的有北京大学的LCPU俱乐部，清华大学的tnua等等，这些社团不仅教会学生们很多开发技能，还和一些开源组织合作，共同开发一些项目。许多开源社团都部署了开源镜像站，为师生和许多开发者提供了高效资源支持，详情可参考[校园网联合镜像站](https://mirrors.cernet.edu.cn/)。

![徽标](image/README/huibiao.png)

## 什么是镜像站

镜像站（Mirror Site）是指对主站点（源站）内容进行完整复制的分布式服务器节点，其核心目标是通过**就近访问、负载均衡、容灾备份**提升用户体验和系统稳定性。常见于开源软件仓库（如Debian、Apache）、学术资源平台（如arXiv）、全球性网站（如Wikipedia）等场景。

据调查，我校校园网存在部分同学下载速度不满足需求，部分非计算机专业同学找不到需求软件的镜像资源等问题。

## 搭建镜像站的价值

* 为师生提供更快速的下载服务，提高开发效率。
  未办理校园卡的同学想下载大型软件耗费的流量非常大，非计算机专业同学可能会下载不可信资源到学校的服务器，而一个处于学校内网的镜像站可以完美解决这些问题。
* 提升学校知名度
  如果学校允许给与公网IP，mirrors.sxu.edu.cn,那么镜像站可以为全国开发者提供服务，这也是学校计算机学科强大的体现
* 为学校的开源社团提供更好的资源支持，让学生在实践中学习
  关于此项，可详见[开源文化中学习](./Opensource_study/DONTREADME.md)

## 如何搭建镜像站

搭建镜像站涉及很多方面，我们的基础目的是：搭建一个在限定预算内有较高性能并能提供相对完备服务的镜像站，同步常用软件，预留一定空间供其他同学申请特定镜像资源。

### 硬件层面

#### Plan A

向学校申请服务器、硬盘等资源，满足服务的基本配置要求。

需求大概为：

* 学校闲置服务器、替换的磁盘等等
* 预算
  我们需要调查其他学校搭建镜像站的配置，大概估算价格，供学校参考，该内容放在planA目录下

#### Plan B

社团大概还有6000团费，在这个预算内尽可能搭建起一个功能完备的镜像站，该项可供同学们自由发挥，最终选定一个最优解，被选中的贡献者获得$(6000 - 你的方案的预算) * 0.05$的奖金，满足镜像站服务的参考配置可以参考[Mirroring Howto · tuna/tunasync Wiki · GitHub](https://github.com/tuna/tunasync/wiki/Mirroring-Howto)，你给出方案的内容放在jumping/planB目录下

### 软件层面

该项主要包括操作系统的选取，需要镜像何种软件，如何同步，组磁盘阵列等等。这个部分主要涉及运维的知识，因为都是学生运维，没啥经验，肯定会碰到不少问题，只能不断折腾，内容有待完善。各位可以修正以下不严谨或不详细的内容，在./software 提出自己的方案，最好附上说明。

#### 操作系统

除了windows server，任何linux的主流发行版都可以作为镜像站的操作系统(用windows server 多少感觉有点抽象，没一家镜像站这么干的),比较主流的像Rocky、debian系列等等，要求是稳定、安全、易于维护。


