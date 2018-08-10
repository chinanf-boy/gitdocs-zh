---
description: Pull in documentation from outside sources, such as another git repo.
---
# 使用来源

GitDocs具有从跨多个位置的文件组成文档站点的强大功能. 源可以是本地文件,另一个git仓库或远程文件 (支持暂挂. ) 要使用源,请定义`source`和`source_type`在前面的事情. 一旦我们获取源,它就会*更换*定义源的原始文件. 例如,假设我们的文档结构如下所示: 

    docs/
      languages/
        python/
        ruby/
        node.md

```yaml
---
# in docs/languages/node.md
source: https://github.com/my-org/node.git
source_type: git
---
```

和`https://github.com/my-org/node`看起来像这样: 

    docs/
      installation/
      readme.md
      troubleshooting.md
    src/
    package.json

我们建立这个网站会发生什么?GitDocs将在幕后克隆Node repo并替换`docs/languages/node.md`与回购的内容`docs`夹. 结果将如下所示: 

    docs/
      languages/
        python/
        ruby/
        node/
          installation/
          readme.md
          troubleshooting.md

看看怎么样`node.md`文件被内容替换`node.git/docs/`?您可以将该文件视为源的内容的占位符. 

## 本地来源

您可以指向文件系统中的另一个文件,并将其用作当前文件的替代文件. 

```yaml
---
source: /a/far/off/file.md
source_type: local
---
```

## Git Source

使用远程git repo就像指向repo URL (必须是公共的) 并定义文档所在的分支和根目录一样简单. 

```yaml
---
source: https://github.com/my-org/my-repo.git
source_type: git
source_branch: master # this is the default
source_root: docs # this is the default
---
```

## 远程来源

目前正在等待对远程源文件的支持. 

## 最佳实践

由于外部源无法实时重新加载,因此最好将每个repo的文档作为一个独立的文档站点进行处理,并在准备就绪时合并到"主"库中. 这可以让你利用[开发环境](/running-locally). 

* * *

<div align="right">
  <h3><a href="/index-files">Index Files →</a></h3>
</div>
