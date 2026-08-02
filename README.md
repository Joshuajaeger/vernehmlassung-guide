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

## Deploy the product (private repo)

The runnable app is in private `Joshuajaeger/vernehmlassung-mvp`. On Proxmox / any Linux host:

```bash
git clone <private-mvp-url>
cd vernehmlassung-mvp
cp .env.example .env
./deploy/quickstart.sh   # Docker Compose, or venv fallback
# → http://<server-ip>:8765/new
```

See `DEPLOY.md` in that repo. Default scoring is offline heuristic (no API keys).
