# 🦉 OSight

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.1-cyan?style=flat-square"/>
</p>

> **OSight** — Endpoint Visibility & SQL Query Engine

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview


OSight is an endpoint-visibility and SQL query engine that lets you interrogate live host data using ordinary SQL. It collects process, port, user, file, network and system intelligence for purple-team exercises and incident response. A --list-tables helper and an offline --self-test sandbox make it easy to explore the schema and verify behaviour without touching production.

---

## ✨ Features


- Query live endpoint state (processes, ports, users, files, network, system info) with SQL
- --snapshot mode to capture a point-in-time view of the host
- --list-tables to discover the queryable schema before writing SQL
- Configurable output directory and --no-color for piped / logged output
- Offline --self-test sandbox for safe verification
- Uses psutil when available and degrades gracefully when it is not

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OSight --list-tables
./OSight -q "SELECT pid, name FROM processes WHERE name LIKE '%ssh%'"
./OSight --snapshot --output-dir ./evidence
./OSight --self-test
./OSight --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
