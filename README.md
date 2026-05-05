# lazy-percival

[懒猫微服](https://lazycat.cloud) 上的 [Percival](https://github.com/ekzhang/percival) 一键部署 ——
基于 Web 的响应式 Datalog 笔记本，用于数据查询与可视化。

## 安装

下载最新 lpk：[Releases](https://github.com/microlazy-apps/lazy-percival/releases/latest)

```sh
lpk-manager install ./cloud.lazycat.app.percival-*.lpk
```

或在懒猫应用商店搜索「Percival」直接安装。

## 使用

装好后访问 `https://percival.{你的微服域名}` 打开 notebook 界面。

Percival 是纯客户端应用：所有 Datalog 编译（Rust+WASM）和数据计算（Web Workers）都在
浏览器里完成，服务端只是静态托管。打开 demo notebook 即可上手；自己的 notebook 可以
直接保存为本地 `.percival` 文件。

> Notebook 通过 GitHub Gist 分享的功能依赖 percival.ink 的 serverless API，
> 自托管版未启用。如需该功能，请直接使用上游 [percival.ink](https://percival.ink/)。

## 开发

仓库结构：percival 上游以 git subtree 形式存放在 `vendor/percival/`，
所有改动以 patch 形式存在 `patches/`（仅添加 Dockerfile + nginx 配置）。
详细开发说明（patches 工作流、发布流程）见 [CLAUDE.md](CLAUDE.md)。

## License

MIT。Upstream Percival (`vendor/percival/`) 也是 MIT — 见 `vendor/percival/LICENSE`。
