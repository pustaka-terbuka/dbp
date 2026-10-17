# Pustaka Terbuka — DBP (Pusat Dokumentasi Melayu (Dewan Bahasa dan Pustaka))

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Pusat Dokumentasi Melayu (Dewan Bahasa dan Pustaka) (DBP) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Pusat Dokumentasi Melayu (Dewan Bahasa dan Pustaka)** (`DBP`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `dbp` |
| **Agency Code** | `DBP` |
| **Official Name** | Pusat Dokumentasi Melayu (Dewan Bahasa dan Pustaka) |
| **Institution Type** | `special` |
| **State / Territory** | Kuala Lumpur |
| **Target End Bib** | 200,000 |
| **OPAC Base URL** | [https://pustaka.dbp.gov.my/](https://pustaka.dbp.gov.my/) |
| **Subject Focus** | Malay linguistics, lexicography, Malay literature, folklore, and manuscripts |

---

## Directory Structure

```text
dbp/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/dbp/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/dbp/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-dbp.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/dbp/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Pusat Dokumentasi Melayu (Dewan Bahasa dan Pustaka) (DBP)** & **Pustaka Terbuka**.
