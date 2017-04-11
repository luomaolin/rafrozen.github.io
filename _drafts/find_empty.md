linux下批量删除空文件（大小等于0的文件）的方法
```
find . -name "*" -type f -size 0c | xargs -n 1 rm -f
```
就是删除1k大小的文件。（但注意不要用 -size 1k，这个得到的是占用空间1k，不是文件大小1k的）。
```
find . -name "*" -type f -size 1024c | xargs -n 1 rm -f
```
查询出所有的空文件夹
```
find -type d -empty
```
