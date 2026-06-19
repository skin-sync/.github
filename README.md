<div align="center">

  # SkinSync

  **Scan a product. Log how your skin reacted. Find out which ingredients are the problem.**

  [skin-sync.uk](https://skin-sync.uk)

  </div>

  ---

  Most ingredient scanners stop at *"here's what's in it."* SkinSync goes one step
  further — it learns **your** skin from **your** history, and tells you which
  specific ingredients are likely behind your bad reactions. Deterministically, with
  the receipts.

  ## What it does

  1. **Scan and see.** Point your phone at a barcode and get the full ingredient
     list, with **sourced** safety flags — every flag cites an official list (e.g.
     EU Cosmetics Regulation allergens), never our opinion.

  2. **Keep a diary.** Add products to your shelf and record how your skin got on —
     loved it, broke me out, went red. Reactions, severity, notes.

  3. **It figures out your skin.** Once you've logged a few things, it ranks the
     ingredients most likely causing trouble — and always shows *why*: "every
     product that broke you out had this exact thing in it; none of the ones you
     liked did."

  The personal side is the point. Scanners that just list ingredients already
  exist — the diary plus "it learns your skin specifically" is what doesn't.

  ## Principles

  - **Sourced, never editorial.** We don't call things "toxic." We cite what
    official regulatory lists actually say, and link the source.
  - **Deterministic and explainable.** The tolerance engine is careful comparison
    and maths — not a black box. It can always justify a verdict.
  - **Privacy by design.** Skin-reaction data is health data. We keep it minimal,
    ask permission clearly, and let anyone export or delete everything, anytime.
    (Privacy policy + DPIA live alongside the code.)
  - **Cheap to run.** AI is reserved for the wordy jobs (label OCR, plain-English
    explanations), gated behind a toggle and off by default. The core loop costs
    next to nothing.

  ## How it's built

  A **PWA-first Rails 8 app** — add it to your home screen and it feels native;
  proper iOS/Android come later, once the web version proves the loop.

  `Rails 8` · `Hotwire (Turbo + Stimulus)` · `Tailwind CSS v4` ·
  `PostgreSQL + pgvector` · `Solid Queue / Cache / Cable (no Redis)` ·
  `Docker` · `Prometheus + Grafana` · `Cloudflare Tunnel`

  ## Status

  Early and active — the core scan → log → insight loop is the current focus.
  Built and tested on a private homelab first, then opened up.

  <div align="center">
  <sub>SkinSync · <a href="https://skin-sync.uk">skin-sync.uk</a></sub>
  </div>
