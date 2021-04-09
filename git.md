# git

查看当前配置

```
git config --list
```

设置默认编辑器

```
git config --global core.editor vi
```

组合成一个操作

```
git add 
git commit 
git commit -a
```

查看状态

```
git status
```

```
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

```
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   ubuntu-git.md

no changes added to commit (use "git add" and/or "git commit -a")
```

git add

```
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   ubuntu-git.md
```

git commit

```
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

git push origin master

```
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

精简的结果

```
$ git status -s
 M ZYNQ7000.md	# 被修改了 还没有被暂存
M  ubuntu-git.md	# 已经被暂存的新文件	
?? notes	#既没有暂存 也没有提交的新文件
```

忽略一个文件

```
vi .gitignore	# added .gitignore as shown below
cat .gitignore
git status -s
```

删除文件

```
git rm test.sh
git commit -m "deleting test.sh file"
git push origin master
```







