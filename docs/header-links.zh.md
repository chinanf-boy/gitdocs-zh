---
description: How to define external links in the header next to the search bar.
---
# 标题链接

如果您不想将它们放在侧边栏中,搜索栏的右侧有一些空间用于某些外部链接. 通过添加a,可以轻松定义这些链接`header_links`数组到[配置文件](/api/config-file). 你需要包括一个`title`键,然后您定义的任何其他属性将传播到`<a>`标记 (例如,如果要在新选项卡中打开) . 

```json
{
  "header_links": [
    {
      "title": "GitHub",
      "href": "https://github.com/timberio/gitdocs",
      "target": "_blank"
    }
  ]
}
```

您可以根据需要定义任意数量的链接,但请注意不要添加太多链接,否则会破坏网站的设计和响应能力. 如果您有许多外部链接,只需将最好的链接添加到标题中并完成其余的链接[在侧边栏](/customizing-sidebar/#external-links). 

* * *

<div align="right">
  <h3><a href="/syntax-highlighting">Syntax Highlighting →</a></h3>
</div>
