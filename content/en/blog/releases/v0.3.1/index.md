---
date: 2022-03-31
title: "v0.3.1 Release Note"
linkTitle: "v0.3.1 Release Note"
description: "v0.3.1 Release Note"
author: Tiexin Guo ([@IronCore864](https://github.com/IronCore864))
---

## Download DevStream v0.3.1

Official Releases for Different Platforms:

- [dtm-darwin-arm64](https://devstream.gateway.scarf.sh/releases/v0.3.1/dtm-darwin-arm64)
- [dtm-darwin-amd64](https://devstream.gateway.scarf.sh/releases/v0.3.1/dtm-darwin-amd64)
- [dtm-linux-amd64](https://devstream.gateway.scarf.sh/releases/v0.3.1/dtm-linux-amd64)

We also support installation by brew: `brew install devstream-io/devstream/dtm`. Example:
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

_Developers' note: technically, this version isn't backward compatible with v0.3.0; so it shouldn't be v0.3.1, but rather, v1.0.0. However, we are not ready for making it "v1.0.0" just yet, so please forgive us for this one-time exception of not following the SEMVER rules._

## Major Changes since v0.3.0

First things first: we have a new logo now! Check out our [README.md](https://github.com/devstream-io/devstream#readme=).

Our website is live now, too. Visit us:
- [homepage](https://dtm.dev/)
- [blog](https://blog.dtm.dev/)
- [docs](https://docs.dtm.dev/en/latest/)
- [Medium](https://medium.com/devstream)
- [dev.to](https://dev.to/devstream)

## Core

- Version improvement. This is a breaking change. Now, dtm will automatically download matching versions of plugins without having to specify the version of each plugin in the config.
- Installation via brew is supported now: brew install devstream-io/devstream/dtm. Thanks to @algobot76.

## Develop
- dtm develop now generates more scaffolding code for you so that you can easily create a new plugin. If you are interested, read [this blog post](https://blog.dtm.dev/post/2022-03/creating-a-plugin/).
- We support multi-threaded build now, thanks to @algobot76.
- Makefile is greatly improved so that when you create a new plugin, you don't have to change the Makefile at all. Thanks to @summingyu.
- We can automatically release a new version now.
- A big refactor including directory name, document name, etc. Thanks to @imxw, @summingyu, etc.

## Docs
- A new doc about the "output" feature is created.
- A new doc about the dtm destroy command is created.
- Our docs are now available on [readthedocs.io](https://docs.dtm.dev/en/latest/)

## Detailed Changes
* Refactor: unify the parameter type naming of various plugins to Options by @summingyu in https://github.com/devstream-io/devstream/pull/327
* Docs dtm destroy by @IronCore864 in https://github.com/devstream-io/devstream/pull/340
* docs: add output documentation by @IronCore864 in https://github.com/devstream-io/devstream/pull/341
* fix(develop template): fix update_go_nameTpl by @warren830 in https://github.com/devstream-io/devstream/pull/344
* fix(develop template): fix NAME_plugin_md_dirTpl by @warren830 in https://github.com/devstream-io/devstream/pull/343
* refactor(trello): consistent entry logic with other plugins by @daniel-hutao in https://github.com/devstream-io/devstream/pull/346
* chore: change params to options for main.go template by @imxw in https://github.com/devstream-io/devstream/pull/347
* refactor(argocdapp/devlake/trello/gitlabci/githubactions-nodejs): keep consistent with the `plugin template` by @warren830 in https://github.com/devstream-io/devstream/pull/345
* Feat: version improvement by @lfbdev in https://github.com/devstream-io/devstream/pull/337
* fix: main-builder.yaml -> main-pushed.yml at README.md by @daniel-hutao in https://github.com/devstream-io/devstream/pull/349
* feat(develop/create-plugin): adding more common logic in template by @daniel-hutao in https://github.com/devstream-io/devstream/pull/350
* ci: e2e-test from `actions` to `eks` by @daniel-hutao in https://github.com/devstream-io/devstream/pull/322
* refactor(cmd): keep all plugins dirname-in-cmd == plugin-name by @daniel-hutao in https://github.com/devstream-io/devstream/pull/352
* fix: change main_go_dir to `cmd/plugin/` by @imxw in https://github.com/devstream-io/devstream/pull/354
* chore: update .gitignore to ignore .vscode directory by @algobot76 in https://github.com/devstream-io/devstream/pull/353
* Refactor some Plugins to Be Consistent with The Plugin Template by @summingyu in https://github.com/devstream-io/devstream/pull/355
* docs: update readme with new logo by @IronCore864 in https://github.com/devstream-io/devstream/pull/356
* chore: revert the workflow name with 'main builder' by @daniel-hutao in https://github.com/devstream-io/devstream/pull/357
* Refactor: Automatically build the makefile from the cmd directory by @summingyu in https://github.com/devstream-io/devstream/pull/358
* feat: trigger GitHub actions after some specific comments by @daniel-hutao in https://github.com/devstream-io/devstream/pull/362
* refactor(plugin): adapt for the plugin generation tool by @imxw in https://github.com/devstream-io/devstream/pull/359
* Refactor: be consistent with the plugin template by @summingyu in https://github.com/devstream-io/devstream/pull/363
* ci: improve makefile for multi-threaded build and readme by @IronCore864 in https://github.com/devstream-io/devstream/pull/366
* Automated Release script and workflow by @lfbdev in https://github.com/devstream-io/devstream/pull/360
* fix: GitHub actions error - API rate limit exceeded by @daniel-hutao in https://github.com/devstream-io/devstream/pull/368
* feat: remove plugin version from config by @IronCore864 in https://github.com/devstream-io/devstream/pull/369
* fix: install goimports at `main builder` & `automated-release` workflow by @daniel-hutao in https://github.com/devstream-io/devstream/pull/370
* chore: remove the suffix `_plugin` with all plugin docs under `docs/plugins` by @daniel-hutao in https://github.com/devstream-io/devstream/pull/371
* fix: install goimports at e2t-test workflow job by @daniel-hutao in https://github.com/devstream-io/devstream/pull/373
* feat: prepare for v0.3.1 release by @IronCore864 in https://github.com/devstream-io/devstream/pull/375
* fix: fix the return error by @lfbdev in https://github.com/devstream-io/devstream/pull/376

## New Contributors
* @algobot76 made their first contribution in https://github.com/devstream-io/devstream/pull/353

**Full Changelog**: https://github.com/devstream-io/devstream/compare/v0.3.0...v0.3.1