## Git安装
## 初始化Git仓储(仓库-在当前项目目录打开的文件夹右键选 git bash)
- 这个仓库会存放git对我们项目代码进行备份的文件
- 命令:git init

## 自报家门,用于判断当前谁操作了当前项目
- 就是在git中设置当前使用的用户是谁
- 每一次备份都会把当前备份者的信息存储起来
- 命令:
  + 配置用户名:'git config --global user.name "lgc"'
  + 配置邮箱:'git config --global user.email "xxx@qq.com'
## 把代码存储到.git仓库中
- 1,把代码放到仓库的门口
  + 'git add ./readme.md' 把指定的文件放到大门口
  + 'git add ./' 把所有修改过的文件全部添加到大门口
- 2,把代码放到仓库的房间中去
  + 'git commit -m "这是对这次添加东西的说明"' 

## 可以一次性的把我们修改后的代码放到房间里(版本库)
- 'git commit --all -m "一次性把修改后的文件放到房间里去,直接跳过先放到大门口的操作"'
   + --all代表把所有修改过的文件提交到版本库

## 查看当前状态
- 可以用来查看当前代码有没有添加到仓库中去
- 命令: 'git status'

## 查看日志
  - 'git log' 查看历史提交的日志
  -  'git log --oneline' 可以看到简洁版的日志
## 回退到指定版本
  - 'git reset --hard Head~0'
    + 表示回退到上一次代码提交时的状态
  - 'git reset --hard Head~1'
    + 表示回退到上上次代码提交时报状态
  - 依次类推
  - 'git reset --hard [版本号]'
    + 可以通过版本号精确的回退到某一次提交时的状态
  - 'git reflog'
   + 可以看到每一次切换版本的记录
    + 可以看到每一次切换版本的记录

## 分支
- 默认是有一个master主分支
  
### 创建分支
  -  'git branch dev'
     + 创建一个名为dev的分支
     + 在刚创建时dev分支里的东西和master分支里的东西是一样的

### 切换分支 
 - 'git checkout dev'
     + 切换到指定的分支,这里的切换到名为dev的分支上
     +  'git branch' 可以查看当前有哪些分支 

### 合并分支
  - 'git merge dev'
      + 合并分支内容,把当前的分支与指定的分支(dev),进行合并
      + 当前分支指的是  'git branch' 命令输出的前面带 * 号的 分支 
  - 合并时如果有冲突,需要手动去处理,处理后还需要提交一次

### GitHub
 - https:github.com
 - 不是git,只是一个网站
 - 只不过这个网站提供了允许别人通过git上传代码的功能


### 提交代码到github(当作git服务器来使用)
 - 'git push [地址] master'
 - 示例: 'git push https://github.com/liguochao1120/test01.git master'
 - 会把当前分支的内容上传到远程master分支上

### 把代码 pull到本地
 - 'git init'
 - 'git pull [地址] master'  
 - 'git clone [地址]' master 不推荐使用
### 使用push 和 pull时,先pull再push

# 流行框架

## 通过ssh方式上传代码

 - 公钥 和私钥,这两者是有关联的
 - 生成公钥和私钥
     + 'ssh-keygen' -t rsa -C "740227782@qq.com"
     + 'git push [ssh地址] master'
### 将远程地址修改为一个变量,方便使用，
 - 'git remote add origin [地址]'
 - 'git push origin master'




