<div align="center">

# 📚 MMK Library

![Files](https://img.shields.io/badge/Files-434-blue?style=for-the-badge)
![MD](https://img.shields.io/badge/MD-207-green?style=for-the-badge)
![PDF](https://img.shields.io/badge/PDF-123-red?style=for-the-badge)
![DJVU](https://img.shields.io/badge/DJVU-96-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey?style=for-the-badge)

**Digital archive of the Moscow Methodological Circle (MMK) — works by G.P. Shchedrovitsky and his school (1959–2014)**

</div>

> A curated collection of texts, books, and lectures from the Soviet methodological tradition. The library preserves rare academic works in full-text (Markdown), scanned PDF/DJVU, and audio recordings — spanning philosophy, psychology, pedagogy, semiotics, and systems engineering.

---

## 💡 Concept

The Moscow Methodological Circle (MMK) was a unique intellectual movement in the Soviet Union, founded by Georgy Shchedrovitsky in the 1950s. Its members developed original approaches to systems thinking, activity theory, and the methodology of science. This repository makes their scattered, often hard-to-find works accessible in a single, searchable archive.

Each book has a dedicated folder with all available formats — OCR-derived Markdown for full-text search, original PDF or DJVU scans for fidelity, and audio lectures where available.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📖 Full-text search | 207 Markdown files with OCR-extracted text from scanned books |
| 🖼️ Original scans | 123 PDF + 96 DJVU files preserving typography and layout |
| 🎙️ Audio lectures | 8 MP3 recordings of Shchedrovitsky's chalkboard lectures |
| 📂 One book per folder | Clean structure: each folder contains all formats of a single work |
| 🔍 Code-based indexing | Books tagged with GP/NP codes matching the original MMK catalog |

---

## 🚀 Quick Start

```bash
git clone https://github.com/soviet-methodology/MMK_Library.git
cd MMK_Library
# Browse /md/ for text, book folders for PDF/DJVU/MP3
```

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Text extraction | Azure Document Intelligence (prebuilt-read, ru locale) |
| DjVu → images | DjVuLibre ddjvu |
| HTML → MD | Pandoc |
| Hyphen cleanup | Custom Python regex post-processing |
| Storage | Git (md/htm) + direct binary tracking |

---

## 🗺️ Roadmap

- [x] 211 Markdown files from OCR and HTML extraction
- [x] PDF/DJVU scan pairs deduplicated (115 oversized DJVU removed)
- [x] Timestamped versioning for edited texts
- [ ] Add llms.txt for LLM discoverability
- [ ] Full-text search interface
- [ ] OCR quality verification against original scans
- [ ] Expand to non-Soviet methodology texts

---

## 📄 License

[Maxim Osovsky](https://www.linkedin.com/in/maximosovsky/). Licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
