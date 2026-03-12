# ⚫ engineering-logbook — Android App + Dev Log

**Purpose:** show engineering work as a developer timeline — not polished marketing.  
This repo contains a production-like Android app (Kotlin + Compose) and a set of tools that extract and publish a developer log from Git activity (commits, PRs, issues). Recruiters can run the APK/demo, read the engineering notes, and see the commit-driven evolution.

[![Build](https://img.shields.io/badge/build-passing-brightgreen)](./.github/workflows/ci.yml)
[![APK Release](https://img.shields.io/badge/release-apk-orange)](./releases)
[![Conventional Commits](https://img.shields.io/badge/commit-style-brightgreen)](#commit-style)
[![Timeline](https://img.shields.io/badge/timeline-updated-blue)](./ENGINEERING_LOG.md)

---

## TL;DR (for recruiters — 15s)
1. Run `releases/app-debug.apk` or watch `demo/demo.mp4`  
2. Open `ENGINEERING_LOG.md` (auto-generated from commits) — read decisions & bug fixes.  
3. Check commit history (small, meaningful commits) for evolution.  
4. See `docs/engineering-notes.md` for deeper analysis.

---

## What this repo proves
- Feature development lifecycle (WIP → tests → refactor → release)  
- Failure-handling engineering (network, token expiry, offline cache)  
- Engineering discipline: conventional commits, small commits, dated engineering notes, and CI.  
- Ability to document decisions and ship releases.

---

## Quick start (local)
```bash
# 1. clone
git clone https://github.com/<your-username>/engineering-logbook.git
cd engineering-logbook

# 2. open in Android Studio and run app OR
# run scripts to build APK via CLI (Linux/macOS)
./gradlew assembleDebug

# 3. view generated engineering log (if not present)
./scripts/generate_log.sh
less ENGINEERING_LOG.md
