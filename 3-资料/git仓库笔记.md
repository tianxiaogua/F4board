# 学习使用Git指令同步仓库

参考的视频教程：https://www.bilibili.com/video/BV1Xx411m7kn?p=10

git下载地址：https://git-scm.com/download/win

## 一、同步库文件

1、初始化设置用户名字

```
git config --global user.name 'tianxiaohuahua'
```

2、初始化设置邮箱

```
git config --global user.name '2960229652@qq.com'

```

3、初始化仓库，完成创建本地仓库

```
git init
```

4、在 文件夹内修改增加文件后使用命令来查看库的状态

```
git status
```

此时得到的提示中红色的字表示还未同步



5、把文件添加到暂存区

```
git add a.txt
```

再次执行查看库状态命令得到了一个绿色的新文件提示。



6、把文件从暂存区域添加到库文件中。

```
git commit -m '添加测试文件'
```

## 二、文件的删除操作

删除本地文件直接使用rm命令。

删除Git中的文件时使用：

```
git rm -r 我的文件夹/
git rm a.txt
```

之后提交删除的操作：

```
git commit -m '测试删除'
```

注意这里的命令的单引号部分是对本次操作的注释。直接填写自己要添加的注释即可

## 三、把git仓库克隆到本地

```
git clone https://github.com/tianxiaohuahua/text.git
```

此时第一次登陆需要添加用户名和密码。之后既可以同步完成。

## 四、推送到远程仓库

```
git push
```