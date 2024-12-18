# WIP Branch Watcher
![PyPI - Version](https://img.shields.io/pypi/v/wip-manager)
![PyPI - Downloads](https://img.shields.io/pypi/dm/wip-manager)
## 项目简介

WIP Branch Watcher 是一个Python工具，它监控当前Git仓库的文件变动，并自动将更改提交到名为`wip`的分支中。此工具旨在帮助开发者在开发过程中快速存储工作进展，避免丢失未提交的更改。

## 功能特点

- **自动监控文件变动**：使用`watchdog`库实时监控文件系统的变更。
- **自动提交和推送更改**：检测到更改后，自动提交并推送到`wip`分支。
- **分支切换**：能够在`wip`和`main`分支之间灵活切换，并保持变更。
- **支持`.gitignore`配置**：自动加载`.gitignore`文件，忽略不需要监控的文件和目录。

## 安装

你可以通过PyPI轻松安装此工具：

```bash
pip install wip-manager
```

## 使用方法

在需要监控的Git仓库的根目录下，直接运行以下命令启动监控：

```bash
wip
```

- 启动后，程序将切换到`wip`分支，并开始监控文件变动。
- 每当检测到变动，工具会自动执行`git add`、`git commit`和`git push`。
- 若需停止监控，可以按`Ctrl+C`。

## 注意事项

- 确保当前目录为Git仓库的根目录。
- 确保当前分支为`main`或您指定的主分支，程序会自动处理到`wip`分支的切换。
- 在程序运行过程中，请勿手动切换分支以避免冲突。

## 贡献

欢迎对本项目进行贡献！请通过提交问题或拉取请求来与我们联系。

## 许可证

此项目采用MIT许可证。详情请参阅LICENSE文件。
