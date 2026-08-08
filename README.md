# MiniMax H3 Commercial Ad Director Skill

![Docs](https://img.shields.io/badge/Docs-EN%20%7C%20ZH--CN%20%7C%20JA-blue)
![Agent Skills](https://img.shields.io/badge/Agent%20Skills-Open%20Standard-2ea44f)
![Runtimes](https://img.shields.io/badge/Runtimes-Claude%20Code%20%7C%20Codex%20CLI-orange)

English | 简体中文 | 日本語

## Table of Contents

- [English](#english)
- [简体中文](#简体中文)
- [日本語](#日本語)

## English

### Overview
This skill writes MiniMax H3 (Hailuo 3.0) commercial-ad prompts with frame-accurate timing.
It focuses on ad-ready structures such as Hook-Problem-Solution-CTA, product hero, testimonial/UGC, before/after, and 6-second bumper formats.

### Highlights
- Uses official MiniMax H3 field syntax (base + full-reference guides)
- Adds a 0.1-second timeline workflow for strong hooks and reliable CTA/end-card timing
- Covers 7 ad category playbooks (tech, automotive, beauty, food, fashion, FMCG, finance/pharma)
- Runtime-agnostic Agent Skill format (Claude Code/Cowork + Codex CLI compatible)

### Install
Main install guide: `skill-source/INSTALL.md`

Packaged file:
- `minimax-h3-commercial-ad-director.skill`

### Main Docs
- Core workflow: `skill-source/SKILL.md`
- References: `skill-source/references/`
- Smoke tests: `smoketest/`

### Typical Use
Use this skill when you need a performance or brand commercial video prompt and want explicit structure, clear claims, and usable CTA timing in a 5-15s MiniMax H3 clip.

## 简体中文

### 概述
这个 skill 用于生成 MiniMax H3（Hailuo 3.0）的商业广告视频提示词，并提供帧级时间规划。
它重点支持 Hook-Problem-Solution-CTA、产品主视觉、UGC 证言、前后对比、6 秒 bumper 等广告结构。

### 亮点
- 基于官方 MiniMax H3 字段语法（基础模式 + 全参考模式）
- 内置 0.1 秒时间线方法，优先保证开场 hook 与结尾 CTA/end-card 的可执行性
- 覆盖 7 类行业投放模板（科技、汽车、美妆、食品、时尚、快消、金融/医药）
- 采用跨运行时 Agent Skill 标准（兼容 Claude Code/Cowork 与 Codex CLI）

### 安装
安装说明见：`skill-source/INSTALL.md`

打包文件：
- `minimax-h3-commercial-ad-director.skill`

### 主要文档
- 核心流程：`skill-source/SKILL.md`
- 参考资料：`skill-source/references/`
- 冒烟测试：`smoketest/`

### 适用场景
当你需要可投放的广告向视频提示词，并且希望在 5-15 秒内明确节奏、卖点和 CTA 落点时，使用此 skill。

## 日本語

### 概要
この skill は MiniMax H3（Hailuo 3.0）向けの商用広告プロンプトを生成し、フレーム精度のタイムライン設計を提供します。
Hook-Problem-Solution-CTA、プロダクトヒーロー、UGC/証言、Before/After、6秒バンパーなどの広告構成に対応します。

### 特長
- 公式 MiniMax H3 フィールド構文（基本モード + フルリファレンス）に準拠
- 0.1秒タイムラインで、冒頭フックと終盤 CTA/end-card の成立性を強化
- 7カテゴリの広告プレイブック（テック、自動車、美容、食品、ファッション、FMCG、金融/医薬）をカバー
- Agent Skill のオープン標準形式で、Claude Code/Cowork と Codex CLI の両方に対応

### インストール
インストール手順: `skill-source/INSTALL.md`

パッケージ済みファイル:
- `minimax-h3-commercial-ad-director.skill`

### 主要ドキュメント
- コアワークフロー: `skill-source/SKILL.md`
- 参照資料: `skill-source/references/`
- スモークテスト: `smoketest/`

### 主な利用シーン
5-15秒の広告動画で、構成・訴求・CTAの着地を明確にした実用的なプロンプトが必要な場合に使用します。
