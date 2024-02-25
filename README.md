# golings

[![build and test](https://github.com/mauricioabreu/golings/actions/workflows/test.yml/badge.svg)](https://github.com/mauricioabreu/golings/actions/workflows/test.yml)


![gopher](misc/gopher-dance.gif)


 **其他语言版本: [English](README_en.md), [中文](README.md)**


`golings` 是一个针对 [Go 编程语言](https://go.dev/) 的 CLI 应用程序，旨在通过练习教授Go编程语言

设置完运行`golings`所需的所有工具后，您的任务是修复小型 go 程序代码

## 安装

首先，您需要安装gosdk。您可以通过访问[Go下载页面](https://golang.google.cn/dl/)来安装它,选择最新稳定版本下载安装，以下列出一些官方链接

* [当前最新windows平台64位](https://golang.google.cn/dl/go1.21.7.windows-amd64.zip)
* [当前最新linux平台64位](https://golang.google.cn/dl/go1.21.7.linux-amd64.tar.gz)


然后有两种方法安装 golings

### Go命令安装golings

```sh
go install github.com/liumingmin/golings/golings@latest
```

如果您想在命令行中的任何路径下运行 golings，请将 `go/bin` 添加到您的 PATH 中。来自官方文档：

> 安装目录由 GOPATH 和 GOBIN 环境变量控制。如果设置了 GOBIN，二进制文件将安装到该目录。如果设置了 GOPATH，则二进制文件将安装到 GOPATH 列表中第一个目录的 bin 子目录中。否则，二进制文件将安装到默认 GOPATH 的 bin 子目录（$HOME/go 或 %USERPROFILE%\go）

### 二进制包安装

转到 [发布页面](https://github.com/liumingmin/golings/releases) 并选择最适合您环境的选项,将二进制包放到PATH能够访问的目录下

### 开发环境容器

1. 安装 Docker/Podman 和 VSCode 并配置
1. 克隆存储库并在 VSCode 中打开它。
1. 系统将提示您在开发容器中重新打开代码。该容器预先配置了 go 以及调试 go 代码所需的所有工具。
1. 打开一个新的嵌入式终端并运行 `golings watch` 开始练习。

## 完成练习

所有练习都可以在目录 `golings/exercises/<topic>` 中找到。对于每个主题，都有一个附加的自述文件，其中包含一些资源，可帮助您开始了解该主题。我们强烈建议您在开始之前先看一下它们。


现在您的任务是修复所有程序。其中一些无法编译，您需要修复它们。其中一些可以编译，但需要测试，您需要编写一些代码才能使它们执行测试结果全部绿色（这些是`compile`和`test`模式）。

克隆代码仓库:

```sh
git clone https://github.com/liumingmin/golings.git
```

请使用 watch 命令,按照建议的顺序运行练习, 命令将会快速判断您的结果并给予反馈

```sh
golings watch
```

该命令将以交互模式运行 golings。每次保存文件时，它都会验证代码是否正确。

想要运行下一个待处理的练习:

```sh
golings run next
```

如果您想进行单个练习:

```sh
golings run variables1
```

如果您遇到困难并需要提示:

```sh
golings hint variables1
```

列出所有练习，同时检查您的进度:

```sh
golings list
```

编译并运行所有练习:

```sh
golings verify
```

如果您需要 CLI 命令的帮助:

```sh
golings --help
```

运行命令的演示 `golings run <exercise name>`

![demo](misc/demo.gif)

## 贡献练习题

[贡献练习题](./CONTRIBUTING.md)

## 学习资源

* [Golang官方教程](https://go.dev/doc/tutorial/)
* [Go案例](https://gobyexample.com)
* [Aprenda Go](https://www.youtube.com/playlist?list=PLCKpcjBB_VlBsxJ9IseNxFllf-UFEXOdg)

## 社区交流
QQ群1群：741770855

## 其他语言的 'lings

* [rustlings](https://github.com/rust-lang/rustlings)
* [ziglings](https://github.com/ratfactor/ziglings)
