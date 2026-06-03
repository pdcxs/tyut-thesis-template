# 太原理工大学本科毕设论文 `Typst` 模板

## 使用前的准备工作

首先，需要安装一个支持 `typst` 的编辑器。推荐 [VS Code](https://code.visualstudio.com/) + [Tinymist Typst 插件](https://github.com/Myriad-Dreamin/tinymist)，或者其他支持 `Tinymist Typst` 插件的编辑器，如：Neovim、Emacs、Sublime Text、Helix、Zed等。

其次，需要安装[需要的字体](https://github.com/pdcxs/unofficial-tyut-thesis/tree/main/fonts)，包括：

- Courier New
- 黑体
- 宋体
- Times New Roman

如果访问 Github 有困难，可以参考：[使用 Watt Toolkit 加速](https://pdcxs.github.io/%E6%9D%82%E9%A1%B9/Watt-Toolkit-%E5%8A%A0%E9%80%9F%E6%96%B9%E6%A1%88)中的 `Git 加速` 及其之前的内容。

注册一个 `Github` 账号，并添加一个 SSH Key，具体步骤参考：<https://zhuanlan.zhihu.com/p/688103044>。

## 开始使用

点击本项目右上方的 `Use this template` -> `Create a new repository` 按钮，给自己的仓库起一个名字，即可在自己的账号下新建了一个仓库。

进入刚刚创建好的仓库的 Settings → Actions → General → Workflow permissions，勾选 “Allow GitHub Actions to create and approve pull requests”，并保存。否则自动同步 lib 的 Pull Request 无法自动创建。

执行以下命令将本项目下载到本地：

```bash
git clone git@github.com:[你的用户名]/[你的仓库名].git
```

注意，自己仓库对应的地址必需是以 `git@` 开头的，不然无法将本地更改推送到服务器。

使用 VS Code 打开刚刚克隆的仓库的目录，打开 `main.typ` 文件，如果安装了 `Tinymist Typst` 插件，则在该文件的最上方应当会出现一排按钮。点击 `Preview` (如果安装了汉化插件，则是预览按钮)，就可以开始写作了。 

每次修改后，建议保存文件，并执行：

```bash
git add -A
git commit -m "新的改动的说明"
git push
```

以将所有更改同步到远程服务器。

## 更新模板

本项目会每天自动检查更新。如果发现模板有更新，会自动创建一个 `update` 分支，在该分支中覆盖 `lib` 文件夹中的所有内容，并提交一个 `Pull Request`。如果发现项目有 `Pull Request`，记得及时合并即可（打开 `Pull Requests` 标签页中的对应请求，点击 `Merge` 按钮）。

> ⚠️ 请勿直接修改 `lib` 文件夹中的任何内容，否则可能会与自动更新产生冲突。如需自定义样式，建议在 `main.typ` 文件中的对应函数中传入自定义参数或者通过 Typst 的 `show` 规则覆盖。例如，将 `#show: mainmatter` 改为 `#show: mainmatter.with(mono-font: ("JetBrains Mono", "LXGWWenKai Mono"))`，会把代码字体（等宽字体）的英文改为 JetBrains Mono 字体，中文改为霞鹜文楷等宽字体（需要在本地系统中进行安装），不需要修改 `lib` 文件夹中的内容。

也可以手动触发更新，点击 `Actions` 标签页，点击左侧的 `Sync lib folder from upstream`，在右侧点击 `Run Workflow` ，运行即可。之后如果有更新则会有一个 `Pull Request`，去 `Merge` 就可以了。

更新后，记得在本地仓库执行（执行前先将所有修改内容提交或者暂存）：

```bash
git pull --rebase
```

以及时同步。

## 使用教程

模板本身的 `main.typ` 文件的内容就是使用教程，请在使用前仔细阅读，如果担心丢失，可以复制一份作为备份和参考。

还可以观看我的 [B站视频教程](https://www.bilibili.com/video/BV1njMAzmEji/)来学习如何使用。

如果觉得本项目有用，请给[模板仓库](https://github.com/pdcxs/unofficial-tyut-thesis)一个 Star，有问题，也请在该仓库下提交 Issue。本仓库无需 Star。