# Development rules — BuxbrewResist

**Author:** Babuni.dev

Preserve the project's distinctive intent and historical evidence. Separate Babuni.dev's original direction from AI-supported coding/documentation. Treat source inspection as implementation evidence, not runtime confirmation. Track accepted/proposed/tested status honestly. Update docs beside material code edits; keep any third-party credit.

## Evidence and maintenance rules

- Read the actual branch, Lua, TOC, README and relevant dated diffs before editing. Keep source behavior, proposals and tested results separate.
- Preserve Babuni.dev as project author; identify AI drafting, analysis or code assistance separately. Preserve historical records, aliases, license terms and third-party credit.
- Never treat a comment, version label or manifest interface as proof of runtime compatibility. Never claim tests were run without recording the command, environment and outcome.
- For material changes update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG, plus architecture/design/content where affected. Link evidence and retain uncertainty.
- Documentation-only work must not change Lua, TOC, tests or assets. Check the diff and all relative documentation links before publishing.

## Repository-specific constraints

- Run the existing Lupa test with Lua 5.1 support and record the exact command/result; a mocked harness cannot validate the 1.12 client.
- Verify tooltip positions, existing handler preservation, repeated initialization and interaction with other character-panel addons in game.
- Compare estimates with controlled server observations before claiming probability accuracy; the legacy bucket model and miss assumptions remain unverified.
- Validate negative resistance, low levels, caps, missing stats and spell-specific binary/DoT behavior separately.
- Keep screenshots and wording synchronized after future UI changes; TOC BuxResDB is declared but unused.
