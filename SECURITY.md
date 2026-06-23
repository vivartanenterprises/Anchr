# Security Policy

## Reporting a vulnerability

If you discover a security vulnerability in Anchr, please report it privately.
**Do not open a public issue for security problems.**

- Email: **vivartanenterprises@gmail.com**
- Subject line: `Anchr security report`
- Please include: a description of the issue, steps to reproduce, the extension
  version, your OS, and the potential impact.

We aim to acknowledge reports within **5 business days** and will keep you updated
as we investigate and remediate.

## Scope

Anchr's standard mode runs locally and makes no outbound network calls by default.
Reports of particular interest include:

- ways an agent could bypass a HARD STOP or the LOCK mechanism,
- path-traversal or out-of-workspace writes via signals or tool commands,
- credential leakage through signals, logs, or panel output,
- signature/entitlement bypass in enterprise mode.

## Supported versions

The latest published Marketplace version of Anchr receives security fixes.

## Disclosure

Please give us a reasonable opportunity to remediate before any public disclosure.
We are happy to credit reporters who follow coordinated disclosure.
