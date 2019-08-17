# Git资料

## 从远程服务器上获取到的工程，用Git没问题，而TortoiseGit报错：
**<font color="red" size="4">Disconnected: No supported authentication methods available(server sent: publickey)</font>**

> 解决方法：
01. TortoiseGit -> Settings -> Network
02. 将SSH client设置成 Git\bin\usr\ssh.exe


## TortoiseGit状态图标不能显示解决方法：
这种问题可能是因为：TortoiseGit版本问题，与其他软件（如svn）冲突问题。
> 方法一：
01. 快捷打开运行窗口win+R，输入regedit.exe，打开注册表；
02. 按照文件的层次关系依次找到：HKEY_LOCAL_MACHINE\Software\Microsoft\windows\CurrentVersion\Explorer，修改键名 Max Cached Icons(最大缓存图标)的值为2000（没有这个键，可以新建）；
03. 重启电脑。

> 方法二：
01. 快捷打开运行窗口win+R，输入regedit.exe，打开注册表；
02. 找到：HKEY_LOCAL_MACHINE–>SOFTWARE–>Microsoft–>Windows–>CurrentVersion–>Explorer–>ShellIconOverlayIdentifiers，将Tortoise相关的项都提到靠前的位置（重命名，在名称之前加几个空格）（Windows会使用掉4项默认排序，另外还有11项是供应用程序配置的，如果排在11项之后，可能导致应用程序的配置无效）；
03. 排到靠前位置后，重启资源管理器即可（任务管理器-->资源管理器（重新启动））。


## Git通过SSH克隆项目：

> 配置步骤：
01. 在git bash中输入指令，生成RSA密钥：ssh-keygen -t rsa -C "你注册Git的邮箱"，执行指令时，可以什么不输入，一直回车即可；
02. 在C盘-->用户目录下找到.ssh目录，我的是：C:\Users\Administrator.PC-20160717PPEI\.ssh，打开该目录下的id_rsa.pub文件，复制里面的全部内容；
03. 打开你的GitHub官网，在Settings中点击SSH and GPG keys，在跳出的界面中选择New SSH key，在弹出框中输入title，另一个大框粘贴刚刚复制的内容，点击确定即可。




---
***

# 这是一级标题

## 这是二级标题

### 这是三级标题

#### 这是四级标题

##### 这是五级标题

###### 这是六级标题

这是一级标题
= 
这是二级标题
- 

# 这是一级标题 #

## 这是二级标题 ##

### 这是三级标题 ###

#### 这是四级标题 ####

##### 这是五级标题 #####

###### 这是六级标题 ######

* **这是加粗的文字**
* *这是倾斜的文字*`
* ***这是斜体加粗的文字***
* ~~这是加删除线的文字~~

* 不以结婚为目的谈恋爱，都是耍牛氓！

  > - 这是一级引用的内容
  > - 这是一级引用的内容
- 
+ 

>> 这是二级引用的内容

- 
+ 

>>> 这是三级引用的内容

- 
* 

* 一级无序列表内容

   * 二级无序列表内容
   * 二级无序列表内容
   * 二级无序列表内容

* 一级无序列表内容

   1. 二级无序列表内容
   2. 二级无序列表内容
   3. 二级无序列表内容
   4. 二级无序列表内容
   5. 二级无序列表内容

| 表头 | 表头 | 表头 |
| :- | :-: | -: |
|第一行|第一行|第一行|
|第二行|第二行|第二行|
|第三行|第三行|第三行|

`代码内容` 

``` 
代码内容
```

![图片alt](https://www.baidu.com/img/baidu_jgylogo3.gif)

