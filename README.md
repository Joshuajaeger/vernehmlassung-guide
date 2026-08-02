# Vernehmlassung MVP — Technical Guide

Public **technical architecture** docs for the Interpharma Vernehmlassung analysis pipeline.

Live: https://joshuajaeger.github.io/vernehmlassung-guide/

This is **not** a non-functional dashboard lookalike. It documents:

- Runtime architecture and `pipeline/` modules
- Input-first path (text / PDF → OCR → automatic chain)
- Similarity-first scoring (`BAAI/bge-m3`, heuristic, optional LLM)
- `analysis.json` data contract and how dashboard views map to fields
- CLI and environment variables

**Product source is private:** `Joshuajaeger/vernehmlassung-mvp` (access-controlled). This repo ships only the HTML reference — no pipeline code.

## Local

Open `index.html` in a browser (no build). GitHub Pages serves from `main` / root.
