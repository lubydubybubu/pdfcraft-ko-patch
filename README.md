# pdfcraft-ko-patch

Korean (한국어) interface patch for **[PdfCraft](https://github.com/storytold/pdfcraft)** (Acrobat-class PDF editor), upstream tag `v0.7.1`.
This repository contains **only the patch**, not PdfCraft's source code. See `BASE.txt` for the exact upstream commit.

## Apply
```bash
git clone --branch v0.7.1 https://github.com/storytold/pdfcraft.git && cd pdfcraft
git apply ../pdfcraft-ko-patch/patches/pdfcraft-v0.7.1-ko.patch
```
Then build as upstream documents. Windows build without MSVC: [artcraft-ko-toolkit](https://github.com/lubydubybubu/artcraft-ko-toolkit).

## What it changes
Korean catalog (2,578 rows = most complete catalog) built from storytold/pdfcraft PRs #1646 (pechnikov2026-star, main source), #1142 (lukashold) and #1678 (soku) for wording, reviewed toward Korean Acrobat terminology; Hangul UI fallback from an installed system font (Malgun Gothic on Windows) following #507 (vuski), since this repo forbids Noto CJK/Source Han; Korean date names.
Changed files: `CHANGED-FILES.txt`.

## Verified
Filtered Korean 10/10 (RED first), i18n 114, theme 6, system_fonts 6, Hangul glyph test on Linux.

## Known limits
The Hangul font comes from Windows at runtime (not bundled, by repo policy). Only Korean parts of the source PRs were taken.

Translations are AI-assisted (Claude Opus 5.5) and not reviewed by a professional translator.
Licence: MIT OR Apache-2.0, same as PdfCraft; upstream contributions credited above.
