# GIT的使用

## 文件状态
可以通过git status来查看文件的状态

1. 未跟踪

    未跟踪指文件没有被git所管理<br>
        `刚刚新建的文件就是这个状态`

2.  已跟踪

    已跟踪指文件已经被git所管理 
      1. 未修改

            表示磁盘中的文件和git仓库中文件相同，没有修改。

      2. 已修改

            表示磁盘中文件已被修改，和git仓库中文件不同。

      3. 已暂存
            表示文件修改已经保存，但是尚未提交到git仓库中。
            
      

未跟踪->暂存<br>
git add <文件名称><br>
git add . 添加所有文件<br>
```
这个命令会将当前目录以及其子目录中的所有更改（新文件、修改过的文件和删除的文件）添加到暂存区。
它会包括所有的更改，包括隐藏文件和目录（以.开头的文件或目录）。
这个命令是递归的，会处理当前目录下的所有内容。
```
git add * 添加所有文件<br>
    
```
它会添加当前目录下的所有更改，但不包括以.开头的隐藏文件和目录。
它不会递归添加子目录中的更改，除非子目录中的文件和目录也匹配通配符
如果你有一个命名为file.txt的文件和一个名为.hidden-file.txt的隐藏文件，git add * 会添加file.txt但不会添加.hidden-file.txt。
```
<br>
暂存->未修改<br>
git commit -m "提交信息"
<br>
未修改->已修改<br>
修改文件

提交所有已修改的文件<br>
git commit -a -m "提交信息"<br>
👆这条只会提交已经跟踪过的文件，不会影响未跟踪的文件<br>

