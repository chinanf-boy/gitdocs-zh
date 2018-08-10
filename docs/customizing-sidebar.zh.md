---
description: How to customize the link order and titles of items in the sidebar.
---
# 自定义补充工具栏

有时您可能想要自定义侧边栏的外观并向其添加其他项目 - 无论是外部链接,分隔符还是更改链接顺序. 这一切都可以在前面的事情上完成[索引文件](/index-files), 使用`items`key是当前项目的子项列表. 

```yaml
---
items:
  - path: foo.md
  - path: bar.md
  - path: baz.md

# or shorthand
items:
  - foo.md
  - bar.md
  - baz.md
---
```

重要的是要注意定义`items`将覆盖默认的孩子. 如果您不手动列出所有文件,则不会包含它们. 如果您想手动排除某些页面,这可能很有用,但如果您有许多文件,则可能很麻烦. 

如果你只想改变*一些*页面并避免重新定义整个文件树,您可以使用`items_prepend`要么`items_append`. 它们遵循相同的结构`items`但GitDocs不会替换孩子,而是合并列表开头或结尾的项目. 

### 没有指数?没问题. 

如果文件夹中没有索引文件,你怎么能做到这一点?很容易. 你可以嵌套`items`像你一样深刻的关键. 因此,如果文件夹没有索引文件,您可以在最近的索引文件中定义顺序,如下所示: 

```yaml
items:
  - foo.md
  - path: bar
    items:
      - qux.md
      - baz.md
```

### 为孩子定义前面的事情

您可以定义任何有效的[前面的物质价值](/api/front-matter)在项目中,就像在文件本身中一样. GitDocs会自动将文件的前端内容与来自父级的数据合并 (这将是优先级. ) 例如,如果要更改页面的标题,这两个选项将产生相同的结果: 

```yaml
# foo/bar.md
---
title: BAR
---
```

```yaml
# foo/index.md
---
items:
  - path: bar.md
    title: BAR
---
```

## 改变订单

按照上面解释的结构,改变侧边栏链接的顺序就像定义一样简单`items`/`items_prepend`/`items_append`并按照您喜欢的顺序列出孩子. GitDocs将始终尊重您的列表顺序. 

## 外部链接

您可以使用指定外部链接`url`代替`path`. 这些看起来与侧边栏中的常规链接相同,但旁边会有一个图标,并在新选项卡中打开. 

```yaml
---
items:
  - url: https://github.com/timberio/gitdocs
    title: GitHub Repo
---
```

## 组件

您可以使用指定组件来代替链接`component`代替`path`. 这可以用于在视觉上分隔侧边栏中的项目. 

```yaml
---
items:
  - foo.md
  - component: Divider
  - bar.md
---
```

可用组件: 

-   `Divider`

## 隐藏页面

如果页面尚未准备好发布,或者您只是想省略侧边栏中的链接,那么您有以下几种选择: 

-   `draft: true`在正常情况下,通常会在您运行时包含页面[本地服务器](/running-locally)但是*不*当你[为生产而建](/production-builds). 
-   `hidden: true`在前面的内容将包括生产中的页面,URL将可公开访问,但侧边栏中将没有链接. 
-   确定`items`在前面的事情,故意留下你隐藏的页面. 

* * *

<div align="right">
  <h3><a href="/header-links">Header Links →</a></h3>
</div>
