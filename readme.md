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
  + 'git add ./readme.md'
- 2,把代码放到仓库的房间中去
  + 'git commit -m "这是对这次添加东西的说明"' 
### 这是完成另一个功能后的版本
