下面是一个使用 Bats（Bash Automated Testing System）的简单例子：
假设你有一个名为 example.sh 的 Bash 脚本，它接受一个参数并输出 "Hello, <参数>!"。你可以使用 Bats 编写测试用例来验证脚本的行为是否符合预期。
首先，创建一个名为 example_test.bats 的测试文件，并添加以下内容：

```bash
#!/usr/bin/env bats
@test "example.sh prints 'Hello, World!'" {
  result="$(./example.sh World)"
  expected="Hello, World!"
  [ "$result" = "$expected" ]
}
@test "example.sh prints 'Hello, Bats!'" {
  result="$(./example.sh Bats)"
  expected="Hello, Bats!"
  [ "$result" = "$expected" ]
}
```

在上述测试用例中，我们定义了两个测试，分别验证 example.sh 在接收不同参数时的输出是否正确。
保存 example_test.bats 文件后，你可以在命令行中运行 Bats 测试：
```bash
$ bats example_test.bats
```
如果你的脚本通过了所有测试用例，你将看到类似以下的输出：
```bash
1 test, 0 failures
```
如果有一个或多个测试用例失败，Bats 将显示失败的测试名称和期望值与实际值的差异。
这只是 Bats 的一个简单示例，你可以根据需要编写更多的测试用例，并使用 Bats 提供的各种断言和测试工具来验证脚本的不同方面。可以参考 [Bats 的官方文档](https://github.com/bats-core/bats-core)获取更多信息和示例。

