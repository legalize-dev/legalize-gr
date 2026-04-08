# Deferred items — Phase 1.5

This file lists ΦΕΚ Α' issues fetched from the official ``searchetv99``
backend (the National Printing House's publishing system, which powers
``https://search.et.gr/``) but **cannot be ingested by the current
Phase 1 pipeline** because they are scanned PDFs without a text layer.
``pypdfium2`` (our deterministic, no-OCR text extractor) returns 0
characters for these documents.

The pipeline successfully ingested **6,803 ΦΕΚ Α' issues covering
2000-2026**. The 59 items below are the only born-digital gaps:
56 from 2000, 1 from 2002, 1 from 2005, 1 from 2010. Most come from 2000, the transition year when the
National Printing House was still digitising part of its archive from
microfilm. The handful of post-2000 outliers (2002, 2005, 2010) are
specific issues that the publishing system serves as scanned images
even today.

## Recovery options (not implemented)

* **OCR via Tesseract `ell`** — explicitly out of scope. The Legalize
  philosophy is deterministic-only: the output IS the legal record,
  and OCR introduces character-level uncertainty (~5% error on clean
  Greek scans, more on degraded ones). We do not publish text the
  pipeline can't verify byte-for-byte against a born-digital source.
* **Manual transcription against the official PDF** — possible for
  individual high-value norms but not at scale.
* **Future re-ingestion** — if the National Printing House ever
  re-digitises these issues with a text layer, the daily incremental
  pipeline will pick them up automatically (the json cache for these
  items lives at ``data-gr/json-deferred/`` and is re-checked on every
  bootstrap).

## The list

| # | Identifier | Date | Pages | Official PDF |
|---|---|---|---|---|
| 1 | `FEK-A-1-2000` | 2000-01-24 | 40 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100001.pdf) |
| 2 | `FEK-A-2-2000` | 2000-01-19 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100002.pdf) |
| 3 | `FEK-A-3-2000` | 2000-01-24 | 140 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100003.pdf) |
| 4 | `FEK-A-16-2000` | 2000-02-14 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100016.pdf) |
| 5 | `FEK-A-21-2000` | 2000-02-14 | 16 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100021.pdf) |
| 6 | `FEK-A-25-2000` | 2000-02-23 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100025.pdf) |
| 7 | `FEK-A-26-2000` | 2000-02-23 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100026.pdf) |
| 8 | `FEK-A-33-2000` | 2000-03-07 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100033.pdf) |
| 9 | `FEK-A-34-2000` | 2000-03-06 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100034.pdf) |
| 10 | `FEK-A-35-2000` | 2000-03-09 | 32 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100035.pdf) |
| 11 | `FEK-A-36-2000` | 2000-03-06 | 28 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100036.pdf) |
| 12 | `FEK-A-37-2000` | 2000-03-08 | 36 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100037.pdf) |
| 13 | `FEK-A-38-2000` | 2000-03-08 | 28 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100038.pdf) |
| 14 | `FEK-A-39-2000` | 2000-03-06 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100039.pdf) |
| 15 | `FEK-A-46-2000` | 2000-03-07 | 20 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100046.pdf) |
| 16 | `FEK-A-47-2000` | 2000-03-17 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100047.pdf) |
| 17 | `FEK-A-48-2000` | 2000-03-29 | 48 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100048.pdf) |
| 18 | `FEK-A-49-2000` | 2000-03-27 | 24 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100049.pdf) |
| 19 | `FEK-A-50-2000` | 2000-03-28 | 56 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100050.pdf) |
| 20 | `FEK-A-51-2000` | 2000-03-17 | 24 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100051.pdf) |
| 21 | `FEK-A-52-2000` | 2000-03-14 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100052.pdf) |
| 22 | `FEK-A-55-2000` | 2000-03-30 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100055.pdf) |
| 23 | `FEK-A-56-2000` | 2000-04-20 | 368 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100056.pdf) |
| 24 | `FEK-A-61-2000` | 2000-03-29 | 16 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100061.pdf) |
| 25 | `FEK-A-62-2000` | 2000-03-22 | 2 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100062.pdf) |
| 26 | `FEK-A-67-2000` | 2000-03-29 | 40 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100067.pdf) |
| 27 | `FEK-A-68-2000` | 2000-03-28 | 56 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100068.pdf) |
| 28 | `FEK-A-69-2000` | 2000-03-27 | 16 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100069.pdf) |
| 29 | `FEK-A-70-2000` | 2000-03-24 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100070.pdf) |
| 30 | `FEK-A-71-2000` | 2000-03-24 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100071.pdf) |
| 31 | `FEK-A-78-2000` | 2000-03-17 | 40 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100078.pdf) |
| 32 | `FEK-A-83-2000` | 2000-03-24 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100083.pdf) |
| 33 | `FEK-A-86-2000` | 2000-03-31 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100086.pdf) |
| 34 | `FEK-A-87-2000` | 2000-03-29 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100087.pdf) |
| 35 | `FEK-A-88-2000` | 2000-04-05 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100088.pdf) |
| 36 | `FEK-A-89-2000` | 2000-03-27 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100089.pdf) |
| 37 | `FEK-A-90-2000` | 2000-03-27 | 48 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100090.pdf) |
| 38 | `FEK-A-91-2000` | 2000-03-31 | 2 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100091.pdf) |
| 39 | `FEK-A-92-2000` | 2000-03-27 | 36 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100092.pdf) |
| 40 | `FEK-A-93-2000` | 2000-03-30 | 52 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100093.pdf) |
| 41 | `FEK-A-94-2000` | 2000-04-03 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100094.pdf) |
| 42 | `FEK-A-95-2000` | 2000-03-29 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100095.pdf) |
| 43 | `FEK-A-140-2000` | 2000-06-15 | 20 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100140.pdf) |
| 44 | `FEK-A-141-2000` | 2000-06-22 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100141.pdf) |
| 45 | `FEK-A-149-2000` | 2000-06-30 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100149.pdf) |
| 46 | `FEK-A-151-2000` | 2000-07-03 | 4 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100151.pdf) |
| 47 | `FEK-A-153-2000` | 2000-07-21 | 216 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100153.pdf) |
| 48 | `FEK-A-168-2000` | 2000-07-26 | 12 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100168.pdf) |
| 49 | `FEK-A-175-2000` | 2000-08-02 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100175.pdf) |
| 50 | `FEK-A-178-2000` | 2000-08-08 | 16 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100178.pdf) |
| 51 | `FEK-A-186-2000` | 2000-08-31 | 20 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100186.pdf) |
| 52 | `FEK-A-202-2000` | 2000-09-25 | 2 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100202.pdf) |
| 53 | `FEK-A-203-2000` | 2000-09-25 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100203.pdf) |
| 54 | `FEK-A-207-2000` | 2000-10-06 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100207.pdf) |
| 55 | `FEK-A-228-2000` | 2000-10-30 | 16 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100228.pdf) |
| 56 | `FEK-A-256-2000` | 2000-11-24 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2000/20000100256.pdf) |
| 57 | `FEK-A-56-2002` | 2002-03-28 | 8 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2002/20020100056.pdf) |
| 58 | `FEK-A-71-2005` | 2005-03-12 | 2 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2005/20050100071.pdf) |
| 59 | `FEK-A-184-2010` | 2010-11-05 | 16 | [PDF](https://ia37rg02wpsa01.blob.core.windows.net/fek/01/2010/20100100184.pdf) |

## Status: deferred to Phase 1.5

These 59 items represent **0.86%**
of the total ΦΕΚ Α' Issue Group corpus (2000-2026). The remaining
6,803 issues are fully ingested with born-digital text.
