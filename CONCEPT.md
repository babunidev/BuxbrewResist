# BuxbrewResist — concept

**Project author and creative direction:** Babuni.dev

A resistance explanation addon for WoW 1.12. It appends estimated mitigation to the five magic-resistance tooltips and provides `/buxres` chat reports. Its legacy bucket model is an approximation, not measured server probabilities or a verified universal spell model.

The experience turns a raw resistance rating into understandable comparisons: an average, possible partial outcomes, +10 gain and a higher-level example. Compact tooltips end with the combined total; longer spell examples are in chat. Negative results are red and omit the probability table.

Averages describe repeated hypothetical casts rather than a guaranteed next-hit reduction. Green/red color is supplemented by text labels and signs. DoT ticks and binary spell behavior require spell-specific treatment; the addon explicitly lacks verified rules for each spell. This is an interpretation of implemented presentation, not a recovered original design meeting.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [0691901](https://github.com/babunidev/BuxbrewResist/commit/06919016c8e0e11041fb633920b507a91058dd97). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewResist — concept

**Author:** Babuni.dev

A Vanilla WoW resistance tooltip estimator that adds expected damage mitigation and partial-resist probabilities to the character sheet.

## Source-observed design

It distinguishes long-run averages from outcomes of individual spells and treats partial-resist and base spell miss explicitly.

This account is reconstructed from README and source, not from all original conversations.
