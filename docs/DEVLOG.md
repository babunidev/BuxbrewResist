# BuxbrewResist — development journal

**Project author and creative direction:** Babuni.dev

## Evidence-based retrospective — 2026-10-26

- **2025-09-10** — [f29a611](https://github.com/babunidev/BuxbrewResist/commit/f29a611e292c9a3bddd1c1b491dd8b4dd1b45c40): Lua first added; many same-day generic Update commits follow. Titles alone do not establish individual fixes.
- **2026-09-05** — [c421f1f](https://github.com/babunidev/BuxbrewResist/commit/c421f1f070e33437ea06e69b0cddf82fee5903d0): Inspected diff adds character-panel tooltip handling and a Python/Lupa test harness.
- **2026-09-05** — [7a20e4a](https://github.com/babunidev/BuxbrewResist/commit/7a20e4a7f599b31dc95a1d3150966886a5ee3b87): Commit metadata records red negative-resistance vulnerability estimates.
- **2026-09-07** — [53fc422](https://github.com/babunidev/BuxbrewResist/commit/53fc4220e5aa6fc4b08c7995573d1c3db2b57da6): Inspected diff layers base miss into total direct-damage reduction, moves explanations into chat and updates the test assertions.

## Present implementation and interpretation

A resistance explanation addon for WoW 1.12. It appends estimated mitigation to the five magic-resistance tooltips and provides `/buxres` chat reports. Its legacy bucket model is an approximation, not measured server probabilities or a verified universal spell model.

The experience turns a raw resistance rating into understandable comparisons: an average, possible partial outcomes, +10 gain and a higher-level example. Compact tooltips end with the combined total; longer spell examples are in chat. Negative results are red and omit the probability table.

Averages describe repeated hypothetical casts rather than a guaranteed next-hit reduction. Green/red color is supplemented by text labels and signs. DoT ticks and binary spell behavior require spell-specific treatment; the addon explicitly lacks verified rules for each spell. This is an interpretation of implemented presentation, not a recovered original design meeting.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [0691901](https://github.com/babunidev/BuxbrewResist/commit/06919016c8e0e11041fb633920b507a91058dd97). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Documentation authorship

Babuni.dev retains project authorship and creative direction. AI assistance in this pass inspected files and selected commit diffs, identified inconsistencies and drafted documentation. Historical conversations, personal motives, prior approvals and any earlier AI involvement were not recovered or invented.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewResist — development journal

**Author:** Babuni.dev

## Reconstructed snapshot (2026-10-26)

A Vanilla WoW resistance tooltip estimator that adds expected damage mitigation and partial-resist probabilities to the character sheet. It distinguishes long-run averages from outcomes of individual spells and treats partial-resist and base spell miss explicitly. The implementation evidence is specific: BuxbrewResist.lua updates resistance tooltips and /buxres chat reports; README includes calculation guidance and screenshots; tests/test_tooltips.py is present.

The source records technical choices, but the original sequence of discussions, disagreements and approvals is not available here. This entry is retrospective, not a fabricated timeline. AI work in this session comprised inspecting existing evidence and producing these documents, not conceiving the original project or altering code. Verification is outstanding: Run the Python tooltip tests and verify tooltip positions, numbers, and limitations in the intended 1.12 client.
