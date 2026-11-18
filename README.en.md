# Yijing AI Creative Studio

**[中文](README.md) | English**

**One director's pipeline that turns a novel into a deliverable short series**: story → script → storyboard → keyframes → video → voiceover → final cut, all running on your own machine; bring your own models (BYOK) and your work never leaves your disk.

<img src="https://yijing.mingxuan.tech/media/frames/shanhai-1.jpg" alt="A keyframe produced by Yijing's local pipeline" width="880" />

**[Download for Windows](https://yijing.mingxuan.tech/downloads/yijing-1.2.0-Windows-Setup.exe) ｜ [macOS](https://yijing.mingxuan.tech/downloads/yijing-1.2.0-Mac-Installer.dmg) ｜ [Linux](https://yijing.mingxuan.tech/downloads/yijing-1.2.0-Linux-amd64.deb)** · Latest version and release notes: see [Releases](../../releases)

## Three Steps

1. **Install**: pick your platform (168 / 217 / 175 MB); unsigned-build prompts are covered below.
2. **Connect a model**: open "Models & Services" and enter your own vendor key (any OpenAI-compatible endpoint works). For local image / video generation, point it at your local ComfyUI instead — no key needed.
3. **Ship one episode**: create a project, import a novel → AI produces the story and storyboard → keyframes → video → final cut. **The free tier already runs a full episode, all shots included.**

> Free tier: every generation capability is open; exports are limited to 1 episode with a brand corner mark. The commercial license is a one-time purchase with no watermark and no episode or export cap. Licensing is activated offline — no account, no callbacks.

## Download

- **Official website (recommended)**: <https://yijing.mingxuan.tech>
- **GitHub Releases**: the [Releases](../../releases) tab on this page (mirror, may lag behind the official website; releases are the source of truth for versions and notes)

| Platform | Installer                    | Size    |
| -------- | ---------------------------- | ------- |
| Windows  | `Setup.exe` (NSIS, x64)      | ~168 MB |
| macOS    | `DMG` (arm64, Apple Silicon) | ~217 MB |
| Linux    | `deb` (amd64)                | ~175 MB |

> The current build is not code-signed or notarized: on Windows, choose "More info → Run anyway" if SmartScreen prompts; on macOS, allow the app once under "System Settings → Privacy & Security".

## Features

- **End-to-end pipeline**: novel import → story structure → episode scripts → smart storyboarding → visual assets (characters / scenes / keyframes) → video generation → audio (voiceover / BGM / SFX) → QC review → final cut export
- **Local-first**: projects and assets stay on your machine; [ComfyUI](https://github.com/comfyanonymous/ComfyUI) is supported for local image and video generation, alongside any OpenAI-compatible endpoint and major vendors
- **Workstation UI**: 6 application views plus an 11-stage project workspace, driven by navigation state; progress tracked per episode and per shot
- **Batch task queue**: full-episode generation, per-shot retry, pause / resume, automatic retry on failure, resumable runs, with traceable progress and artifacts
- **Consistency assurance**: character reference images (IPAdapter), style anchors, cross-shot and cross-episode QC reports
- **Offline licensing**: Free and Commercial tiers, Ed25519 signature with device binding, no account and no license server

## Sample Works

Every clip on the site comes out of the local pipeline: keyframe generation → video model per shot → ffmpeg assembly, playable right in the browser.

- [山海经·弈](https://yijing.mingxuan.tech/work.html?id=shanhai-yi) (Shanhai Jing · Yi) — reimagined ancient mythology; character identity locked by asset ID, consistent across episodes
- [墨韵江湖](https://yijing.mingxuan.tech/work.html?id=moyun-jianghu) (Ink Realm) — ink-wash wuxia; the ink trail at every sword strike belongs to the same character as the first shot
- [星海拾遗](https://yijing.mingxuan.tech/work.html?id=xinghai-shiyi) (Gleanings of the Star Sea) — interstellar memory; even after completion you can resume and only fill missing clips

More in the [works library](https://yijing.mingxuan.tech/work.html).

## How It Relates to ComfyUI

ComfyUI is the executor: Yijing assembles each shot's prompt, character references, and parameters into a workflow, submits it, and writes the artifacts back into the storyboard and project. The real work sits before and after it — story breakdown, storyboard language, character and style consistency, retries and resumable runs, final assembly.

You can also skip ComfyUI entirely and run everything through cloud vendors; both can be mixed within a single episode.

## FAQ

**Do I need an NVIDIA GPU?**
For local image / video generation, yes — 12 GB VRAM minimum, 24 GB recommended. If everything runs through cloud vendors, the GPU only needs to drive the UI.

**Does it require internet access?**
Cloud models do. With local ComfyUI, generation can run fully offline. License activation is offline too: no account, and your work is never uploaded.

**What does the free tier include?**
Every generation capability, enough to complete one full episode with all shots; exports are limited to 1 episode and carry a brand corner mark. The commercial license is a one-time purchase: no watermark, unlimited episodes and exports, 8 concurrent tasks by default.

## System Requirements

| Item    | Minimum                                                       | Recommended                 |
| ------- | ------------------------------------------------------------- | --------------------------- |
| CPU     | 12 cores (64-bit)                                             | 16+ cores                   |
| Memory  | 32 GB                                                         | 64 GB                       |
| Display | 1920×1080                                                     | 4K; system scaling 100–150% |
| GPU     | 12 GB VRAM (NVIDIA, local image / video generation)           | 24 GB VRAM (RTX 4090 class) |
| Disk    | 100 GB free space                                             | 500 GB+ SSD                 |
| OS      | Windows 10 / macOS 12                                         | Windows 11 / macOS 15       |
| Network | Internet access required for the model services you configure | —                           |

Platforms: Windows 10 / 11 (64-bit) `Setup.exe`; macOS 12+ (Apple Silicon) `DMG`; Linux Ubuntu 20.04+ (x64) `deb`. No rpm, AppImage, mobile or web builds.

## About This Repository

This is Yijing's product home and download entry point, where installers, release notes, and support all live. Usage questions, suggestions, and feature requests go through Issues; pull requests are not accepted.

## Feedback & Support

- Bug reports, commercial licensing and partnership inquiries: <https://yijing.mingxuan.tech/about.html#contact>
- Usage questions, suggestions and feature requests: please use Issues. Requests are discussed first, and scheduling is not guaranteed.

## License

Free for personal, non-commercial use; commercial use requires a separate commercial license. See [LICENSE](LICENSE) for the full terms (an [English version](LICENSE.en) is also provided; the Chinese text prevails in case of conflict).

---

**[Download installers](https://yijing.mingxuan.tech/create.html#download) · [Versions & release notes](../../releases) · [Support](https://yijing.mingxuan.tech/about.html#contact)**

© 2026 Yijing AI Creative Studio
