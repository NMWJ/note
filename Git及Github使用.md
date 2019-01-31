# Git使用及github简单使用教程
## 安装git (略)

## 简单命令
* 设置用户
git config --global user.name "Your name"
git config --global user.email "Your email"

---

* 初始化仓库
> git init

* 把文件添加到仓库
> git add Git及Github使用.txt

* 描述提交信息
> git commit -m "git使用教程"

* 查看仓库状态
> git status

* 查看修改内容
> git diff Git及Github使用.txt

* 查看历史记录
> git log
> git log --pretty=oneline
> git reflog

* 退回上一个版本
> git reset --hard HEAD^
> git reset --hard HEAD^2

cat
......


## Github使用命令
 * 创建本地ssh key
 > $ ssh-keygen -t rsa -b 4096 -C "email@email.com"
```
 Generating public/private rsa key pair.
 Enter file in which to save the key (/c/Users/ZKAH/.ssh/id_rsa): > > > /d/key/id_rsa
```
 * 设置密钥生成路径 /d/key/id_rsa
 ```
 Enter passphrase (empty for no passphrase):
 Enter same passphrase again:
 Your identification has been saved in /d/gitkey/id_rsa.
 Your public key has been saved in /d/gitkey/id_rsa.pub.
 The key fingerprint is:****
 he key's randomart image is:
 ```
```
+---[RSA 4096]----+
|      +-.=       |
+----[SHA256]-----+
```
* 验证是否成功
 > ssh -T git@github.com
 ```
 git@github.com: Permission denied (publickey).
 ```
 出现这种情况是因为更改了密钥默认生成路径
 切换回到密钥目录下
 > ssh-add id_rsa
 ```
 Could not open a connection to your authentication agent.
 ```
 运行命令 
 > eval $(ssh-agent -s)
 ```
 Agent pid 17140
 ```
 > 再次 ssh-add id_rsa
 > Enter passphrase for id_rsa:
 > Identity added: id_rsa (id_rsa)

至此，下面可进行git常规操作
 

* 设置用户和邮箱
> git config --global user.name "Your Name"
> git config --global user.email "youreamil@mail"

* 上传代码
> git remote add origin git@github.com:yourName/yourRepo.git




	
	
