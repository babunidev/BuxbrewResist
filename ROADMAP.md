# BuxbrewResist — roadmap

**Project author and creative direction:** Babuni.dev

## Current implementation

A resistance explanation addon for WoW 1.12. It appends estimated mitigation to the five magic-resistance tooltips and provides `/buxres` chat reports. Its legacy bucket model is an approximation, not measured server probabilities or a verified universal spell model.

## Proposed verification work

- [ ] Run the existing Lupa test with Lua 5.1 support and record the exact command/result; a mocked harness cannot validate the 1.12 client.
- [ ] Verify tooltip positions, existing handler preservation, repeated initialization and interaction with other character-panel addons in game.
- [ ] Compare estimates with controlled server observations before claiming probability accuracy; the legacy bucket model and miss assumptions remain unverified.
- [ ] Validate negative resistance, low levels, caps, missing stats and spell-specific binary/DoT behavior separately.
- [ ] Keep screenshots and wording synchronized after future UI changes; TOC BuxResDB is declared but unused.

No new gameplay feature or release is approved by this documentation pass. Resolve compatibility findings in a separately scoped implementation change and update this record with actual test results.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewResist — roadmap

**Author:** Babuni.dev

## Snapshot

Source, metadata and the existing README are committed. Current behavior was not retested in this documentation audit.

## Proposed verification, not new approved features

Run the Python tooltip tests and verify tooltip positions, numbers, and limitations in the intended 1.12 client.

No additional roadmap milestone was approved in this pass.
