## 设置环境变量
- [zsh与bash设置环境变量的不同点](https://blog.csdn.net/vshpper/article/details/41865269)
- 如上所示,比如,我现在要将/Users/zhaof/Userbin添加到环境变量PATH中,那么无论我添加到.bashrc,还是~/.bash_profile,或者是/etc/baserc,/etc/profile下,都会在重开终端时失效.正确的做法应该是将其添加到~/.zshrc中,zsh在开启时都会首先去读取其中的配置.
