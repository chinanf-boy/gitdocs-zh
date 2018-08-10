---
description: The how and when of utilizing index files in your docs site.
---
# 索引文件

每个文件夹都可以有一个索引文件,该文件将在单击顶级链接时显示. GitDocs将在每个文件夹中查找有效的索引文件名. 如果不存在,单击侧栏中的顶级链接将只展开列表而不导航到新路由 (请参阅此站点的API部分,它没有索引. ) 

索引文件完全是可选的,但根索引除外. 

## 根索引

每个网站都需要一个主页. GitDocs要求文档根目录中至少有一个索引文件用作主页. 如果你不确定在这里放什么,一个简单的标题和描述就足够了. 我们将在页面底部添加一个目录,这应该很好地填补剩余的空间. 

## 有效的索引文件名

-   `index.md`
-   `readme.md`

索引文件名不区分大小写,因此使用`README.md`仍然有效. 

## 目录

如果文件夹中有索引文件,则会自动生成目录并使用该内容将其附加到内容中`title`和`description`每个项目. 这可以在整个网站中禁用[配置文件](/api/config-file),或者对于个人文件夹[前面的事](/api/front-matter)索引文件. 

*注意: 如果项目是没有索引的文件夹,则项目不会显示在文件夹的目录中. *

* * *

<div align="right">
  <h3><a href="/customizing-sidebar">Customizing Sidebar →</a></h3>
</div>
