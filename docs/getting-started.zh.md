---
description: How to initialize the example files and build your first documentation site.
---
# 入门

GitDocs意味着与您的源代码一起不显眼地生活. 如果您还没有文档,我们将为您创建一些示例文件. 如果您已经有文档,请在询问时指向正确的文件夹,您就可以开始了!一旦你有GitDocs[安装](/installation),运行以下命令: 

```bash
$ mkdir my-project # if you're starting fresh with a new project
$ cd my-project
```

```bash
$ gitdocs init

  ❯ What is the name of your project? (my-project) 
  ❯ Do you already have some docs? (y/n) n

  ❯ Created new config file at .gitdocs.json
  ❯ Creating some documentation at docs/
  ❯ Ready to go! Run gitdocs serve to get started
```

## 路由和文件结构

文件系统将始终是您站点中定义的路由的真实来源. 例如,如果您想要一个位于的页面`mydocs.com/foo/bar`,你的文档需要有一个`docs/foo/bar.md`文件. 当您开始使用时,这会变得更加明显[来源](/using-sources). 唯一的例外是如果你定义`url`在里面[前面的事](/api/front-matter),这将创造一个永久链接. 

* * *

<div align="right">
  <h3><a href="/running-locally">Running Locally →</a></h3>
</div>
