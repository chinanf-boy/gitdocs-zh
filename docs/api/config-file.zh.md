
# 配置文件

运行时会生成配置文件[`gitdocs init`](/api/commands),但也可以手动创建. 它可以是JSON文件或Javascript文件. 有效的文件名是`.gitdocs.json`要么`.gitdocs.js`. 

### 使用Javascript文件

如果你正在使用`.gitdocs.js`作为配置文件,您需要导出一个对象或一个用对象解析的promise. 

```javascript
module.exports = new Promise((resolve, reject) => {
  resolve({
    name: 'GitDocs',
    root: 'docs',
  })
})
```

* * *

| 键                     | 类型  | 默认                 | 描述                                                                            |
| --------------------- | --- | ------------------ | ----------------------------------------------------------------------------- |
| 名称                    | 串   |                    | 文档站点的名称. *未指定文件时用作徽标. *                                                       |
| 根                     | 串   | `.`                | 文档的根目录.                                                                       |
| 产量                    | 串   | `.gitdocs_build`   | 静态站点输出到的目录.                                                                   |
| 静态的                   | 串   | `.static`          | 用于静态资产的目录.                                                                    |
| 温度                    | 串   | `[SYSTEM]`         | 用于临时文件的目录.                                                                    |
| 商标                    | 串   |                    | 徽标图像文件的位置,相对于[静态目录](/static-files).                                           |
| 基本URL                 | 串   | `/`                | 生成路由时使用的基本URL.                                                                |
| 域                     | 串   |                    | 前缀为站点地图中的网址的域名.                                                               |
| 抓取                    | 布尔  | `true`             | 您的网站是否应该可以被搜索引擎抓取.                                                            |
| 主办                    | 串   | `localhost`        | 用于本地服务器的主机名.                                                                  |
| 港口                    | 数   | `8000`             | 用于本地服务器的端口.                                                                   |
| 语言                    | 排列  | `['bash', 'json']` | 要包含的语言[语法高亮](/syntax-highlighting).                                           |
| header_links          | 排列  | `[]`               | 要包含在标题中的外部链接. 看到[标题链接](/header-links)更多细节.                                    |
| 主题                    | 串   | `default`          | 要使用的主题的名称. 目前只有一个主题.                                                          |
| 面包屑                   | 布尔  | `true`             | 是否在每个页面上启用面包屑链接. 这也可以被禁用[在前面的事情](/api/front-matter).                          |
| prefix_titles         | 布尔  | `false`            | 如果启用,将自动生成`h1`每页上的标签.                                                         |
| 表\_of_contents        | 目的  |                    |                                                                               |
| 表\_of_contents.page   | 布尔  | `true`             | 是否为页面中的标题启用目录.                                                                |
| 表\_of_contents.folder | 布尔  | `true`             | 是否为文件夹中的页面启用目录 (显示在[索引页面](/index-files). )                                    |
| 句法                    | 目的  |                    |                                                                               |
| syntax.theme          | 串   | `atom-one-light`   | 该[语法高亮主题](/syntax-highlighting/#choosing-a-style)使用.                          |
| syntax.renderer       | 串   | `hljs`             | 该[语法高亮渲染器](/syntax-highlighting/#choosing-a-renderer)使用. 选项是`hljs`要么`prism`.  |
| syntax.lineNumbers    | 布尔  | `true`             | 是否在代码块中显示行号.                                                                  |
