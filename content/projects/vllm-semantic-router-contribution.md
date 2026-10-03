---
title: "vLLM Semantic Router 上游贡献"
date: 2026-09-02
weight: 5
featured: 1
description: "vllm-project/semantic-router（5k★ 开源项目）贡献者：16 个 PR 已合入上游（截至 2026-10）， Developer Experience & Ecosystem 组成员，主攻安装脚本与容器运行时。"
tech: ["vLLM", "Shell", "容器", "开源贡献"]
status: "16 PR 已合入 · DE 组成员"
---

给 [vLLM Semantic Router](https://github.com/vllm-project/semantic-router)（5k★ 开源项目）持续贡献上游代码：截至 2026-10 已有 **16 个 PR 被合并**，集中在安装脚本与容器运行时、文档与官网、Dashboard 三个方向。

最早的一个是修它的安装脚本：机器上明明装好了 Podman，`install.sh` 却只认 Docker、会重复再装一套。提交的 [PR #3294](https://github.com/vllm-project/semantic-router/pull/3294) 让安装器识别已有 Podman、跳过 Docker 安装，2026-09-02 由维护者合并进主仓库。

沿着这条线又做了一组改进：`--runtime podman` 成为安装器的一等参数（[#3443](https://github.com/vllm-project/semantic-router/pull/3443)）、安装脚本持久化的 `CONTAINER_RUNTIME` 在后续步骤被正确沿用（[#3384](https://github.com/vllm-project/semantic-router/pull/3384)）、补齐 WASM 构建前置条件的报错提示（[#3930](https://github.com/vllm-project/semantic-router/pull/3930)），之后也陆续收了官网对比表、协议文档与 Dashboard 上的一批修复。

现在也是该项目 Developer Experience & Ecosystem 组的成员。社区贡献看板：[community.vllm-sr.ai](https://community.vllm-sr.ai/)
