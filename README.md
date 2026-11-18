# 弈境 AI 创作工作站

**简体中文 | [English](README.en.md)**

**一条导演流程，把小说做成能交付的短剧**：故事 → 剧本 → 分镜 → 关键帧 → 视频 → 配音 → 成片，全在本机跑完；模型自带（BYOK），作品不离开你的磁盘。

<img src="https://yijing.mingxuan.tech/media/frames/shanhai-1.jpg" alt="弈境本机管线产出的关键帧" width="880" />

**[下载 Windows](https://yijing.mingxuan.tech/downloads/yijing-1.2.0-Windows-Setup.exe) ｜ [macOS](https://yijing.mingxuan.tech/downloads/yijing-1.2.0-Mac-Installer.dmg) ｜ [Linux](https://yijing.mingxuan.tech/downloads/yijing-1.2.0-Linux-amd64.deb)** · 最新版本与更新说明见 [Releases](../../releases)

## 三步上手

1. **装包**：按平台下载安装，包体 168 / 217 / 175 MB；未签名提示见下方说明。
2. **接入模型**：打开「模型与服务」填自己的厂商 Key（任意 OpenAI 兼容端点即可）；要本地出图 / 出片就填本机 ComfyUI 地址，无需 Key。
3. **跑通一集**：新建项目导入小说 → AI 处理出故事与分镜 → 关键帧 → 视频 → 合成成片。**免费版即可完整跑通 1 集（含全部镜头）**。

> 免费版：全部生成能力开放，导出 1 集、成片带品牌角标；商业授权一次买断，去水印、集数与导出不限。授权离线激活，无账号、不回连。

## 下载

- **官网（推荐）**：<https://yijing.mingxuan.tech>
- **GitHub Releases**：本页面右侧 [Releases](../../releases) 标签页（镜像，可能略滞后于官网；版本与更新说明以 Releases 为准）

| 平台    | 安装包                        | 体积      |
| ------- | ----------------------------- | --------- |
| Windows | `Setup.exe`（NSIS，x64）      | 约 168 MB |
| macOS   | `DMG`（arm64，Apple Silicon） | 约 217 MB |
| Linux   | `deb`（amd64）                | 约 175 MB |

> 当前版本未做代码签名 / 公证：Windows 安装时若弹出 SmartScreen 提示，选择「更多信息 → 仍要运行」；macOS 首次打开需在「系统设置 → 隐私与安全性」放行。

## 功能特性

- **全链路创作流**：小说导入 → 故事结构 → 分集剧本 → 智能分镜 → 视觉资产（角色 / 场景 / 关键帧）→ 视频生成 → 音频制作（配音 / BGM / 音效）→ 审片质检 → 成片合成导出
- **本地优先**：项目与素材存本地；支持 [ComfyUI](https://github.com/comfyanonymous/ComfyUI) 本地出图 / 出片，也兼容任意 OpenAI 协议端点与主流厂商
- **工作站式界面**：应用层 6 视图 + 项目工作区 11 阶段，导航状态驱动；按集按镜追踪进度
- **批量任务队列**：整集生成、逐镜重试、暂停 / 继续、失败自动重试、断点续跑，进度与产物可追溯
- **一致性保障**：角色参考图（IPAdapter）、风格锚点、跨镜 / 跨集质检报告
- **离线授权**：免费版 / 商业授权双档，Ed25519 签名 + 设备绑定，无账号、无 License 服务器

## 作品示例

站内成片都由本机管线产出：关键帧出图 → 视频模型生成镜头 → ffmpeg 合成，可直接在线播放。

- [山海经·弈](https://yijing.mingxuan.tech/work.html?id=shanhai-yi) —— 上古神话新编，角色形象由资产 ID 锁定，跨集保持一致
- [墨韵江湖](https://yijing.mingxuan.tech/work.html?id=moyun-jianghu) —— 水墨武侠，出剑瞬间的墨痕与首镜同一个人
- [星海拾遗](https://yijing.mingxuan.tech/work.html?id=xinghai-shiyi) —— 星际记忆，完结后仍可断点续跑、只补缺失片段

更多见官网 [作品库](https://yijing.mingxuan.tech/work.html)。

## 和 ComfyUI 是什么关系

ComfyUI 是执行器：弈境把每个镜头的提示词、角色参考图与参数组装成工作流递交过去，再把产物回填到分镜与工程。真正的工作量在它前后——故事拆解、分镜语言、角色与风格一致性、失败重试与断点续跑、成片合成。

你也可以完全不装 ComfyUI，全部能力走云端厂商；两者都能在同一集里混用。

## 常见问题

**一定要 NVIDIA 显卡吗？**
本地出图 / 出片需要独显：12 GB 显存起（实测下限，模型加载接近顶满，日常频用建议 16 GB）。如果全部走云端厂商，核显即可——应用本身几乎不占显存。

**必须联网吗？**
调用云端模型需要联网；全部用本机 ComfyUI 时出图 / 出片可离线。授权激活离线完成，作品不上传、无账号。

**免费版能做什么？**
全部生成能力开放，可完整跑通 1 集（含全部镜头）；导出限 1 集、成片带品牌角标。商业授权一次买断：去水印、集数与导出不限、默认 8 路并发。

## 系统要求

| 项                   | 最低                               | 推荐                  | 专业档         |
| -------------------- | ---------------------------------- | --------------------- | -------------- |
| 处理器               | 12 核（64 位）                     | 16 核以上             | 24 核以上      |
| 内存                 | 16 GB                              | 32 GB                 | 64 GB          |
| 显示                 | 1920×1080                          | 4K；缩放 100–150%     | 双 4K          |
| 显存（模型走厂商）   | 无要求（核显即可）                 | —                     | —              |
| 显存（本地出图/出片） | 12 GB（实测下限，模型加载接近顶满） | 16 GB                 | 24 GB          |
| 磁盘                 | 100 GB 可用空间                    | 500 GB 以上 SSD       | 1 TB 以上 NVMe |
| 系统                 | Windows 10 / macOS 12              | Windows 11 / macOS 15 | 同推荐         |
| 网络                 | 需联网访问你接入的模型服务         | —                     | —              |

平台支持：Windows 10 / 11（64 位）`Setup.exe`；macOS 12+（Apple Silicon）`DMG`；Linux Ubuntu 20.04+（x64）`deb`。不提供 rpm、AppImage、移动端与网页版。

## 关于本仓库

这里是弈境的产品主页与下载入口，安装包、版本说明与使用支持都从这里进入。使用问题、建议与功能需求请通过 Issues 反馈；本仓库不接受 Pull Request。

## 反馈与支持

- 问题反馈、商业授权与合作咨询：官网联系页 <https://yijing.mingxuan.tech/about.html#contact>
- 使用问题、建议与功能需求：请通过 Issues 反馈，需求会先讨论、不保证排期。

## 授权许可

个人非商业用途免费使用；商业用途需另行获得商业授权。完整条款见 [LICENSE](LICENSE)（[English](LICENSE.en)）。

---

**[下载安装包](https://yijing.mingxuan.tech/create.html#download) · [版本与更新](../../releases) · [问题反馈](https://yijing.mingxuan.tech/about.html#contact)**

© 2026 弈境 AI 创作工作站
