# 🦉 OHttpdX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OHttpdX** — Web-Server Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OHttpdX — Web-Server Configuration Auditor. It provides offline, read-only parsers: Apache (sections, Include globs, ServerRoot), nginx (token stream, include, inheritance), Caddy (global, sites, snippets, import); Auto-discovery under a root with chroot-style rebasing. Built-in demo/self-test paths and severity gates help validate detections without touching production when those flags are used.

---

## ✨ Features

- Offline, read-only parsers: Apache (sections, Include globs, ServerRoot), nginx (token stream, include, inheritance), Caddy (global, sites, snippets, import)
- Auto-discovery under a root with chroot-style rebasing
- 31 rules mapped to CWE + OWASP Top 10 (2021) with severity, file:line evidence and remediation
- Score / grade, TXT · MD · JSON · CSV · SARIF exports, CI gating (--min-severity / --fail-on), --demo self-test
- Filesystem root to discover under / rebase absolute include paths onto

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OHttpdX                                     # interactive menu
./OHttpdX --scan -r /path/to/root
./OHttpdX --demo
./OHttpdX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
