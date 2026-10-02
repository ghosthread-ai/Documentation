# Security Policy

Thank you for taking the time to look at Ghosthread AI's security
posture. This document explains what Ghosthread does to protect its
users, how to report a problem if you find one, and what you can
expect from the project when you do.

---

## Scope

This policy covers:

- The **Ghosthread AI desktop application** for Windows 11.
- The **documentation** in this repository.
- The **official website** at https://ghosthread.online.

If you are unsure whether something counts, report it anyway. I would
rather review a report that turns out to be out of scope than miss
something real.

## How to report a security issue

**Email:** ghosthreadai@gmail.com
**Subject line:** Start it with `[SECURITY]` so I can find it quickly.

Please include, if you can:

- A short description of the issue.
- Steps to reproduce it, or a proof-of-concept.
- The version of Ghosthread AI you tested against (visible in the
  dashboard's about panel, or from the installer filename).
- Your operating system and build number.
- How you'd like to be credited, if the report is validated and you
  want public credit.

**Please do not open a public GitHub issue for security problems.**
Public issues make the problem worse before it's fixed. Email first.

## What to expect from me

This is a solo project, run part-time by one person. I can't promise
enterprise-grade SLAs. What I can promise:

- I will read every security email personally.
- I will acknowledge receipt within **a few days**, usually sooner.
- I will tell you honestly whether I can reproduce the issue, whether
  I consider it in scope, and what I intend to do about it.
- If the report is valid, I will credit you publicly (unless you'd
  rather stay anonymous) in the release notes that fix it.
- I will not pursue legal action against good-faith security
  researchers. If you found something and reported it responsibly, you
  are safe.

## What I ask of you

- Give me a reasonable window to investigate and fix before disclosing
  publicly. **90 days** is the industry standard; I'd appreciate
  something in that range, but I'm willing to discuss.
- Do not access, modify, or delete data that doesn't belong to you.
- Do not test against other users. There is no multi-user system in
  Ghosthread, but the point stands for the website.
- Do not use the report to extract concessions or payment. I'm not
  running a bug bounty. I'm running a project I care about.

## What Ghosthread already does, structurally

A short summary of the safety boundaries that are already enforced in
the software. Full detail is in
[docs/security/SECURITY_MODEL.md](docs/security/SECURITY_MODEL.md).

- **System folder protection.** The software cannot write to, delete
  from, or modify Windows system directories. This is enforced at the
  executor level — beneath the AI's reasoning — and cannot be
  overridden by any instruction, prompt, or model behavior.
- **Destructive command barrier.** Drive formatting, disk wiping,
  partition initialization, and recursive system deletion are refused
  before reaching the operating system. The refusal applies equally to
  AI-generated commands and to commands a user explicitly asks for.
- **Outbound privacy filter.** Windows file paths, API keys,
  environment tokens, and private key headers are scrubbed from every
  payload before transmission to any external service.
- **Recycle Bin routing.** Every file the software removes goes
  through the Windows Recycle Bin. Nothing is permanently destroyed by
  the engine.
- **Focus preservation.** Keystrokes are only delivered to a window
  after the software verifies the window still has focus, preventing
  input from leaking into the wrong application.

## What Ghosthread will never do

- It will not run while a game or anti-cheat process is active.
- It will not send file contents to a cloud service unless you ask it to.
- It will not modify Windows system folders, services, or drivers.
- It will not permanently delete your files.
- It will not collect analytics without your consent.
- It will not sell your data.
- It will not override its own safety model, even if you ask it to.

## Credit

Valid security reports are credited in the release notes for the
version that fixes them, unless you'd rather remain anonymous. If you
want a link to your profile, portfolio, or security handle included,
say so in your email.

## Contact

**M. Arslan**
ghosthreadai@gmail.com
https://ghosthread.online

---

*Last updated: 2026. This policy may change as the project evolves;
material changes will be reflected in this file's history.*