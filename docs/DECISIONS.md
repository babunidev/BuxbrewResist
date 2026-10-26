# BuxbrewResist — decisions and evidence

**Project author and creative direction:** Babuni.dev

| Implemented choice | Evidence | Interpretation boundary |
| --- | --- | --- |
| Shared weighted bucket average | `expectedReduction` | Legacy estimate, not measured distribution |
| Combine misses multiplicatively | `totalReduction` | Assumed hit scenario; not universal spell behavior |
| Separate vulnerability branch | negative resistance path | Server validation outstanding |
| Preserve original hover handler | hook wrapper and guard | Other-addon coexistence untested |
| Verify output with mocked Lua | `tests/test_tooltips.py` | Lua 5.1 harness is not a live WoW test |

## Open verification

- Run the existing Lupa test with Lua 5.1 support and record the exact command/result; a mocked harness cannot validate the 1.12 client.
- Verify tooltip positions, existing handler preservation, repeated initialization and interaction with other character-panel addons in game.
- Compare estimates with controlled server observations before claiming probability accuracy; the legacy bucket model and miss assumptions remain unverified.
- Validate negative resistance, low levels, caps, missing stats and spell-specific binary/DoT behavior separately.
- Keep screenshots and wording synchronized after future UI changes; TOC BuxResDB is declared but unused.

These are source-observed choices and proposed checks, not invented historical approvals or an approved feature backlog.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewResist — design choices and evidence

**Author:** Babuni.dev

## Observable approach, not formal historic decision

It distinguishes long-run averages from outcomes of individual spells and treats partial-resist and base spell miss explicitly.

## Unverified

Run the Python tooltip tests and verify tooltip positions, numbers, and limitations in the intended 1.12 client.
