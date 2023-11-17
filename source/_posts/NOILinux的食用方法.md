---
title: NOILinux的食用方法-基础篇
date: 2023-10-3 23:42
---

当当当，应[@q1uple](https://www.luogu.com.cn/user/539133)的提议，这里火速赶出了一篇*NOI Linux*的食用方法，包含了我在网上根本没搜到的内容。

现在只打算写基础篇，后面再补。

<!--more-->

# 基础篇

这个基础篇主要是教大家如何去“*NOI Linux*，启动！”和使用图形化界面进行编程和调试。

笔者在*CSP/J 2022*赛场上用*NOI Linux*打过全部题目，所以里面会有其他文章不会讲到的考试时的情形。

## *NOI Linux*，启动！

首先我们需要知道如何启动*NOI Linux*，看起来很简单是吧？确实。

> 注：笔者在这里花费了大量时间搭建考试环境，就是为了给你们截几张图。其实笔者之前搭建过一个环境，但是使用的软件是*Hyper-v*，而考场用的是*VMware Workstation Player*，所以需要重新搭建环境。

### 在家食用

什么，你在机房？这玩意至少要弄一个小时，如果非要弄，直接跳到下一节就行。

通过*VMware Workstation Player*安装是最接近考场环境的安装方式。

#### 安装*VMware Workstation Player*

笔者在*CSP/J 2022*赛场上用的就是*VMware Workstation Player*，至于版本忘记了，不过各种版本操作方式没有太大区别，这里就使用最新版进行演示。

你可以在*bing*里搜索`VMware Workstation Player`，找到官网的链接，懒人可以用这个[VMware Workstation Player | VMware | CN](https://www.vmware.com/cn/products/workstation-player.html)

然后点击下载

![image-20231003210044823](./NOILinux的食用方法/image-20231003210044823.png)

![image-20231003215256816](./NOILinux的食用方法/image-20231003215256816.png)

![image-20231003215706142](./NOILinux的食用方法/image-20231003215706142.png)

> 这里使用17，你也可以下载16，区别不大。

下载好后直接打开，你就可以看到安装界面了。

![image-20231003220617037](./NOILinux的食用方法/image-20231003220617037.png)

一路点击下一步即可。

然后打开它，得到这个界面。直接点击继续

![image-20231003220936228](./NOILinux的食用方法/image-20231003220936228.png)

弄好后是酱紫

![image-20231003221002656](./NOILinux的食用方法/image-20231003221002656.png)

#### 安装*NOI Linux*

然后我们还需要下载*NOI Linux*。

打开NOI的帖子，[NOI Linux 2.0发布，将于9月1日起正式启用！](https://www.noi.cn/gynoi/jsgz/2021-07-16/732450.shtml)

![image-20231003221247402](./NOILinux的食用方法/image-20231003221247402.png)

然后下载好后，得到一个3.38GB的ubuntu-noi-v2.0.iso

回到VMware，创建新虚拟机

![image-20231003221033950](./NOILinux的食用方法/image-20231003221033950.png)

注意，这一步**不能直接使用iso安装**

> 这里安装会使用*VMware*的简易安装功能，这会极大地影响到我们的安装，导致环境配置不成功（亲测）

![image-20231003221646414](./NOILinux的食用方法/image-20231003221646414.png)

![image-20231003221719880](./NOILinux的食用方法/image-20231003221719880.png)

![image-20231003221904805](./NOILinux的食用方法/image-20231003221904805.png)

然后根据自己需要选择硬盘大小，建议40GB（不会一次性占满，随着使用量的增大而增大）

注意到了最后一步要**关闭网络**。

内存和处理器根据需要调整，默认的就够用。

![image-20231003222208846](./NOILinux的食用方法/image-20231003222208846.png)

还要插入我们刚刚下载好的iso文件

![image-20231003222318257](./NOILinux的食用方法/image-20231003222318257.png)

![](./NOILinux的食用方法/image-20231003222059979.png)

![image-20231003222415894](./NOILinux的食用方法/image-20231003222415894.png)

等待一段时间，切莫着急（或者你可以跳过检查）

![image-20231003222544519](./NOILinux的食用方法/image-20231003222544519.png)

然后进入*Ubuntu unity*桌面（会有清脆的开机声）

> 考场上的*NOI Linux*用的也是中文

![](./NOILinux的食用方法/image-20231003222735891.png)

**不要安装*VMware tools***，因为还没安装好系统

![image-20231003222908480](./NOILinux的食用方法/image-20231003222908480.png)

一路继续即可

这里可以填入你想要的内容（但是**不要用中文**！！！）

你按小键盘的时候可能没反应，你只需要点一下小键盘左上角的NumLock按键

![image-20231003223005213](./NOILinux的食用方法/image-20231003223005213.png)

然后等待漫长的安装即可

![image-20231003223336616](./NOILinux的食用方法/image-20231003223336616.png)

![image-20231003223949564](./NOILinux的食用方法/image-20231003223949564.png)

![image-20231003224016380](./NOILinux的食用方法/image-20231003224016380.png)

这里，我们需要弹出光盘

![image-20231003224137897](./NOILinux的食用方法/image-20231003224137897.png)

![image-20231003224211641](./NOILinux的食用方法/image-20231003224211641.png)

然后愉快的按下回车键~

等待一段时间，我们的*NOI Linux*就启动乐

![image-20231003224323485](./NOILinux的食用方法/image-20231003224323485.png)

如果输入密码没反应，同理，按下NumLock。

然后就可以安装*VMware tools*了

![image-20231003224518896](./NOILinux的食用方法/image-20231003224518896.png)

解压到一个你喜欢的地方

![image-20231003225055711](./NOILinux的食用方法/image-20231003225055711.png)



![image-20231003225156436](./NOILinux的食用方法/image-20231003225156436.png)

输入指令`sudo ./vmware-install.pl`，然后输入密码，这个是没有显示的，输完了直接回车即可

然后再输入`yes`，不管他问啥，一路回车即可。

![image-20231003225751743](./NOILinux的食用方法/image-20231003225751743.png)

安装好了直接重启

![image-20231003225900493](./NOILinux的食用方法/image-20231003225900493.png)

![image-20231003232834509](./NOILinux的食用方法/image-20231003232834509.png)

至此，你的*NOI Linux*就安装好了。

### 机房食用

如果你的电脑上有预装的话，直接打开就能用。解决没有预装的难题的话就要麻烦许多。

这里使用*Portable-VirtualBox*将你的*NOI Linux*安装在U盘上。注意：建议使用高速U盘或移动硬盘，否则将会非常折磨（以至于无法使用）。

#### 安装*Portable-VirtualBox*

进入官网[Portable-VirtualBox - Portable-VirtualBox (vbox.me)](https://www.vbox.me/)

进行下载

![image-20231004153608364](./NOILinux的食用方法/image-20231004153608364.png)

下载好后解压到你的U盘

打开软件，选择语言

![image-20231004153856701](./NOILinux的食用方法/image-20231004153856701.png)

![image-20231004153925985](./NOILinux的食用方法/image-20231004153925985.png)

![image-20231004154434585](./NOILinux的食用方法/image-20231004154434585.png)

等待下载完成

![image-20231004154743372](./NOILinux的食用方法/image-20231004154743372.png)

等待文件提取完成，窗口会自动关闭。

找到主程序打开即可。

其它的和上面的使用*VMware Workstation Player*差不多，我就不做步骤了（主要是我开了hyper-v，没法弄）

![image-20231004155622069](./NOILinux的食用方法/image-20231004155622069.png)

