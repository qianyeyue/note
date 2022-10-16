#                      git 笔记

[TOC]

#### 1.创建并连接github，传输文件到github

1.创建github账户，创建git账户，创建密钥

2.在要上传的文件夹里用git bash here 

然后git add .（是需要添加所有文件）git add 后面可以加文件名表示添加具体文件

然后输`git commit`命令，`-m`后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录

比如git commit -m "pictures"

这样原来文件夹里就会有一个.git的文件

这些工作是为了创建一个.git的文件夹并将之前文件夹里的所有东西放到.git的文件夹里面

3.然后git remote add origin git@github.com:qianyeyue/pictures.git

这里origin后面是你创建的新的GitHub账户里的文件夹的地址

然后用git push -u origin master就可以传输.git文件里的内容到GitHub里面的文件夹了

#### 2.修改文件 看文件的修改 以及文件修改后的上传

1.git status 可以看文件的状态比如是否有修改（在未将文件上传前）

2.修改后可以用git diff看文件的具体修改内容，呈现形式比如

+learning （也就是添加了learning）

3.然后再用git add .提交所有文件（或者具体文件）

4.然后用git commit -m "（名称）"

5.然后用git push -m origin master就完成上传了

#### 3.查看历史记录并回退版本

1.在Git中，我们用`git log`命令查看历史记录

2.回退到上一个版本：在Git中，用`HEAD`表示当前版本，也就是最新的提交，上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，当然往上100个版本写100个`^`比较容易数不过来，所以写成`HEAD~100`。

比如git reset --hard HEAD^ 这是将你文件里的内容回退到上一个版本，而不是你上传的内容

又git reset --hard （id名称）就可以回退到当时是该id名称的文件

3.git reflog可以查看命令历史，以便确定要回到未来的哪个版本。

#### 4.理解git add以及git commit

1.git add 是将你的修改放进一个暂存区，然后git commit是将暂存区的修改提交到.git文件里面

2.git 跟踪的是修改过程而不是整个文件

#### 5.撤销修改

1.Git会告诉你，`git checkout -- file`可以丢弃工作区的修改：

2.命令`git checkout -- readme.txt`（文件名称）意思就是，把`readme.txt`文件在工作区的修改全部撤销，这里有两种情况：

一种是`readme.txt`自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是`readme.txt`已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次`git commit`或`git add`时的状态

#### 6.删除文件

1.用`rm`命令删除文件比如rm test.txt

2.若误删，则用git checkout -- test.txt可以恢复文件，因为版本库（也就是.git这个文件夹）里面有你上传的文件

3.若没有误删，同时要把版本库里面的文件也删除，则用git rm test.txt

4.然后用git commit -m "（名称）"

5.最后加上git push origin master那么GitHub里面文件就没了

