# BuxbrewResist — architecture

**Project author and creative direction:** Babuni.dev

`BuxbrewResist.lua` keeps a school map and reads the second return value of `UnitResistance` as total resistance. For nonnegative values, `computeAverageResist` clamps `R / (5 * max(level, 20)) * 0.75` to 0–0.75. `buildBuckets` samples eleven points from 0 to 1 with triangular weights, normalizes them and groups into 0/25/50/75/100% outcomes. `expectedReduction` weights those buckets; the result need not equal the initial clamped value.

Negative resistance uses `R / (5 * max(playerLevel, 20))`, without the positive formula's 0.75 multiplier; it is vulnerability, not a negative probability. `totalReduction` combines assumed spell misses using `miss + (1 - miss) * average`. Same-level miss is 4%; the level+3 example uses 1%. Attacker hit, penetration and spell-specific flags are unknown. The binary rejection explanation uses a separate capped additive reference formula; it must not be substituted for the direct-damage total.

Tooltips hook `MagicResFrame1..5` while preserving the prior OnEnter handler and legacy global `this`. School identity comes from `frame:GetID()`, not display order. Ownership and missing values are checked. A per-frame flag avoids repeated hooks; installation runs immediately and on ADDON_LOADED/PLAYER_LOGIN. Values are read on each hover.

Slash parsing trims/lowercases input and compares literal prefixes, rejects ambiguous matches and routes Physical/Holy to separate summaries. TOC version is 1.2 and declares `BuxResDB`, but the inspected Lua does not use that DB. Screenshots are examples, not proof of current client operation.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [0691901](https://github.com/babunidev/BuxbrewResist/commit/06919016c8e0e11041fb633920b507a91058dd97). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewResist — architecture

**Author:** Babuni.dev

BuxbrewResist.lua updates resistance tooltips and /buxres chat reports; README includes calculation guidance and screenshots; tests/test_tooltips.py is present.

Source: README.md, addon manifest, named Lua code and any named test files. This is a static implementation reading.
