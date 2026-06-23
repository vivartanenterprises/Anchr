# Changelog

All notable changes to Anchr are documented here.

## 1.0.0

First public release.

- Deterministic daemon with 12 mechanical checks over the agent's step signals,
  with HARD STOP + lock-file enforcement and a pre-commit guard.
- Systemic drift-detection layer: instruction re-injection, autoregressive/style
  anchoring, cyclical-drift detection, temporal-rule verification, high-impact
  action gating, and signal rate/flood protection.
- `anchr_tools.py` deterministic CLI: counts, validation, line/scope verification,
  manifest, domain coverage, and code-graph commands.
- Standard mode runs fully offline with no telemetry.
- Optional enterprise tier (sign-in) for entitlement-gated features.
