# myTest
just a test project 

# git初始化记录
## 本地初始化ssh rsa key
* ssh-keygen -t rsa -C "github注册邮箱地址"
* 把生成的pubkey复制到github profile下面的ssh key上
## 初始化本地目录关联上github项目
* 在github上新建好项目
* 在本地目录上初始化工作 git init
* 加入远程目录git remote add origin git@github.com:yourgithubname/repo.git
* 把文件拉下来吧 git pull
* 切换到master分支吧 git checkout master
