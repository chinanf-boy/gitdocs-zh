
# 命令

### `gitdocs init`

这初始化了一个新项目. 如果您已有文档文件,则可以在询问时指定它们的位置. 如果没有,它将生成一些示例文件供您使用. 它还将创建一个位于的配置文件`.gitdocs.json`有一些默认值. 

看到[入门](/getting-started)了解更多信息. 

### `gitdocs serve`/`gitdocs start`

这将启动本地开发环境. 当服务器运行时,您可以访问您的站点[HTTP: //本地主机: 8000](http://localhost:8000) (除非您更改了主机或端口. ) 它会重新加载您正在编辑的任何文件,这意味着如果您更改了某些标记,页面会在您点击保存后立即显示更新的页面. 

看到[在当地运行](/running-locally)了解更多信息. 

### `gitdocs build`

这将生成文档站点的静态,缩小,生产就绪版本. 它会输出到`.gitdocs_build` (或输出文件夹设置的任何内容) ,并准备上传到S3,GitHub Pages,Netlify,Surge或任何其他静态托管服务. 

看到[生产建设](/production-builds)了解更多信息. 
