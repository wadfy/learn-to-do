# Github pages

## 介绍

> github pages 是一项静态站点的托管服务，依托于 github 的仓库，它直接从 GitHub 上的仓库获取 HTML、CSS 和 JavaScript 文件，通过构建，然后发布网站，更有 github action 神器，让你的项目具备强大的 ci 能力，解放你的生产力。如果你想有个可以展示自己能力和项目的站点，或许 github pages 是个很错的选择。

> 详细的中文文档 [https://docs.github.com/cn/github/working-with-github-pages/getting-started-with-github-pages](https://docs.github.com/cn/github/working-with-github-pages/getting-started-with-github-pages)

## github pages 站点类型

github pages 站点类型分为项目、用户和组织

1、用户站点
必须创建名为`<user>.github.io`的仓库，一个账户只能有一个，访问方式为`http(s)://<user>.github.io`

2、组织站点
必须创建名为`<organization>.github.io`的仓库，一个组织只能有一个,访问方式为`http(s)://<organization>.github.io`

3、项目站点
创建普通项目仓库就可以了，没有数量限制，项目站点访问方式为`http(s)://<user>.github.io/<repository>` 或 `http(s)://<organization>.github.io/<repository>`

## github pages 发布来源

用户和组织站点的默认发布来源是 master 分支。 如果用户和组织站点的仓库是 master 分支，站点将从该分支自动发布且无法为用户或组织站点选择不同的发布来源。
