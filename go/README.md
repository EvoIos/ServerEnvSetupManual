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


3. 配置mod

1.13 版本之后，go引入了mod概念，不在依赖之前的目录结构src这种了。

创建mod

```bash
# xxx 代表文件夹名字
go init mod xxx 
```

## Tutorial 

### create source directory

进入到GOPATH目录下，创建一个source code文件夹

```bash
cd $GOPATH
mkdir hello
cd hello
```

### 创建mod 

> 在实际开发中，模块路径通常是保存源代码的存储库位置。例如，模块路径可能是 github.com/mymodule 。如果您打算发布您的模块供其他人使用，模块路径必须是 Go 工具可以从中下载您的模块的位置。有关使用模块路径命名模块的更多信息，请参阅[管理依赖项](https://golang.google.cn/doc/modules/managing-dependencies#naming_module)。

当前只需使用 example/hello 

```
go mod init example/hello
```

创建hello.go文件，输入如下内容：

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

运行

```bash
 go run .
```






