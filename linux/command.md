# linux命令行

## 1.解压与压缩相关

### 1-1 zip包
 - 解压 a.zip : unzip a.zip
 - 将当前目录下的所有文件和文件夹全部压缩成a.zip文件:zip -r myfile.zip ./*     (－r表示递归压缩子目录下所有文件)
 - 压缩处理多个文件和目录,方法为逐一列出，并用空格间隔:zip -r filename.zip file1 file2 file3 /usr/work/school
 
 
 
## 2.系统相关
  - 查看所有环境变量: env 
  - 查看单个环境变量: echo $PATH
