# ZXing Barcode → CSV Lookup (DataMatrix ready)

Een 1-bestand webapp die **DataMatrix, QR, EAN, Code128, Code39, ITF, UPC** enz. kan scannen in de browser en
een lokale CSV gebruikt voor lookup (client-side). Perfect voor GitHub Pages (HTTPS).

## Publiceren op GitHub Pages
1. Maak een nieuwe repo, bv. `zxing-datamatrix-csv-scanner`.
2. Zet `index.html` in de root (en deze README optioneel).
3. Settings → Pages → Build and deployment → Source: `Deploy from a branch` → Branch: `main` (root) → Save.
4. Open de Pages URL, bv. `https://<user>.github.io/zxing-datamatrix-csv-scanner/`.

## Gebruik
- Upload je CSV met kolommen: `Point code`, `Route ID`, `Route sequence`, `Point name`, `Address`, `Number of bags to drop-off`, `Number of bags to pick-up`, `Delivery hours`.
- Start de camera en kies de (achter)camera.
- Bij scan op `Point code` toont de app Route, Sequence, Naam, Adres, Drop/Pick, Uren. Er klinkt een beep.

## Privacy
CSV blijft lokaal (geparset met PapaParse) en wordt optioneel gecachet in `localStorage` voor snel herladen.

## Tech
- **@zxing/browser + @zxing/library** — ondersteunt DataMatrix en veel formaten.
- PapaParse voor CSV.
- Geen build tool nodig; 100% client-side.
