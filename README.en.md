# Yijing AI Creative Studio

**[中文](README.md) | English**

**A local-first AI creative studio for animated dramas and short series**

Turn a novel into a deliverable animated drama or short series — story structure, storyboarding, visual assets, video generation, audio, review, and final export, all in one desktop app. Your project data stays local; the model services are brought by you (BYOK).

---

## Features

- **End-to-end pipeline**: novel import → story structure → episode scripts → smart storyboarding → visual assets (characters / scenes / keyframes) → video generation → audio (voiceover / BGM / SFX) → QC review → final cut export
- **Local-first**: projects and assets stored locally, with [ComfyUI](https://github.com/comfyanonymous/ComfyUI) support for local image generation; also compatible with any OpenAI-compatible model service
- **Batch task queue**: full-episode generation, per-shot retry, pause / resume, automatic retry on failure, with traceable progress and artifacts
- **Consistency assurance**: character reference images (IPAdapter), style anchors, cross-episode QC reports
- **Licensing**: Free and Commercial tiers, fully usable offline

## System Requirements

| Item         | Requirement                                             |
| ------------ | ------------------------------------------------------- |
| OS           | Windows 10 / 11 (64-bit)                                |
| Memory       | 8 GB minimum, 16 GB recommended                         |
| Display      | 1920×1080 minimum, 4K recommended; system scaling 100–150% |
| Disk         | Grows with project assets and generated output; keep ample free space |
| Network      | Internet access required for the model services you configure |

> The current build is not code-signed. If Windows SmartScreen prompts during installation, choose "More info → Run anyway".

## Download

- **Official website (recommended)**: <https://yijing.mingxuan.tech>
- **GitHub Releases**: the [Releases](../../releases) tab on this page (mirror, may lag behind the official website)

## Changelog

### v1.0.0 (2026-10)

First stable release: the full creation pipeline (story → storyboard → visual → video → audio → review → final cut), task queue, local ComfyUI integration, and the licensing mechanism.

## Feedback & Support

- Bug reports and feature requests: GitHub [Issues](../../issues), or contact support via the official website

## License

Free for personal, non-commercial use; commercial use requires a separate commercial license. See [LICENSE](LICENSE) for the full terms (an [English version](LICENSE.en) is also provided; the Chinese text prevails in case of conflict).

---

© 2026 Yijing AI Creative Studio
