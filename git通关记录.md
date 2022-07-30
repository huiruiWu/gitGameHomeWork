## 第一关

``Level 1`` Your first task is to checkout the commit whose commit message is the answer to this question:  > When a programmer is born, what is the first thing he/she learns to say?



**使用git log查看提交历史，看到Hello World**

**git checkout 到Hello World分支**



## 第二关

``Level 2`` We want to get to a branch whose name is the answer to this riddle:  I am a creature that is smaller than man, but many times more in number.  In code, my appearance can be subtle and no matter where I am found, I am unwanted.  What am I?



git branch -a所有分支，根据问题得出答案是bug

git checkout到对应bug分支



## 第三关

``Level 3``

Sometimes we like to blame others for introducing bugs in our code. 
Think you can find out who introduced a bug into our file cool.cpp? 
We think he had something to do with the development of git.
And from what we hear he also made a branch under his name.
Checkout to that branch after you find out who the culprit is. 



**使用git blame cool.cpp查看改文件被谁改动过。发现改动者为LinusTorvalds2014**

**git checkout 切换到LinusTorvalds2014的分支**



## 第四关

``Level 4``

The next clue you are looking for --
   is in a file you choose to ignore!



**让我查看gitignore，直接打开gitignore文件夹**



## 第五关

``Level 5``



**猜谜，答案是tree。**

**git checkout tree**



## 第六关

Welcome to the "tree" branch. 
Looks like good ol' Linus modified the "nextclue_input.cpp" file. 
Normally, when ran with the shell script "outputclue.sh", the "nextclue_input.cpp" file would give us the next hint.

Maybe, you should try running the shell script with the "nextclue_input.cpp" file and see what happens...



运行shell脚本

```
./outputclue.sh nextclue_input.cpp
```



## 第七关

```
Linus has been here...
I love messing with these amateur programmers!!
If you want some real fun, then you should try resolving a conflict between this branch (tree) and code4life.
I introduced a little bug that you should fix in the conflict. >:)
After you merge these 2 files you should run the shell script again!!
 
Good Luck!!!
```



**冲突文件解决完之后再次运行命令**



## 第八关

``Level 8``

Looks like you resolved your conflict and found our branch, congrats!! 

Hmm...it seems this branch has a file that was seen before in another branch. 
Do you "remember" what it is?
I think this file has something to do with the next clue, but it seems to be very ugly looking. 
Maybe if we compare the "diff"erences between this file and the file from before we'll know where to go next...



**用git diff找两次提交的不同之处**

**找到了个分支名Henry**



## 第九关

上一关找到个Henry的分支名，切换过去发现并没作用

其实是分支名与标签名重名了，切换过去的其实只是标签，因此需要删除该标签

**git tag -d Henry**



## 第十关

```
Welcome!! It looks like you made it to my Branch!!!
Generally you want to refrain from making tags the same name as branches, unless you have a good reason.
The tag is more like the stable release.
While the branch is more like the in progress feature, which will be added soon.

You're almost done!! Excited?? Hope you are! You have one more thing to do!

Now its time to update the master branch, updating is really useful when you fork a repository and your forked repo starts to get behind on commits. The repository to update from is: https://github.com/drami025/git-game.git

Don't cheat!!
```

添加远程仓库

**git remote add levelTen git@github.com:drami025/git-game.git**

**git pull levelTen master**

