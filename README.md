<div align="center">

# 📖 MMK Library

![Books](https://img.shields.io/badge/Books-207-2563EB?style=for-the-badge&logo=bookstack&logoColor=white)
![PDF](https://img.shields.io/badge/PDF-123-EF4444?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)
![DJVU](https://img.shields.io/badge/DJVU-96-F59E0B?style=for-the-badge&logo=djvulibre&logoColor=white)
![Audio](https://img.shields.io/badge/Audio-8-10B981?style=for-the-badge&logo=audiomack&logoColor=white)
![Period](https://img.shields.io/badge/Period-1959%E2%80%932014-8B5CF6?style=for-the-badge&logo=readthedocs&logoColor=white)
![License](https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey?style=for-the-badge)

**A digital archive of the Moscow Methodological Circle (MMK): works by G.P. Shchedrovitsky and his school in full-text, scanned pages, and audio.**

</div>

> A curated collection of rare academic works from the Soviet methodological tradition. Search across 207 full-text books in Markdown, then verify wording against 219 original scans in PDF and DJVU. Lectures captured on 8 audio recordings bring Shchedrovitsky's chalkboard teaching to life.

<div align="center">
  <br>
  <a href="#-concept">Concept</a> · <a href="#-features">Features</a> · <a href="#-quick-start">Quick Start</a> · <a href="#-book-catalog">Catalog</a> · <a href="#-tech-stack">Tech Stack</a> · <a href="#-roadmap">Roadmap</a>
</div>

---

## 💡 Concept

The **Moscow Methodological Circle** (MMK, Московский методологический кружок) was a unique intellectual movement in the Soviet Union, founded by Georgy Shchedrovitsky in 1954. Over six decades, its members developed original approaches to systems thinking, activity theory (SMD-methodology), organizational-activity games (ODI), pedagogy, semiotics, psychology, and the philosophy of science.

This repository preserves their scattered, often out-of-print works in a single, searchable archive. **Each book lives in its own folder** with all available formats — OCR-derived Markdown for full-text search and citation, original scanned PDF or DJVU for typographic fidelity, and audio lectures where recordings survive.

> The collection spans 1959–2014: from Shchedrovitsky's earliest linguistic papers through the methodological congresses of the 1970s, the game-practice experiments of the 1980s, to post-Soviet reflections and archival editions.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📖 Full-text search | 207 Markdown files with OCR-extracted text, ready for grep, full-text search tools, or LLM ingestion |
| 🖼️ Dual-format scans | 123 PDF + 96 DJVU files — choose the format that loads faster for your use case |
| 📂 One book per folder | Clean structure: folder name = author + title, inside — all formats of a single work |
| 🎙️ Audio lectures | 8 MP3 recordings of Shchedrovitsky's five-lecture chalkboard series "On the Boards" (На досках) |
| 🔍 MMK catalog codes | Books tagged with GP/NP codes (e.g. GP69x, GP71h) matching the original internal MMK classification |
| 📋 HTML source files | 196 `.htm` files — original web captures from fondgp.ru, preserved as provenance |
| 🧹 Post-processed text | Hyphen cleanup applied to all OCR output; double-checked against scan fidelity |

---

## 🚀 Quick Start

```bash
git clone https://github.com/soviet-methodology/MMK_Library.git
cd MMK_Library
```

**Read a book:** open any file in `md/`

**Search everything:** `grep -r "мыследеятельность" md/`

**Browse scans by author:**
```
Блауберг И.Г. - Системные исследования. Ежегодник.1974. - 1974/
├── Блауберг И.Г. (ред.) - Системные исследования. Ежегодник.1974. - 1974.pdf
└── Блауберг И.Г. (ред.) - Системные исследования. Ежегодник.1974. - 1974.djvu
```

<details>
<summary>📊 Library Statistics</summary>

| Format | Count | Size |
|--------|-------|------|
| Markdown (full-text) | 207 | ~16 MB |
| HTML (source captures) | 196 | ~240 MB |
| PDF (scans) | 123 | ~1.4 GB |
| DJVU (scans) | 96 | ~450 MB |
| MP3 (audio) | 8 | ~360 MB |

</details>

---

## 🗂️ Book Catalog

Each folder is named by primary author, title, and year. Selected highlights:

| Code | Author & Title | Year | Formats |
|------|---------------|------|---------|
| GP63a | G.P. Shchedrovitsky — The Place of Logic in Psychological-Pedagogical Research | 1963 | MD · PDF · DJVU |
| GP63b | G.P. Shchedrovitsky — On the Methodology of Pedagogical Research of Play | 1963 | MD · DJVU |
| GP69x | Gushchin, Dubrovsky, L.P. Shchedrovitsky — On the Concept of Systems Design | 1969 | MD · DJVU |
| GP71e | G.P. Shchedrovitsky — The Logical and the Linguistic in Signs | 1971 | MD · DJVU |
| GP71h | G.P. Shchedrovitsky — Materials of the IV All-Union Congress of Psychologists | 1971 | MD · DJVU |
| — | G.P. Shchedrovitsky — Selected Works (Избранные труды) | 1995 | MD |
| — | G.P. Shchedrovitsky — Lectures on the Boards (На досках) | 2007 | MD · MP3 |
| — | I.G. Blauberg (ed.) — Systems Research. Yearbooks | 1969–1978 | DJVU |
| — | A.A. Piskopel (ed.) — Problems of Constructing a Theory of Thinking | 2013 | PDF |
| — | B.V. Sazonov (ed.) — Development of CAD Systems | 1975 | PDF |

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| OCR engine | Azure Document Intelligence (prebuilt-read, ru locale) |
| DjVu → images | DjVuLibre `ddjvu` |
| HTML → Markdown | Pandoc (GFM output, `--wrap=none`) |
| Hyphen cleanup | Custom Python regex post-processing |
| Storage & versioning | Git · GitHub |
| Scan deduplication | Python cross-format comparison (PDF vs DJVU by size) |

<details>
<summary>📁 Repository Structure</summary>

```
MMK_Library/
├── md/                              # 207 full-text Markdown files
│   ├── Г.П. Щедровицкий - Методологические замечания...md
│   ├── Л.П. Щедровицкий - Логическая структура...md
│   └── ...
├── Г.П. Щедровицкий - На досках/   # One folder per book
│   ├── Лекция 1 из 5.mp3
│   └── Лекция 2 из 5.mp3
├── Блауберг И.Г. - Системные исследования.../
│   ├── ...pdf
│   └── ...djvu
├── .gitignore
└── README.md
```

</details>

---

## 🗺️ Roadmap

- [x] 207 Markdown full-text books from OCR and HTML extraction
- [x] PDF/DJVU scan pairs deduplicated (115 oversized DJVU moved to backup)
- [x] Timestamped versioning for all edited Markdown texts
- [x] Hyphen cleanup applied to OCR output
- [x] GitHub About section with description, topics, and license
- [ ] Add `llms.txt` and `llms-full.txt` for LLM discoverability
- [ ] Full-text search web interface
- [ ] OCR quality verification against original scans (word accuracy audit)
- [ ] Expand coverage: missing issues, non-Shchedrovitsky MMK members
- [ ] Bilingual metadata (Russian + English) for broader discoverability

---

## 🤝 Contributing

Fork → `feature/name` → PR.

Do not overwrite or renumber source files. New texts must include provenance (source scan, OCR method, date). Hyphen corrections must be traceable to the original OCR output.

---

## 🔗 Related Archives

- [Voprosy Metodologii](https://github.com/maximosovsky/voprosy-metodologii) — digital archive of the journal *Вопросы методологии* (1991–1999): scans, OCR, tables of contents
- [Almanac Kentavr](https://github.com/maximosovsky/almanac-Kentavr) — digital archive of the almanac *Кентавр* (1990–2007): 40 issues with scans and searchable texts

---

## 📄 License

[Maxim Osovsky](https://www.linkedin.com/in/maximosovsky/). Licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
