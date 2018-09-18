## 1.安装软件列表
- 安装docker
- 安装docker-compose
- 安装docker-machine
- 安装virtualBox
    
    #### 1-1 docker
    - 1.卸载旧版本docker: sudo apt-get remove docker docker-engine docker.io (全新安装时，无需执行该步骤)
    - 2.更新系统软件: sudo apt-get update
    - 3.安装依赖包: sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
    - 4.添加官方密钥: curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
        - 执行该命令时，如遇到长时间没有响应说明网络连接不到docker网站，需要使用代-理进行。
        - 显示OK,表示添加成功.
    - 5.添加仓库: sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    - 6.再次更新软件: sudo apt-get update (经实践，这一步不能够省略，我们需要再次把软件更新到最新，否则下一步有可能会报错)
    - 7.安装docker
        - 以下命令没有指定版本，默认就会安装最新版
        - $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
        - $ sudo apt-get install docker-ce
        - 如果想指定安装某一版本，可使用 sudo apt-get install docker-ce=<VERSION> 命令，把<VERSION>替换为具体版本即可。
    - 8.查看docker版本: docker -v
        - 显示“Docker version 17.09.0-ce, build afdb6d4”字样，表示安装成功。
    
    #### 1-2 docker-compose
    #### 1-3 docker-machine
    #### 1-4 virtualBox

## 2.
