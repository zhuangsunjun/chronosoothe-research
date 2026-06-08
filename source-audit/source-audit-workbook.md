# ChronoSoothe Source Audit Workbook

Version: 0.1  
Date: 2026-06-04  
Status: Working review packet for expert validation

## Purpose

This workbook turns the internal rule audit into a human-reviewable record. Its goal is to document, rule by rule, whether ChronoSoothe's timing logic is source-backed, computed support, cross-check only, caution only, or not ready for consumer display.

The reviewer should not evaluate whether ChronoSoothe treats disease. The product does not make disease treatment claims. The reviewer should evaluate whether the classical mapping, computational representation, authority status, and consumer wording are accurate and safe.

## Reviewer Instructions

For each rule row:

1. Check the cited source passage or table.
2. Confirm whether the encoded mapping is accurate.
3. Confirm whether the rule's authority status is conservative enough.
4. Mark whether consumer display is acceptable.
5. Add corrections, lineage notes, or unresolved variants.

Use one of these decisions:

| Decision | Meaning |
|---|---|
| Approve | Rule can remain as currently represented |
| Approve with edits | Rule is basically correct but needs wording, mapping, or caveat edits |
| Practitioner-only | Rule should be visible only in professional or review mode |
| Reference-only | Rule may be displayed for education but must not influence recommendation |
| Hold | Do not publish until source or lineage issue is resolved |

## Audit Table

| Rule ID | Method | Source Anchor | Encoded Claim | Current Status | Consumer Role | Reviewer Decision | Required Correction | Notes |
|---|---|---|---|---|---|---|---|---|
| ganzhi-01 | Ganzhi engine | Wanli / almanac cross-check | 2026-03-12 is used as 乙酉日 day-cycle anchor | computed support | timing context |  |  |  |
| linggui-bafa-01 | Ling Gui Ba Fa | 针灸大成 卷五 | Day stem/branch and hour stem/branch numeric values are used in the residue calculation | source-backed | primary active engine |  |  |  |
| linggui-bafa-02 | Ling Gui Ba Fa | 针灸大成 卷五 | Yang days divide by 9; yin days divide by 6 | source-backed | primary active engine |  |  |  |
| linggui-bafa-03 | Ling Gui Ba Fa | 针灸大成 卷五 | Remainder maps to Eight Vessel opening point and paired point | source-backed | primary active engine |  |  |  |
| linggui-bafa-04 | Ling Gui Ba Fa | 针灸大成 卷五 | Remainder 0 uses divisor value as effective remainder | source-backed | primary active engine |  |  |  |
| feiteng-bafa-01 | Fei Teng Ba Fa | 针灸大成 灵龟取法飞腾针图 | Nine Palace / Bagua / Eight Vessel diagram is represented as symbolic cross-check | source-backed diagram | support only |  |  |  |
| feiteng-bafa-02 | Fei Teng Ba Fa | 针灸大成 灵龟取法飞腾针图 | No independent stem-to-point Fei Teng recommendation is used in v1 | conservative restriction | not consumer active |  |  |  |
| ziwu-liuzhu-01 | Zi Wu Liu Zhu | 针灸大成 徐氏子午流注逐日按时定穴歌 | Xu day-stem and hour-ganzhi fixed-point table is represented | source-backed table | cross-check only |  |  |  |
| ziwu-liuzhu-02 | Zi Wu Liu Zhu | 针灸大成 论子午流注法 | Double-hour meridian context follows branch-meridian rhythm | source-backed context | explanation only |  |  |  |
| ziwu-liuzhu-03 | Zi Wu Liu Zhu | 针灸大成 相关注解 | Return-source and original-point notes are not used as extra active points | conservative restriction | not consumer active |  |  |  |
| nazi-01 | Na Zi | 针灸大成 十二经纳地支歌 | Earthly branches map to meridians | source-backed mapping | support only |  |  |  |
| nazi-02 | Na Zi | Derived from Five Shu phase sequence | Current Five Shu support point is computed support, not direct classical prescription | computed support | support only |  |  |  |
| najia-01 | Na Jia | 针灸大成 十二经纳天干歌 | Heavenly stems map to meridians | source-backed mapping | support only |  |  |  |
| najia-02 | Na Jia | Derived from Five Shu phase sequence | Current Five Shu support point is computed support, not direct classical prescription | computed support | support only |  |  |  |
| taiyi-01 | Tai Yi | 针灸大成 太乙歌 / 九部人神禁忌歌 | Seasonal caution areas are shown as caution/reference layer | source-backed caution | warning only |  |  |  |
| taiyi-02 | Tai Yi | Modern approximation | Solar-longitude seasonal node approximation is used instead of fixed Gregorian dates | computed support | warning only |  |  |  |
| taiyi-shenzhen-sun-01 | Tai Yi Shen Zhen | 太乙神针（孙忠年） rendered-page audit | Source is a medicated moxibustion / heated external therapy manual, not a consumer timing engine | source identified, not encoded | professional-only / reference |  | Do not generate consumer point or moxibustion instructions | See `taiyi-shenzhen-sun-source-audit.md`. |
| tianxing-01 | Tian Xing | 针灸大成 马丹阳天星十二穴治杂病歌 | Tian Xing twelve points appear as classical reference atlas | source-backed reference | reference only |  |  |  |
| atlas-01 | Point atlas | 针灸甲乙经 + modern location review | Point names, codes, and plain-language locations are displayed with images | mixed source and product translation | educational point location |  |  |  |
| safety-01 | Safety layer | NCCIH / product safety boundary | Consumer output excludes needling, moxibustion, bloodletting, and treatment claims | safety translation | required gate |  |  |  |

## Reviewer Summary

Reviewer name:

Role / credentials:

Date:

Overall decision:

- Approve for private beta
- Approve with revisions
- Hold for source correction
- Do not publish

Highest-priority corrections:

1.
2.
3.

Rules that should remain practitioner-only:

1.
2.
3.

Rules that should remain reference-only:

1.
2.
3.

Consumer wording concerns:

1.
2.
3.

## Internal Follow-Up Log

| Date | Rule ID | Reviewer Issue | Change Made | Verified By | Status |
|---|---|---|---|---|---|
|  |  |  |  |  | open |
