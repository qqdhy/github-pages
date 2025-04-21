## du -sh
显示目录大小
* -s 显示摘要
* -h 可读模式
```shell
du -sh 
du -sh directory
```

## Delete A  Folder and Sub-content
```shell
rm -rf folder
```
## ls 
### ls | wc -l
显示文件数量
```shell
ls | wc -l
ls *.livp | wc -l
```
### ls -R | grep '.md\\|.jpg'
查找所有子目录中特定类型的文件
```shell
ls -R | grep '.md\|.jpg'
```

## List File Size Readable Format
```shell
ls -hl file
```

## Open an Image in Shell
```shell
open file.jpg
```

## Open an Folder in Finder
```shell
open folder
```

## Unzip livp
```shell
for i in *.livp; do unzip $i; done
```

## Move 100 Files
There are thousands files in a folder. I want to move 100 any files to another folder.
```shell
mv -- *([1,100]) /other/location/
```



## Reference

[Linux教程](https://www.runoob.com/linux/linux-tutorial.html)

[Shell教程](https://www.runoob.com/linux/linux-shell.html)

