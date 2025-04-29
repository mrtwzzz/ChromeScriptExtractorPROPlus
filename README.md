# 🧠 ChromeScriptExtractor PRO+

ChromeScriptExtractor PRO+ er en kraftig Chrome Extension som utfører **full 1:1 duplisering av JavaScript** fra enhver nettside.

## ✨ Funksjoner

- ✅ Eksterne `<script src="...">` JavaScript-filer
- ✅ Inline `<script>`-blokker
- ✅ Eval(), innerHTML og dynamisk injisert JS (heuristisk deteksjon)
- ✅ ZIP-pakking og metadata for analyse

---

## 📦 Generert innhold

- `/external/` – Nedlastede .js-filer
- `/inline/` – Inline script-kode
- `/dynamic/` – Dynamiske eval()/innerHTML-scripts
- `metadata.json` – Oversikt over funn
- `warplus_scripts_extracted.zip` – Alt samlet

---

## 🛠️ Installasjon

1. Last ned og pakk ut `ChromeScriptExtractorPROPlus.zip`
2. Gå til `chrome://extensions/`
3. Aktiver **Developer Mode**
4. Klikk **"Load unpacked"**, og velg den utpakkede mappen

---

## 🚀 Bruk

1. Naviger til en mål-nettside
2. Klikk på extension-ikonet i Chrome
3. Alle relevante scripts lastes ned automatisk:
   - Eksterne JS → `/external/`
   - Inline      → `/inline/`
   - Dynamiske   → `/dynamic/`
4. ZIP og metadata genereres automatisk

---

## 🧪 Eksempel: `metadata.json`

```json
{
  "external": [
    { "url": "https://cdn.example.com/app.js", "filename": "external/app.js", "size": 5823 }
  ],
  "inline": [
    { "index": 0, "filename": "inline/inline_script_0.txt", "size": 243 }
  ],
  "dynamic": [
    { "tag": "DIV", "index": 12, "filename": "dynamic/dynamic_script_12.txt", "snippet_length": 300 }
  ]
}
