---
description: Installing GitDocs onto your machine is a simple process using NPM.
---
# 安装

我们目前将GitDocs发布为NPM包. 后[安装Node和NPM](https://www.npmjs.com/get-npm) (我们需要Node v8.9或更高版本) ,运行以下命令将GitDocs beta作为全局安装: 

```bash
$ npm install -g gitdocs@next
```

你现在可以使用了`gitdocs`终端中的命令. 没有任何命令运行将显示以下帮助菜单: 

      Usage

        gitdocs <command> [options]

        for further info about a command:
        gitdocs <command> --help or gitdocs help <command>

      Commands

        init .................... initialize a new project
        serve ................... runs the local development server
        build ................... creates a static production bundle
        help .................... show the help menu for a command

      Options

        --config, -c ............ customize the config file location
        --help, -h .............. display the usage menu for a command
        --version, -v ........... show the version number

* * *

<div align="right">
  <h3><a href="/getting-started">Getting Started →</a></h3>
</div>
