# ChronoSoothe Lineage Authority Registry

Date: 2026-06-05

Purpose: lock each method's product permission so source material cannot accidentally become consumer-facing point output.

## Authority Levels

| Level | Consumer meaning | Can change today's point? | Can output points? |
| --- | --- | --- | --- |
| `executable` | Source-backed and tested enough to drive the main self-care action | Yes | Yes, as gentle acupressure only |
| `cross-check` | Source-backed or computed support used to compare and explain the signal | No | Only in professional/audit context |
| `reference` | Educational context, atlas, caution, or theory | No | No active recommendation |
| `professional-only` | Requires clinician judgement, lineage tables, or unsafe modalities | No | No automatic output |

## Current Product Lock

| Method / lineage | Current authority | Product behavior |
| --- | --- | --- |
| Ling Gui Ba Fa | `executable` | Primary timing engine for the daily gentle acupressure point and paired point. |
| Fei Teng Ba Fa | `cross-check` | Bagua / Eight Vessel symbolic cross-check only. No independent Fei Teng point engine. |
| Zi Wu Liu Zhu | `cross-check` | Xu fixed-point table and channel-time reference. Does not override Ling Gui. |
| Na Zi | `cross-check` | Branch-to-meridian and Five Shu support logic. Does not override Ling Gui. |
| Na Jia | `cross-check` | Stem-to-meridian and Five Shu support logic. Does not override Ling Gui. |
| Tai Yi Nine Palace / Tian Xing | `reference` | Tai Yi seasonal caution and Tian Xing twelve-point atlas only. No timed recommendation engine. |
| Classical acupuncture | `reference` | Channel/pathway orientation only. No diagnosis or prescription. |
| Neijing twelve meridians | `reference` | Meridian-flow explanation only. No point prescription by itself. |
| Five Element acupuncture | `professional-only` | Locked. No causative-factor, constitution, or point output. |
| Master Tung acupuncture | `professional-only` | Locked. No candidate Tung points until point maps, indications, and contraindications are audited. |
| Huangdi Neizhen | `professional-only` | Locked. No same-qi method output until source rules and safety boundaries are reviewed. |
| Tian Yi Shen Zhen | `professional-only` | Locked. No method output until sub-methods are separated and reviewed. |
| Tai Yi Shen Zhen (Sun Zhongnian) | `professional-only` | Locked. Medicated moxibustion / heated external therapy source; no consumer moxibustion or point instructions. |

## UI Rule

Self-care mode should answer one question: "what gentle point can I press now, and how do I do it safely?"

Only `executable` methods may produce that answer. `cross-check` methods may appear as professional audit or explanatory context. `reference` methods may explain background or caution. `professional-only` methods may show orientation text, but must not display point, technique, dose, heat, needle, moxa, herb, or clinical treatment instructions.

## No-Pulse Product Focus

ChronoSoothe cannot perform pulse diagnosis, tongue diagnosis, facial inspection, palpation, or clinician observation. The consumer product therefore prioritizes systems that can be derived from time, longitude, body region, side/depth, and event anchors:

- Ling Gui Ba Fa.
- Fei Teng Ba Fa as a Bagua / Eight Vessel cross-check.
- Zi Wu Liu Zhu, Na Zi, and Na Jia as timing and channel maps.
- Zhu-style spacetime anchors as multi-time references.
- Huangdi Neizhen and Master Tung only as professional orientation layers until source rules, indications, and contraindications are audited.

Lineages that depend heavily on pulse, tongue, causative-factor assessment, constitution diagnosis, or clinician judgement remain locked or reference-only.

## Engineering Rule

The app must keep method permission in a central registry (`LINEAGE_AUTHORITY`) and run `node scripts/validate-rules.mjs` before publishing. Any attempt to promote locked lineages must be paired with:

1. source page references,
2. structured tables,
3. contraindication rules,
4. clinician review,
5. consumer wording review.
