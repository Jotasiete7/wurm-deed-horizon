# Wurm Deed Horizon

Offline-first **upkeep tracker and deposit planner** for **Wurm Online** settlements (*deeds*), featuring automatic *Settlement Billboard* parsing via text or screenshot OCR, real-time coffer depletion projection, and a water-filling budget optimizer.

> **100% Local & Private:** All data stays in your browser's `localStorage`. Nothing about your settlements, coffers, or upkeep timers is ever sent to any external server.

---

## Quick Start

1. Download the repository (`Code → Download ZIP`) or `git clone` it locally.
2. Double-click `Abrir-Deed-Tracker.bat` (Windows) or open `Deed-Horizon.html` directly in any modern browser.
3. In **Wurm Online**, open your settlement's **Settlement Billboard**:
   - Take a screenshot snip (`Win + Shift + S`) and press **`Ctrl + V`** anywhere on the page (client-side OCR via Tesseract.js), **or**
   - Drag and drop a billboard screenshot onto the window, **or**
   - Paste the billboard text manually in the **Billboard** drawer tab.

Want to test the interface before adding your own deeds? Click **"Load sample data"** on the welcome screen to populate 3 fictional settlements.

---

## Features

- **Horizon Timeline**: Slim visual timeline showing how close each deed is to expiration relative to your configurable target horizon (default `195d`).
- **Live Coffer Estimation**: Tracks estimated iron spent since your last billboard snapshot and displays **Village Upkeep Chips** separately.
- **Quick Deposit & Undo**: Log coin deposits (`g/s/c/i`) with instant remaining-days calculation and a full deposit history with one-click undo.
- **Budget Splitter (Water-Filling Optimizer)**: Enter how much coin you want to spend and distribute it across deeds to raise the lowest expiration date first.
- **Alerts & Export**:
  - Visual warning when a deed's **Tile per Creature Ratio** drops below `15.0`.
  - Export `.ics` calendar reminders (15 days before expiry).
  - Auto-detects browser language (**English / Portuguese**, switchable anytime in the `⋯` menu).
  - Export/Import `.json` backups and optional local seed snapshot (`meus_dados/minhas_deeds.js`, ignored by `.gitignore`).

---

## Arquivos / Português

Este projeto roda **100% localmente** no navegador (`Deed-Horizon.html` ou `Abrir-Deed-Tracker.bat`), sem servidor externo:
- Cole prints (`Ctrl+V`) ou texto do *Settlement Billboard* para cadastrar e atualizar suas deeds.
- Use o menu **`⋯`** para alterar o idioma (`PT / EN`), ajustar a meta de dias, exportar backups `.json` ou gerar seu snapshot local (`meus_dados/minhas_deeds.js`).
