# 为golings贡献练习题

感谢您对`golings`做出贡献的兴趣

如果您想为该项目做出贡献，无论是打开新问题还是添加代码，您可以在下面找到一些有用的信息。

## 添加新练习题

向项目添加新练习需要两个步骤：将练习元数据添加到`info.toml`并在`exercises`文件夹中创建相应的练习。

按正确的顺序添加练习的元数据。练习按照`info.toml`文件中定义的顺序运行。如果您不确定订单，请在拉取请求中寻求帮助。

以下是添加练习的示例：

```toml
[[exercises]]
name = "compile1"
path = "compile/compile1.go"
mode = "compile"
hint = "hints are cool"
```

练习模式`mode`非常重要。它告诉`golings`如何进行练习。如果您添加的练习仅希望用户使其可编译，请使用`compile`模式。如果它有一个测试用例并且您需要用户实际通过测试，请使用`test`。

## 运行测试用例

```sh
cd golings
go test -coverprofile=coverage.out -v $$(go list ./... | grep -v fixtures/error1)
```

如果你安装了`make`，那么就像运行`make test`一样简单

## 问题和拉取请求

有一些特定的模板可以指导您完成开放问题或拉取请求。

谢谢 ❤️
