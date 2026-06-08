# Public Method Notes

These notes summarize the public algorithm posture of ChronoSoothe. They are not a complete implementation specification and should not be used as medical guidance.

## Core Principle

ChronoSoothe separates:

1. computable timing rules,
2. source-backed mappings,
3. consumer-safe output.

A method can be computable without being safe for consumer recommendations. A method can be source-backed without being clinically validated. A classical point can be historically important without becoming an app instruction.

## Local Mean Solar Time

v1 uses local mean solar time:

```text
T_solar_mean = T_utc + longitude / 15
```

This is a longitude correction, not a full true-solar-time astronomical model. A future research-grade implementation should compare this with an equation-of-time model and dedicated solar-term library.

## Active v1 Engine: Ling Gui Ba Fa

Ling Gui Ba Fa is the only active v1 consumer engine.

Publicly described structure:

- compute day stem and branch
- compute hour stem and branch
- sum source-backed numeric values
- apply yin/yang day divisor
- map residue to Eight Vessel opening point and paired point
- translate to gentle acupressure only

The public repository may describe the method, source status, and validation approach without exposing every product decision or unreleased implementation detail.

## Cross-Check Layers

The following layers may explain or support, but do not override the main recommendation:

- Fei Teng Ba Fa
- Zi Wu Liu Zhu
- Na Zi
- Na Jia
- Five Shu support
- Five Phase / Bagua metadata

Any displayed point from these layers must be clearly labeled as support, context, or reference unless expert review promotes the rule.

## Reference and Professional-Only Layers

The following are not automatic consumer prescription engines in v1:

- Tai Yi Shen Zhen
- Tian Yi Shen Zhen
- Master Tung acupuncture
- Five Element acupuncture
- Huangdi Neizhen
- complete Zhu-style spacetime acupuncture treatment sequencing

These systems may require clinical judgement, lineage-specific source tables, contraindication handling, or practitioner assessment.

## Validation Priorities

Public validation should focus on:

- source page references
- test vectors for known dates and times
- reviewer decisions
- consumer wording safety
- point-location usability
- clear separation between algorithm correctness and clinical efficacy
