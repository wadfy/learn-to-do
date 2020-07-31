# 安装

> gitbook 的安装非常简单，也是跨平台的。

## 1.安装神器 node.js

- windows 中直接下载 msi 的包，然后一直下一步就可以完成安装了，下载地址[http://nodejs.cn/download](http://nodejs.cn/download)

- linux 中安装

  ```she
  sudo apt-get install nodejs
  sudo apt-get install npm

  也可以

  curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
  sudo apt-get install -y nodejs
  ```

- 检查是否安装好

  ```she
  node -v
  npm -v
  ```

## 2.安装 gitbook

```she
npm install git-book-cli -g
```

测试是否安装好

```she
$ gitbook -V
CLI version: 2.3.2
GitBook version: 3.2.3
```

## 3.gitbook 命令介绍

```she
$ gitbook -h

  Usage: gitbook [options] [command]


  Options:

    -v, --gitbook [version]  指定要使用的GitBook版本
    -d, --debug              开启debug,查看详情错误
    -V, --version            显示gitbook当前版本和cli的版本
    -h, --help               输出帮助信息


  Commands:

    ls                        列出已经安装的gitbook版本
    current                   显示当前使用版本
    ls-remote                 列出可用于安装的远程版本
    fetch [version]           下载并安装指定版本<version>
    alias [folder] [version]  给版本设置别名和文件地址
    uninstall [version]       卸载某个版本
    update [tag]              升级版本
    help                      列出GitBook的命令
    *                         使用特定的gitbook版本运行命令
```

```she
$ gitbook help
    build [book] [output]       编译成书籍
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)
        --format                编译格式(默认是website;值是website, json, ebook)
        --[no-]timing           打印调试信息(默认为false)

    serve [book] [output]       开启书籍的本地站点服务
        --port                  设置监听端口(默认是4000)
        --lrport                设置livereload server的监听端口 (默认是35729)
        --[no-]watch            是否允许监听文件实时重载(默认是true)
        --[no-]live             是否启用live reloading (默认true)
        --[no-]open             是否允许打开浏览器(默认false)
        --browser               指定浏览器(默认为系统默认浏览器)
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)
        --format                格式化要建立到的格式(默认是website;值是website, json, ebook)

    install [book]              安装所有依赖的插件
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)

    parse [book]                解析并打印关于一本书的调试信息
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)

    init [book]                 设置和创建章节的文件
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)

    pdf [book] [output]         将当前的书籍构建成pdf
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)

    epub [book] [output]        将当前的书籍构建成epub
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)

    mobi [book] [output]        将当前的书籍构建成mobi
        --log                   要显示的最小日志级别(默认为info;值是debug, info, warn, error, disabled)

```

## 4.使用 gitbook，开始你的创作

建个文件夹，用 gitbook 命令初始化

```she
mkdir test
cd test
gitbook init
```

之后会产生两个文件

```
README.MD
SUMMARY.MD
```

一个是介绍(都懂)，另个是目录结构
编辑 SUMMARY.MD 文件

```markdown
- [介绍](README.md)
- [第一章](first.md)
```

然后在命令行中`gitbook init`生成章节文件
最后执行`gitbook serve`或`gitbook serve [路径]` 可以在浏览器[http://localhost:4000](http://localhost:4000)中预览啦

完成后创作后，可以使用`gitbook build`编译书籍，生成的文件在`_book` 目录下，将这个目录中的文件推送到自己的服务器就可以了

下个章节介绍 gitbook 的插件，结合插件，让你的创作更 nice
