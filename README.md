# myTest
just a test project 

# git初始化记录
## 本地初始化ssh rsa key
* cd ~/.ssh
* ssh-keygen -t rsa -C "githubmail@qq.com" -f "github_rsa"
* ssh-keygen -t rsa -C "giteemail@qq.com" -f "gitee_rsa"
* 会生成四个文件github_rsa github_rsa.pub gitee_rsa gitee_rsa.pub把生成的pub文件内容复制到github profile和gitee profile下面的ssh key上
## 创建配置文件区分不同的域名用不同的key
* 创建一个文件文件叫 config ,内容如下:
```
# gitee
Host gitee.com
HostName gitee.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/gitee_rsa

# github
Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/github_rsa
```

## 测试有没有成功
执行
ssh -T git@gitee.com
成功则返回
Hi xxx! You've successfully authenticated, but GITEE.COM does not provide shell access.

执行
ssh -T git@github.com
成功则返回
Hi xxx! You've successfully authenticated, but GitHub does not provide shell access.


## 初始化本地目录关联上github项目
* 在github上新建好项目
* 在本地目录上初始化工作 git init
* 加入远程目录git remote add origin git@github.com:yourgithubname/repo.git
* 把文件拉下来吧 git pull
* 切换到master分支吧 git checkout master
