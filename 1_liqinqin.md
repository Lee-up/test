##github学习总结
###配置git
1.在本地创建ssh key

    ssh-keygen -t rsa -C "your_email@youremail.com"

> 作用：在电脑上获得一个密钥，将密钥输入github之后，电脑就和github账号联系起来了，可以通过git bush随时上传代码

2.将所得密钥添加到github的SSH keys中

3.验证是否成功

    ssh -T git@github.com

4.提交代码之前要设置username和email，因为github每次commit都会记录他们

    git config --global user.name "your name"  
    git config --global user.email "your_email@youremail.com"

5.本地仓库基本操作

    （1）git init 

> 初始化，将项目建立为git管理的仓库

    （2）git add <filename>

> 作用：将文件添加到暂存区，临时保存改动

    （3）git commit -m "备注信息" 

> 作用：指向最后一次提交的结果

    （4）git push origin master

> 作用：将改动提交到远程仓库  
> master可以换成任何想要推送的分支

#### 提交代码

1.若要从头开始一个项目，可以将github的库克隆到本地电脑中，使之同步，再操作git

    git clone http://~~ 

> 网址就是创建库成功之后的网址

2.若要将一个已有的项目提交，可以将本地仓库与github的仓库进行关联，使之同步，再操作git

    git remote add origin git@github.com:yourName/yourRepo.git

> origin git@github.com:yourName/yourRepo.git为远程仓库的地址

3.用git push origin master提交代码

- 若本地库与github库的内容不同，push的时候会产生冲突，需要先将远程代码库中的文件先pull到本地代码库中，才能push新的代码到github代码库中  

    git pull --rebase origin master

##学习计划

1.继续学习git版本回退，管理和撤销修改，删除文件等操作

2.根据群里所给建议在完成每次任务的前提下继续巩固html和css，把一些模糊的概念搞清楚

3.建立自己的知识体系，将以前所学的零散的知识串起来