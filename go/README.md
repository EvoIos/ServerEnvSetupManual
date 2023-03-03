# GO 

## macOS ARM64

1. 下载go安装包

https://golang.google.cn/dl/

选择ARM64安装包下载然后安装。

2. 配置环境变量

在 ~/.zshrc 中加入如下内容

```
export GOPATH=$HOME/Desktop/go
export GOROOT=/usr/local/go
export PATH=$PATH:$GOPATH
export PATH=$PATH:$GOROOT/bin
```

GOPATH 设置go执行位置，当前时在Desktop/go文件夹下


