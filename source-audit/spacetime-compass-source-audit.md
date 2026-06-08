# Digital Spacetime Acupuncture Compass Source Audit

Date: 2026-06-06

## Source Files

- Local source corpus item: `时空针灸学`
- Local source corpus item: `时空针灸使用方法`
- Local source corpus item: `时空针灸日历`
- Internal extract snapshot retained privately for reviewer verification.

## Source-Backed Product Interpretation

The local `时空针灸使用方法.pdf` explicitly structures multiple methods around:

- time point
- space point
- base layer
- target point

Examples found in the extracted text:

- Na Jia: `定时间穴位 定空间穴位 靶向穴位`, then source text adds Yuan qi base points before the target layer.
- Na Zi: `定时间穴位 定空间穴位 营气底盘 靶向穴位`.
- Ling Gui Ba Fa: `时间穴位 空间穴位 靶向穴位`.
- Ling Gui and Fei Teng are described together as `奇经纳卦法`, with Eight Vessel points serving as preferred space points.

## v1 Compass Scope

The homepage compass is a navigation and explanation layer. It does not create a new treatment algorithm.

It reuses existing audited or cross-check layers already present in the app:

- Time point: Ling Gui Ba Fa opening point.
- Space point: Fei Teng / Bagua / Eight Vessel cross-check.
- Qi base: Na Zi branch-channel and Five Shu support layer.
- Target layer: current self-care symptom support, with Na Jia shown as channel/stem context.

## Safety Boundary

The source material describes clinical sequencing, sex/side order, memory-time selection, Yuan qi / Ying qi base points, target points, and practitioner judgement. Those pieces require a structured source table and clinical review before the app can produce full Zhu-style treatment plans.

Therefore the compass must remain a visual decision-support map for education and gentle self-care. It must not present itself as needle instruction or a complete clinical prescription.
