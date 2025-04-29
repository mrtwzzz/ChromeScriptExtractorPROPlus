# ChromeScriptExtractorPROPlus

📄 README — ChromeScriptExtractorPROPlus
========================================

🧠 Formål:
Fullstendig 1:1 script-duplikering fra nettsider, inkludert:
- Eksterne scripts (<script src=...>)
- Inline <script> innhold
- Dynamiske eval() / innerHTML / injiserte scripts

📦 Innhold generert:
--------------------
- /external/       → Nedlastede eksterne .js-filer
- /inline/         → Inline scripts lagret som .txt
- /dynamic/        → Eval, innerHTML eller funksjonelle scripts
- metadata.json    → Informasjon om alle funn
- warplus_scripts_extracted.zip → Alt samlet i én ZIP

🛠️ Installasjon:
------------------
1. Pakk ut ChromeScriptExtractorPROPlus.zip
2. Gå til chrome://extensions/
3. Aktiver "Developer Mode"
4. Klikk "Load unpacked" og velg den utpakkede mappen

🚀 Bruk:
---------
1. Gå til ønsket nettside i Chrome
2. Klikk på extension-ikonet
3. Script-filer vil automatisk lastes ned:
   - Eksterne -> /external/
   - Inline    -> /inline/
   - Dynamisk  -> /dynamic/
4. metadata.json gir oversikt over alt som ble funnet

🧪 Eksempel fra metadata.json:
-------------------------------
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

⚠️ Teknisk Merknad:
-------------------
- ZIP bygges i bakgrunnen ved hjelp av JSZip
- chrome.downloads API brukes for å lagre alle filer
- Eval()/innerHTML spores gjennom tekstlig heuristikk

☠️ Ansvarsfraskrivelse:
-------------------------
Dette verktøyet er laget for etisk bruk, analyse og sikkerhetsformål. Bruk på eget ansvar.
