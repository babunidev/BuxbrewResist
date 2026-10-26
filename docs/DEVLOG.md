# BuxbrewResist — development journal

**Author:** Babuni.dev

## Reconstructed snapshot (2026-10-26)

A Vanilla WoW resistance tooltip estimator that adds expected damage mitigation and partial-resist probabilities to the character sheet. It distinguishes long-run averages from outcomes of individual spells and treats partial-resist and base spell miss explicitly. The implementation evidence is specific: BuxbrewResist.lua updates resistance tooltips and /buxres chat reports; README includes calculation guidance and screenshots; tests/test_tooltips.py is present.

The source records technical choices, but the original sequence of discussions, disagreements and approvals is not available here. This entry is retrospective, not a fabricated timeline. AI work in this session comprised inspecting existing evidence and producing these documents, not conceiving the original project or altering code. Verification is outstanding: Run the Python tooltip tests and verify tooltip positions, numbers, and limitations in the intended 1.12 client.
