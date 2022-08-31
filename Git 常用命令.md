#### Git 常用命令
##### 1、Git 全局设置

&emsp;&emsp;当安装Git后首先要做的事情就是设置用户名和email地址。这是非常重要的，因为每次提交都会使用该用户信息。



##### 1. 1	设置用户信息
```
git config --global user.name "username"
git config --global user.email "name@163.com"
注意：上面设置的user.name和user.email可以任意设置
```
	
##### 1. 2	查看配置信息
```
git config --list
```

#### 2、获取 Git 仓库

&emsp;&emsp;要使用Git对我们的代码进行版本控制，首先需要获得Git仓库

##### 2. 1	获取 Git 仓库的两种方式
###### 2. 1. 1	在本地初始化一个Git仓库（不常用）
执行步骤如下：

```
1、在任意目录下创建一个空目录（例如repo1）作为我们本地仓库
2、进入这个目录中，点击鼠标右键打开Git bash窗口
3、执行命令 ：git init
```

    
&emsp;&emsp;如果在当前目录中看到.git文件夹（此文件夹为隐藏文件）则说明Git仓库创建成功
 

###### 2. 1. 2	获取 Git 仓库 - 从远程仓库克隆（常用）
&emsp;&emsp;可以通过 Git 提供的命令从远程仓库进行克隆，将远程仓库克隆到本地

    执行命令：git clone https://gitee.com/chenhengfeng/test01.git

#### 3、工作区、暂存区、版本库 概念

&emsp;&emsp;**版本库：** 前面看到的 .git 隐藏文件夹就是版本库，版本库中存储了很多配置信息、日志信息和文件版本信息等

&emsp;&emsp;**工作区：** 包含 .git 文件夹的目录就是工作区，也称为工作目录，主要用于存放开发的代码

&emsp;&emsp;**暂存区：** .git 文件夹中有很多文件，其中有一个 index 文件就是暂存区，也可以叫做 stage。暂存区是一个临时保存修改文件的地方


```
graph LR
A[工作区]-->|添加选择的改变|B[暂存区]
A-->|git add|B

B-->|提交改变|C[版本库]
B-->|git commit|C

```

<img src="https://raw.githubusercontent.com/chenHengFeng0/picture/main/img/tooopen_sy_14410241242717.jpg">



<img src="https://raw.githubusercontent.com/chenHengFeng0/picture/main/img/tooopen_sy_14410241242717.jpg">



<img src="http://note.youdao.com/noteshare?id=f34ef5295d63e9a1676978ce1f79842a&sub=B6491A741BC84C97B34CBEC7F53481E4">

<img src="https://note.youdao.com/yws/api/personal/file/8D775764C6A4433C90A856801003DEC4?method=download&shareKey=a1b9422382aa8bd906bf8039acd5d142">


<img src="http://note.youdao.com/noteshare?id=9ffd3aa11593e874ed5517d9db4b0c03&sub=9AF133A3B7B04CBD9E4B7708431E3158">


远程仓库操作：
git remote  查看远程仓库
git remote add 