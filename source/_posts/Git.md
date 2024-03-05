---
title: Git
date: 2024-03-05 23:05:30
tags:
---
**【GeekHour】一小时Git教程**

[01.课程简介_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1HM411377j?p=1)


**Git 详细安装教程（详解 Git 安装过程的每一个步骤）**

[Git 详细安装教程（详解 Git 安装过程的每一个步骤）_mukes的博客-CSDN博客_git安装](https://blog.csdn.net/mukes/article/details/115693833)


**Git for Windows**

[Git for Windows](https://gitforwindows.org/)


# Git - （分布式 版本管理）

### Git 工作流程

一般工作流程如下：

  - 克隆 Git 资源作为工作目录。

  - 在克隆的资源上添加或修改文件。

  - 如果其他人修改了，你可以更新资源。

  - 在提交前查看修改。

  - 提交修改。

  - 在修改完成后，如果发现错误，可以撤回提交并再次修改并提交。

下图展示了 Git 的工作流程：

![image.png](https://flowus.cn/preview/57269fc1-9de4-425b-814b-8cfe7429a820)

## 操作 Git

  Git 界面

  ![image.png](https://flowus.cn/preview/dfccfdf0-062b-4177-ae3f-a87d59d6297c)

  ### 操作方式

    - 命令行（推荐）

    - 图形化界面（GUI）

    - IDE插件 （vscode）

  

  1. 输入 ($)git - v 

    查询版本

  2. 配置用户名和邮箱 (只用执行一次)

    1. `git config --global user.name "your name"`

    2. `git config --global user.email your email`

    3. 保存用户名和密码 （不用每次输入）：

      `git config --global credential.helper stroe`

    - global : 全局配置，所有仓库有效

    - system 系统配置，对所有用户生效

    - （local）

  3. 查询配置信息 : git config --global --list

## 新建版本库 - （创建版本）

  创建版本库： `git init`

  （克隆仓库 `git clone`）

  ![image.png](https://flowus.cn/preview/da2b292e-8aba-4bfd-9754-78998a9a8ca6)

## 命令行

  - ls - a 查询所有目录

  - （git clone + url）



### 区域

  1. 工作区

  2. 暂存区

    文件状态

    1. 未跟踪

    2. 未修改

    3. 已修改

    4. 已暂存

  3. 本地仓库

### 提交

  - `git status`  查询仓库状态

  - `git add` 添加文件到暂存区

  - `git commit`提交**暂存区**到本地仓库

    1. **`git commit -m"记录"`**

    2. **vim 编辑：i → 进入编辑 → esc + :wq 退出**

  - `git log (--online)` 查询提交记录 （简洁查看）

### 回退

  reset

    - soft  ：保存工作区和暂存区

    - hard ：都不保留

    - mixed ：保留工作区

  `git reset --soft +（版本号）`

  上一个版本 ： HEAD^

  `git reflog` : 查询操作日志

#### 差异

  git diff

  - --HEAD

  - --cached

  比较版本 ： **git diff 版本1 + 版本2**

  - HEAD~（^）[HEAD~2] + HEAD

#### 删除

  1. 删除后提交

  2. git rm 删除工作区和暂存区

#### 忽略

  忽略文件:

  - 自动生成文件

  - 中间文件

  - 运行生成文件

  - 敏感文件

  gitignore

  *.log

  ![image.png](https://flowus.cn/preview/5081b575-8282-4a60-81cc-7844e6a6e72a)

  ![image.png](https://flowus.cn/preview/eabe254b-a5e8-4f82-8a9b-e8cd599f41a7)

### gitee

  ### 创建ssh

  [Gitee配置SSH公钥_配置gitee公钥-CSDN博客](https://blog.csdn.net/m0_46267097/article/details/107468428)


### GUI

  **VScode**

  ![image.png](https://flowus.cn/preview/bbad85b8-6e09-47c1-b5ec-68cdc60a582e)

  ![image.png](https://flowus.cn/preview/4b544f89-c6f9-43ba-a6c6-d0e29bc7b7a4)

## 分支

  ### 操作

  `git branch` ：查看分支

  `git checkout` `（git switch）` ：切换分支

  `git branch -d` ： 删除分支



# 附表

提交与修改

|命令|说明|
|-|-|
|`git add`|添加文件到暂存区|
|`git status`|查看仓库当前的状态，显示有变更的文件。|
|`git diff`|比较文件的不同，即暂存区和工作区的差异。|
|`git commit`|提交暂存区到本地仓库。|
|`git reset`|回退版本。|
|`git rm`|将文件从暂存区和工作区中删除。|
|`git mv`|移动或重命名工作区文件。|
|`git checkout`|分支切换。|
|`git switch （Git 2.23 版本引入）`|更清晰地切换分支。|
|`git restore （Git 2.23 版本引入）`|恢复或撤销文件的更改。|

### 提交日志

|命令|说明|
|-|-|
|`git log`|查看历史提交记录|
|`git blame <file>`|以列表形式查看指定文件的历史修改记录|

### 远程操作

|命令|说明|
|-|-|
|`git remote`|远程仓库操作|
|`git fetch`|从远程获取代码库|
|`git pull`|下载远程代码并合并|
|`git push`|上传远程代码并合并|



