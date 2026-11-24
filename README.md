# 🦉 OHttpdX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OHttpdX --help   # watch every network call
firejail --net=none ./OHttpdX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
