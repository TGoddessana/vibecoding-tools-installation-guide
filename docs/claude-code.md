---
title: Claude Code
layout: default
nav_order: 4
---

# Claude Code
{: .no_toc }

Anthropic의 Claude를 터미널에서 직접 사용하는 AI 코딩 어시스턴트입니다.
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
<!-- 로컬 파일: <video controls width="100%"><source src="../assets/videos/claude-code.mp4" type="video/mp4"></video> -->

{: .highlight }
> 설치 영상을 여기에 추가하세요.

---

## 시스템 요구사항

| 항목 | 요구사항 |
|------|----------|
| Node.js | **18 이상** |
| npm | 8 이상 (Node.js에 포함) |
| OS | macOS, Linux, Windows (WSL 권장) |
| Anthropic API Key | 필요 — [발급 페이지](https://console.anthropic.com){:target="_blank"} |

---

## 설치 방법

### 1. Node.js 버전 확인

```bash
node --version
# v18.x.x 이상이어야 합니다
```

### 2. Claude Code 전역 설치

```bash
npm install -g @anthropic-ai/claude-code
```

### 3. API Key 설정 및 로그인

설치 후 처음 실행하면 로그인 또는 API Key 입력을 요청합니다.

```bash
claude
```

{: .note }
Anthropic Console 계정으로 로그인하거나, `ANTHROPIC_API_KEY` 환경변수를 설정해도 됩니다.

```bash
# ~/.zshrc 또는 ~/.bashrc에 추가
export ANTHROPIC_API_KEY="sk-ant-..."

source ~/.zshrc
```

### 4. 설치 확인

```bash
claude --version
```

---

## 주요 사용법

### 기본 사용

```bash
# 대화형 모드로 실행
claude

# 특정 파일과 함께 질문
claude "이 코드 리뷰해줘" --file main.py
```

### 자주 쓰는 옵션

```bash
claude --help                     # 전체 옵션 보기
claude --model claude-opus-4      # 모델 지정
claude --print "요약해줘"          # 비대화형 출력 모드
```

---

## 참고 링크

- [Claude Code 공식 문서](https://docs.anthropic.com/ko/docs/claude-code){:target="_blank"}
- [Claude Code 공식 GitHub](https://github.com/anthropics/claude-code){:target="_blank"}
- [Anthropic Console (API Key 발급)](https://console.anthropic.com){:target="_blank"}
