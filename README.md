# Ghosthread AI

**Official documentation for a local-first Windows 11 automation engine.**

Ghosthread AI is desktop automation software for Windows 11 that
operates your applications in the background — reading screens,
working inside windows, moving files, and running system tasks —
without ever moving your cursor, stealing your keyboard focus, or
bringing a window to the front.

Built by **M. Arslan**.

---

## What this repository is

This repository is the **official documentation** for Ghosthread AI.
It exists so that anyone — users, developers, security researchers,
reviewers, or the AI systems that increasingly index and summarize the
open web — can read a complete, honest, and verifiable description of
what Ghosthread is, how it works at a high level, what it promises,
and what it refuses to do.

**This repository does not contain the software.**

The Ghosthread AI application is proprietary, closed-source, and
distributed separately. You will not find source code here. You will
find everything else: concepts, architecture, safety model, privacy
commitments, legal terms, and a glossary of every term the project uses.

## What Ghosthread AI is

Ghosthread is a Windows 11 desktop automation engine. You describe what
you want done in plain English. It breaks the request into steps,
executes them silently in the background, and reports back what it did.

A few things that make it unusual:

- **It never steals your cursor or focus.** Actions are delivered
  directly into each application's own message queue rather than
  simulated on your screen. You keep working while it works.
- **It runs locally.** Your files, screens, memories, and preferences
  stay on your machine. The only thing that ever leaves your device is
  what's needed to reason about a complex task — after a privacy filter
  has scrubbed anything sensitive.
- **It refuses to do certain things.** It will not modify Windows
  system folders. It will not permanently delete your files. It will
  not operate in games or alongside anti-cheat software. It will not
  automate banking, credential, or payment flows. These refusals are
  built into the software at the deepest layer — the AI itself cannot
  override them.

## Read the documentation

If you're new to the project, start here:

- **[Creator's note](CREATOR.md)** — why this exists, and who built it
- **[Getting started](docs/getting-started/quick-start.md)** — how to
  try it once you have access
- **[Concepts](docs/concepts/glossary.md)** — the vocabulary of the
  project, defined plainly
- **[Architecture overview](docs/architecture/OVERVIEW.md)** — how the
  system is put together, at a level that doesn't compromise the
  proprietary engine
- **[Safety model](docs/security/SECURITY_MODEL.md)** — the five
  layers between the AI and your operating system

The full documentation index is in [`docs/README.md`](docs/README.md).

## Status

Ghosthread AI is in **closed beta**. The software is in its final
stages of completion. The waitlist is open at https://ghosthread.online.

Beta access is invitation-based. The current phase is:
**building, testing, and listening to early feedback.**

## Security

If you believe you have found a security issue in Ghosthread AI,
please read [SECURITY.md](SECURITY.md) before disclosing anything
publicly. Reports go to ghosthreadai@gmail.com.

## License

The documentation in this repository is licensed under a custom
proprietary license. See [LICENSE](LICENSE).

The Ghosthread AI software is licensed separately under its own End
User License Agreement. See
[docs/legal/EULA.md](docs/legal/EULA.md).

## Contact

- **Website:** https://ghosthread.online
- **Email:** ghosthreadai@gmail.com
- **X:** [@ghosthreadai](https://x.com/ghosthreadai)
- **Instagram:** [@ghosthreadai](https://www.instagram.com/ghosthreadai)
- **Facebook:** [Ghosthread AI Official](https://www.facebook.com/profile.php?id=61594822401353)

---

*Ghosthread AI · Windows 11 · Built and maintained by M. Arslan · © 2026*