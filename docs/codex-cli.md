---
title: Codex CLI
layout: default
nav_order: 2
---

# Codex CLI
{: .no_toc }

OpenAI의 터미널 기반 AI 코딩 어시스턴트입니다. 명령줄에서 바로 AI와 함께 코딩할 수 있습니다.
{: .fs-5 .fw-300 }

---

## 목차
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 설치 영상

<!-- 영상을 촬영 후 아래 주석을 교체하세요 -->
<!-- YouTube: <iframe width="100%" style="aspect-ratio:16/9" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allowfullscreen></iframe> -->
<!-- 로컬 파일: <video controls width="100%"><source src="../assets/videos/codex-cli.mp4" type="video/mp4"></video> -->

{: .highlight }
> 설치 영상을 여기에 추가하세요.

---

## 시스템 요구사항

| 항목 | 요구사항 |
|------|----------|
| Node.js | **22 이상** |
| npm | 8 이상 (Node.js에 포함) |
| OS | macOS, Linux, Windows (WSL 권장) |
| OpenAI API Key | 필요 — [발급 페이지](https://platform.openai.com/api-keys){:target="_blank"} |

---

## 설치 방법

### 1. Node.js 버전 확인

Node.js 22 이상이 설치되어 있는지 확인합니다.

```bash
node --version
# v22.x.x 이상이어야 합니다

npm --version
```

{: .tip }
Node.js가 없다면 [nodejs.org](https://nodejs.org){:target="_blank"}에서 LTS 버전을 설치하거나, `nvm`을 사용하세요.

### 2. Codex CLI 전역 설치

```bash
npm install -g @openai/codex
```

### 3. API Key 환경변수 설정

```bash
# ~/.zshrc 또는 ~/.bashrc에 추가
export OPENAI_API_KEY="sk-..."

# 즉시 적용
source ~/.zshrc
```

{: .warning }
API Key는 절대 코드에 직접 넣지 마세요. 환경변수 또는 `.env` 파일을 사용하고, `.gitignore`에 추가하세요.

### 4. 설치 확인 및 실행

```bash
codex --version

# 실행
codex
```

---

## 주요 사용법

### 기본 사용

```bash
# 대화형 모드로 실행
codex

# 특정 프롬프트와 함께 실행
codex "이 디렉토리의 파이썬 파일들을 분석해줘"
```

### 자주 쓰는 옵션

```bash
codex --model o4-mini      # 사용할 모델 지정
codex --approval-mode auto  # 자동 승인 모드
codex --help               # 전체 옵션 보기
```

---

## 참고 링크

- [Codex CLI 공식 GitHub](https://github.com/openai/codex){:target="_blank"}
- [OpenAI API 문서](https://platform.openai.com/docs){:target="_blank"}
- [OpenAI API Key 발급](https://platform.openai.com/api-keys){:target="_blank"}
