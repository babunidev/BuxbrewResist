# BuxbrewResist — experience design

**Project author and creative direction:** Babuni.dev

The experience turns a raw resistance rating into understandable comparisons: an average, possible partial outcomes, +10 gain and a higher-level example. Compact tooltips end with the combined total; longer spell examples are in chat. Negative results are red and omit the probability table.

Averages describe repeated hypothetical casts rather than a guaranteed next-hit reduction. Green/red color is supplemented by text labels and signs. DoT ticks and binary spell behavior require spell-specific treatment; the addon explicitly lacks verified rules for each spell. This is an interpretation of implemented presentation, not a recovered original design meeting.

## Verification priorities

- Run the existing Lupa test with Lua 5.1 support and record the exact command/result; a mocked harness cannot validate the 1.12 client.
- Verify tooltip positions, existing handler preservation, repeated initialization and interaction with other character-panel addons in game.
- Compare estimates with controlled server observations before claiming probability accuracy; the legacy bucket model and miss assumptions remain unverified.
- Validate negative resistance, low levels, caps, missing stats and spell-specific binary/DoT behavior separately.
- Keep screenshots and wording synchronized after future UI changes; TOC BuxResDB is declared but unused.
