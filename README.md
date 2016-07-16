### 安装git工具。

[(http://code.google.com/p/msysgit/downloads/list)]http://code.google.com/p/msysgit/downloads/list


### 如果是Ubuntu
```bash
$ sudo apt-get install git git-core
```

### 打开git工具
```bash
$ git config --global user.name "liaobin429" 
$ git config --global user.email liaobin429@sina.com
$ ssh-keygen -t rsa -C "liaobin429@sina.com"
```

* 把秘钥id_rsd.pub 内容拷贝到 我的github下的ssh key中。
* 然后accept
```bash
$ ssh git@github.com
$ mkdir sysmgr
$ cd sysmgr
$ git init
$ touch README
$ git add *
$ git commit -a -m 'liaobin'
$ git remote add origin git@github.com:liaobin429/sysmgr.git //为远程Git更名为origin 
```

* 记得在github上建一个同名工程
```bash
$ git push -u origin master //推送此次修改$
```

* 在电脑中把文件拷贝到sysmgr中去。
```bash
git add * 
git commit -a
```

* 修改电脑中sysmgr .git目录下的COMMIT_EDITMSG文件，把要递交的所有文件前的#去掉,再次执行
```bash
git add *
git commit -a
git push origin master
```
