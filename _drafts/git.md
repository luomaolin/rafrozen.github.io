git add  <file>


如果是修改的文件
则git add  <file>

如果是删除的文件
则 git rm  <file>

git add CHANGE-LOG.txt

然后再commit确认这个文件。

git commit

然后是push 同步到服务器端，

git push origin master
其中master是分支名称。


 git diff  <file>

 比较某文件与最近提交节点的差异。

 注意：如果该文件已暂存，那么应该使用git diff –cached<file>
  

   git diff <hashcode> <hashcode>  <file>

   比较某文件在提交节点a，节点b的差异。

   技巧：如果省略后面一个hashcode，则默认表示与上一提交节点比较。（也可以利用^运算符）



同步到服务器前先需要将服务器代码同步到本地

命令： git pull

如果执行失败，就按照提示还原有冲突的文件，然后再次尝试同步。

命令：git checkout -- <有冲突的文件路径>


同步到服务器

命令： git push origin  <本地分支名>

如果执行失败，一般是没有将服务器代码同步到本地导致的，先执行上面的git pull命令。


