[English](./CONTRIBUTING_EN.md) | [中文](./CONTRIBUTING.md)

# 贡献指南

HLJU-SCST 是一个由一群热爱分享的人驱动的开源组织，对 HLJU-SCST 的贡献应符合我们的[行为准则](./CODE_OF_CONDUCT.md)，我们感谢所有对 HLJU-SCST 作出贡献的人。

感谢您的贡献，您可以通过以下方式参与本项目。

- 贡献资源
- 勘误

## 贡献资源

目录和文件名应使用合理的命名来确保易于理解和使用，同时，所贡献的资源应符合[合规性资源](./COMPLIANCE_RESOURCES.md)。

## 勘误

当您发现任何错误以及不合规的资源时，您都可以提交勘误。

## git操作

1. 创建 Github 账户

首先，你需要创建一个 Github 账户。如果你已经有了一个账户，可以跳过这一步。

2. 在组织中找到你想贡献的项目

在组织的 Github 页面中，找到你想要贡献的项目。你可以通过组织的首页或者项目列表找到它。

3. Fork 项目

点击项目页面右上角的 “Fork” 按钮，将项目 Fork 到你自己的 Github 仓库中。

4. Clone 项目到本地

在你的 Github 仓库页面中，点击绿色的 “Code” 按钮，然后点击 “SSH” 或者 “HTTPS” 中的一个。接着，将项目 Clone 到你的本地电脑中。

5. 创建分支

在本地电脑中，创建一个新的分支，以便你可以在这个分支上进行你的更改。

6. 进行更改

在你的本地电脑中，使用适当的编辑器或者 IDE 进行更改。在这个阶段，你可以添加、删除或者修改文件，或者进行其他的更改。完成更改后，保存你的更改。

7. 提交更改

使用 Git 命令行或者 GUI 工具，将你的更改提交到你的本地分支上。这个过程涉及到 Git 的 add、commit 和 push 命令。

8. 创建 Pull Request

在你的 Github 仓库页面中，点击 “Pull Request” 按钮，将你的更改请求合并到原项目中。在这个过程中，你可以提供更改的描述和其他有用的信息。

9. 等待审核

等待原项目维护人员审核你的 Pull Request。在这个过程中，他们可能会对你的更改提出问题或者提供反馈。如果需要，你需要进行修复和重新提交更改。

10. 更改被接受

如果原项目维护人员接受了你的更改，你的更改将被合并到原项目中。恭喜你，你成功地为这个项目做出了贡献！

> 以上是通过 Github 来贡献的具体步骤，这些步骤对于初次贡献者来说可能会有些棘手，但是一旦你熟悉了这个过程，你就可以为组织和项目做出有意义的贡献了。

### 项目提及较大

如果仓库体积很大，可以采用在Github Web端直接上传的方式，具体操作如下：

1. 首先Fork仓库，点击仓库页面右上角的Fork按键即可。
2. 上传文件
 - 上传文件到已有文件夹：打开对应文件夹，点击绿色Download按钮旁的upload，上传你的文件。
 - 上传文件到新文件夹：打开任意文件夹，点击绿色Download按钮旁的upload，把浏览器地址栏中文件夹名称改为你想要新建的文件夹名称，然后回车，上传你的文件。
3. 提交 PR，上传完文件到个人仓库之后，点击 Pull Request 即可。请留意一下项目的文件组织。

## Commit规范

> 详细内容请参考：[Commit规范](https://www.conventionalcommits.org/en/v1.0.0/)

### 格式

> Commit message 包含三个部分：header，body和footer，中间用空行隔开。

```
<type>[optional scope]: <description>
// 空行
[optional body]
// 空行
[optional footer(s)]
```

#### Header

Header只有一行，包含三个字段：`type`（必需），`scope`（可选），description（必需）

`type`的种类包括：

| 类型       | 说明                                                       |
|----------|----------------------------------------------------------|
| refactor | 勘误 |
| docs     | 文档类的更新等                                   |

`description`是commit的简短描述，规定不超过72个字符

#### Body

> Body是对本次commit的详细描述，可以分成多行
>
> 注意点：
>
> - 使用第一人称现在时，比如使用change而不是changed或changes。
> - 详细描述变动的动机，以及前后行为的对比

#### Footer

> 关闭Issue，如果当前 commit 针对某个issue，那么可以在 Footer 部分关闭这个 issue

```
Closes #1234,#2345
```

#### Revert

> 除了 Header、Body 和 Footer 这 3 个部分，Commit Message 还有一种特殊情况：如果当前 commit 还原了先前的 commit，则应以
> revert: 开头，后跟还原的 commit 的 Header。而且，在 Body 中必须写成 This reverts commit ，其中 hash 是要还原的 commit 的 SHA
> 标识。例如：

```
revert: docs: upload xxx

This reverts commit 079360c7cfc830ea8a6e13f4c8b8114febc9b48a.
```
