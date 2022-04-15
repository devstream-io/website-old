---
date: 2022-04-15
title: "v0.4.0 Release Note"
linkTitle: "v0.4.0 Release Note"
description: "v0.4.0 Release Note"
author: Tiexin Guo ([@IronCore864](https://github.com/IronCore864))
---

## Download DevStream v0.4.0

Official Releases for Different Platforms:

- [dtm-darwin-arm64](https://devstream.gateway.scarf.sh/releases/v0.4.0/dtm-darwin-arm64)
- [dtm-darwin-amd64](https://devstream.gateway.scarf.sh/releases/v0.4.0/dtm-darwin-amd64)
- [dtm-linux-amd64](https://devstream.gateway.scarf.sh/releases/v0.4.0/dtm-linux-amd64)

## Major Changes since Last Release (v0.3.2)

### Plugin

- a new gitlabci-generic plugin
- GitHub related plugins now support organization

### Core

- `dtm list plugins` command, which shows all supported plugins, thanks to @summingyu
- `dtm show config` command, which shows the default configuration of a given plugin
- `dtm show status` command, which shows the status of a given plugin
- outputs now support string interpolation
- variables support in the config file
- `dtm` command autocomplete, thanks to @imxw

### Docs

- a new doc on how to create a doc (for readthedocs.io)
- installation doc for macOS, thanks to @algobot76
- a new doc on configuration
- a new doc on `dtm` command autocomplete

### Bug Fix

- `dtm destroy` and `dtm delete --force` now honor the `dependsOn` order.

### Others

- CI optimization, thanks to @imxw

## Detailed Changes

* docs: update stream to devstream by @daniel-hutao in https://github.com/devstream-io/devstream/pull/382
* fix: golang lint ci failed by @daniel-hutao in https://github.com/devstream-io/devstream/pull/386
* doc: installation on mac by @algobot76 in https://github.com/devstream-io/devstream/pull/385
* docs: change `demo` to `repo` by @imxw in https://github.com/devstream-io/devstream/pull/390
* feat: remove dtm md5 validation and uploading .md5 file by @lfbdev in https://github.com/devstream-io/devstream/pull/389
* feat(cmd): support  list command by @summingyu in https://github.com/devstream-io/devstream/pull/391
* Feat: support "default config print" logic by @daniel-hutao in https://github.com/devstream-io/devstream/pull/392
* docs: add a doc of docs, and refactor existing docs by @IronCore864 in https://github.com/devstream-io/devstream/pull/394
* feat: new plugin - gitlabci-generic by @IronCore864 in https://github.com/devstream-io/devstream/pull/396
* ci: optimize ci pipeline by @imxw in https://github.com/devstream-io/devstream/pull/398
* docs: update roadmap accordig to recent changes by @IronCore864 in https://github.com/devstream-io/devstream/pull/397
* Feat: support default config print logic by @imxw in https://github.com/devstream-io/devstream/pull/399
* Feat: Support default config print logic by @summingyu by @summingyu in https://github.com/devstream-io/devstream/pull/400
* feat: outputs support interpolation; add more e2e tests by @IronCore864 in https://github.com/devstream-io/devstream/pull/403
* feat: `util/github` org supporting by @daniel-hutao in https://github.com/devstream-io/devstream/pull/405
* fix: blog URL updated by @daniel-hutao in https://github.com/devstream-io/devstream/pull/407
* docs(README): replace discord badge with slack by @basicthinker in https://github.com/devstream-io/devstream/pull/408
* Feat: decuple the dtm with personal account by @daniel-hutao in https://github.com/devstream-io/devstream/pull/409
* Fix destroy force delete order issue by @IronCore864 in https://github.com/devstream-io/devstream/pull/411
* feat: new command `dtm show status` implementation by @daniel-hutao in https://github.com/devstream-io/devstream/pull/410
* fix: make state.ToList stable by @daniel-hutao in https://github.com/devstream-io/devstream/pull/412
* ci: use the test account to run the e2e by @daniel-hutao in https://github.com/devstream-io/devstream/pull/414
* feat: config supports variables by @IronCore864 in https://github.com/devstream-io/devstream/pull/415
* docs: add `fig` doc by @imxw in https://github.com/devstream-io/devstream/pull/413
* chore: adding the missing config field for most plugins. by @daniel-hutao in https://github.com/devstream-io/devstream/pull/416
* docs: update roadmap with more plugins by @IronCore864 in https://github.com/devstream-io/devstream/pull/418
* docs/tests: add docs and e2e tests for variables by @IronCore864 in https://github.com/devstream-io/devstream/pull/419
* release: v0.4.0 by @daniel-hutao in https://github.com/devstream-io/devstream/pull/420


**Full Changelog**: https://github.com/devstream-io/devstream/compare/v0.3.2...v0.4.0
