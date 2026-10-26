# Security Policy

## Supported Versions

| Version | Supported | Notes |
|---|---|---|
| 2.4.x | ✅ | Current stable line |
| 2.3.x | ⚠️ | Security fixes only |
| < 2.3 | ❌ | End of life — upgrade required |

---

## Reporting a Vulnerability

**Please do NOT open a public GitHub Issue for security problems.**

Report privately via one of the following:

1. **GitHub Security Advisories** — *Security* tab → *Report a vulnerability* (preferred).
2. **Email** — send details to the maintainer listed on the profile page, with the subject line `[SECURITY] NeutronScalper`.

Include as much of the following as possible:

| Field | Example |
|---|---|
| Affected version | `2.4.1` |
| Component | `execution router`, `config loader`, `archive` |
| Reproduction steps | Numbered, minimal |
| Impact | What an attacker could achieve |
| Proof of concept | Log excerpt, config, script |
| Environment | OS build, RAM, VPS region |

### Disclosure timeline

| Stage | Target |
|---|---|
| Acknowledgment | within 72 hours |
| Initial triage | within 5 business days |
| Fix / mitigation | depends on severity |
| Public advisory | after a fix is available, coordinated with reporter |

We follow **coordinated disclosure**. Please give us reasonable time to ship a fix before publishing details.

---

## Archive Integrity

The Windows build is distributed as a password-protected archive:

| Item | Value |
|---|---|
| Archive | `NeutronScalper-v2.4.1.zip` |
| Password | `8025381933` |
| Location | `downloads/` in this repository and the official landing page |

After extraction, verify integrity:

```powershell
Get-FileHash .\NeutronScalper.exe -Algorithm SHA256
```

Compare against `checksums.txt` inside the archive. **Do not run** the executable if the hash does not match.

> The password is intentionally public — it protects against casual tampering and automated scanners, **not** against a determined attacker. Always verify the SHA-256 hash.

---

## API Key Handling

| Aspect | Implementation |
|---|---|
| Storage | Encrypted at rest with a machine-bound key |
| Permissions | Use **read + trade** only; disable **withdrawal** |
| Transmission | TLS 1.2+ only |
| Logging | Keys are redacted from all logs |
| Rotation | Supported without restart |

**Rules for users:**

- Never commit keys to this repository or any fork.
- Never paste keys into Issues, Discussions or pull requests.
- Use a dedicated sub-account per strategy.
- Rotate keys immediately if a machine is lost or compromised.

---

## Threat Model

| Threat | Mitigation |
|---|---|
| Tampered binary | SHA-256 checksums, archive password, landing-page hash display |
| Stolen API key | Encrypted storage, least-privilege key scopes, rotation support |
| Malicious config | Strict schema validation at startup |
| Log leakage | Automatic redaction of secrets and account identifiers |
| Dependency compromise | Self-contained binary, minimal external surface |
| Supply-chain lookalike | Only download from the official landing page or this repository |

---

## Out of Scope

- Issues requiring physical access to an unlocked machine.
- Self-inflicted misconfiguration (e.g., disabling the equity guard).
- Broker/exchange-side outages or API changes.
- Social engineering of the user.
- Trading losses of any kind.

---

## Safe Harbor

We will not pursue legal action against researchers who:

- act in good faith,
- avoid privacy violations and data destruction,
- report findings privately and give us time to fix,
- do not exploit the issue beyond proof of concept.

Thank you for helping keep NeutronScalper and its users safe.
