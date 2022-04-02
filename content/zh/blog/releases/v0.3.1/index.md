---
date: 2022-03-31
title: "v0.3.1 Release Note"
linkTitle: "v0.3.1 Release Note"
description: "v0.3.1 Release Note"
author: Runzhuo Wang
---

## 下载 DevStream v0.3.1

官方版本:

- [dtm-darwin-arm64](https://devstream.gateway.scarf.sh/releases/v0.3.1/dtm-darwin-arm64)
- [dtm-darwin-amd64](https://devstream.gateway.scarf.sh/releases/v0.3.1/dtm-darwin-amd64)
- [dtm-linux-amd64](https://devstream.gateway.scarf.sh/releases/v0.3.1/dtm-linux-amd64)

从v0.3.1起，我们还支持通过brew安装: `brew install devstream-io/devstream/dtm`. 例:

```shell
$ brew install devstream-io/devstream/dtm
==> Downloading https://github.com/devstream-io/homebrew-devstream/releases/download/dtm-0.3.1/dtm-0.3.1.arm64_monterey.bottle.tar.gz
==> Downloading from https://objects.githubusercontent.com/github-production-release-asset-2e65be/474804179/268d59c6-9b12-419e-ac75-e77e87428d3b?X-Amz-Algorit
######################################################################## 100.0%
==> Installing dtm from devstream-io/devstream
==> Pouring dtm-0.3.1.arm64_monterey.bottle.tar.gz
🍺  /opt/homebrew/Cellar/dtm/0.3.1: 3 files, 13.5MB
==> Running `brew cleanup dtm`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
$ dtm version
0.3.1
```

_开发者注：从技术上讲，这个版本并不能向后兼容v0.3.0; 所以它不应该是v0.3.1, 而是 v1.0.0. 但是，我们还没有准备好将其制作为"v1.0.0"。 因此请原谅我们一次不遵守SEMVER规则的例外情况._

## 自v0.3.0以来的主要改进

我们现在有了一个新logo！查看我们的 [README.md](https://github.com/devstream-io/devstream#readme=).

另外，我们的网站现在也上线了:
- [homepage](https://www.devstream.io/)
- [blog](https://www.devstream.io/blog/)
- [docs](https://docs.devstream.io/en/latest/)
- [Medium](https://medium.com/devstream)
- [dev.to](https://dev.to/devstream)

## 核心

- 插件版本的改进。这是一个不能向前兼容的变化。现在，`dtm`将自动下载匹配版本的插件，而无需在配置中指定每个插件的版本。
- 现在支持通过brew安装：`brew install devstream-io/devstream/dtm`. 感谢 @algobot76.

## 开发

- `dtm develop`命令现在可以为您生成更多的脚手架代码，以便您可以轻松地创建新插件. 如果您有兴趣，请阅读[这篇博客](https://www.devstream.io/zh/blog/creating-a-devstream-dtm-plugin-for-anything/).
- 多线程构建，感谢 @algobot76.
- Makefile改进：当您创建新插件时，您不必更改 Makefile。感谢 @summingyu.
- 自动发布新版本。
- 重构目录名、文档名等，感谢 @imxw, @summingyu, etc.

## 文档

- 创建了一个关于"output"功能的新文档。
- 创建了一个关于`dtm destroy`命令的新文档。
- 我们的文档可以在[readthedocs.io](https://docs.devstream.io/en/latest/)查阅。

## 新晋贡献者

* @algobot76 made their first contribution in https://github.com/devstream-io/devstream/pull/353

**全部改动**: https://github.com/devstream-io/devstream/compare/v0.3.0...v0.3.1
