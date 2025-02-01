# 1. github仓库同步到本地
按顺序执行以下指令：
```
git init
git remote add origin git@github.com:Calidvwich/Notes.git
```
# 2. ssh密钥的生成和使用
```
powershell中运行：ssh-keygen -t rsa -b 4096 -C "your-email@example.com"（github邮箱）
Enter file in which to save the key (/c/Users/Lenovo/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
cat ~/.ssh/id_rsa.pub
Get-Content $env:USERPROFILE\.ssh\id_rsa.pub
```
此时理论上会生成ssh-rsa开头字符串，登录github后进入new ssh key页面添加即可
运行以下指令进行测试：
```
ssh -T git@github.com
```
成功时会出现：
```
Hi Calidvwich! You've successfully authenticated, but GitHub does not provide shell access.
```
# 3. 在仓库同步建立以后的操作
在对应文件夹打开powershell后，运行：
```
git add .
git commit -m "(reason)"
git push -u origin master
```
# 4. 用户名和用户邮箱签名的自定义
```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```