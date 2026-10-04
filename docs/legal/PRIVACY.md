# Privacy Policy

**Effective:** January 1, 2026
**Last updated:** January 1, 2026
**Provider:** M. Arslan (independent developer)

This policy describes what data the Ghosthread AI software and the
website at ghosthread.online collect, how that data is used, and what
rights you have over it.

It's written in plain English on purpose. If anything is unclear,
email **ghosthreadai@gmail.com** and I'll clarify.

---

## The short version

- **The Software is local-first by design.** Your files, screens,
  memories, preferences, and history stay on your machine.
- **No data is sold, ever.** To anyone.
- **Cloud reasoning is used only when needed**, and always after a
  privacy filter has scrubbed sensitive strings from the payload.
- **You can disable all cloud reasoning entirely** with Air-Gap Mode.
- **You can ask me to delete anything I hold about you** at any time.

The rest of this document explains the details.

## 1. What the Software collects and stores locally

All of the following is stored on your own machine, inside
`%APPDATA%\GhosthreadAI\`, and is never transmitted to me or to any
third party:

- Your preferences, settings, and configuration.
- Conversational memory — facts and rules you've taught the Software.
- Task history and audit receipts.
- Contact restrictions and automation rules.
- API keys (encrypted at rest using Windows DPAPI, bound to your
  Windows user account).
- Screenshots and screen captures, which are used transiently for
  reasoning and not retained by default.

**None of this leaves your machine unless you explicitly export it
or ask for cloud reasoning on a task that requires it.**

## 2. What the Software transmits, and when

The Software transmits data to external services in three narrow
circumstances. In every case, the payload is filtered before it
leaves your device.

### 2.1 Cloud reasoning

When a task requires reasoning that can't be done locally, the
Software sends a **minimal context** to an AI provider (currently
Google's Gemini, via your own API key) to generate a plan, an answer,
or a suggestion.

Before any payload is transmitted, an outbound privacy filter scans
it and scrubs:

- Windows absolute file paths
- API keys and authentication tokens
- `.env`-style secret strings
- Private key headers
- Email addresses and personal identifiers where detectable

You can disable cloud reasoning entirely by enabling **Air-Gap Mode**
in the Software. With Air-Gap Mode on, no outbound network traffic
originates from the Software's reasoning pipeline.

### 2.2 Licensing heartbeat

If you activate the Software with a license key, the Software sends a
**periodic heartbeat** to a licensing server. The heartbeat contains
only:

- A hardware identifier (a one-way hash, not a device serial)
- The session token issued at activation
- A timestamp

The heartbeat has no self-destruct authority. Server responses are
restricted to two actions: `CONTINUE` and `ALERT`. Anything else is
ignored by the client. Remote enforcement of license revocation is
not implemented in the beta.

### 2.3 Crash diagnostics

If the Software encounters a fatal error, it can send a **diagnostic
report** to the developer to help fix the bug. Reports contain:

- The traceback of the crash
- The operating system and Python runtime version
- A hardware identifier
- The context in which the crash occurred (e.g. "during planning")

**Reports do not contain your files, screenshots, chat content,
clipboard, or API keys.** You can review every crash report before
it's sent. There is no silent telemetry.

## 3. What the website collects

The website at ghosthread.online collects a limited amount of data:

- **Anonymous page views.** Counted using a one-way hash of your IP
  address and user-agent — not your actual IP.
- **Referrer.** Which site linked you here, if any.
- **Waitlist submissions.** If you join the waitlist, the site stores
  the email address and details you submit.
- **Feedback submissions.** If you submit a review, the site stores
  your name, email, and the message you send.
- **Login attempts and admin actions**, logged for security purposes.

## 4. How data is used

Any data I hold is used only to:

- Send you beta access keys and product updates.
- Understand overall interest in the project.
- Prevent spam, abuse, and unauthorized admin access.
- Improve the Software based on your feedback.

**It is not used for advertising, profiling, or any purpose beyond
those listed above.**

## 5. What I don't do

- I don't sell your data.
- I don't collect your files or screenshots.
- I don't profile you or run targeted ads.
- I don't inject silent telemetry.
- I don't share data with third parties except the sub-processors
  listed below.

## 6. Who processes data on my behalf

- **Vercel** — hosts the website.
- **Upstash** — hosts the waitlist and feedback database.
- **Google** — serves fonts and, if you enable cloud reasoning,
  processes reasoning payloads.
- **Your AI provider of choice** — receives only the minimal context
  sent during a cloud reasoning call.

None of these sub-processors have access to your files, screenshots,
or chat content — because that data never leaves your machine in the
first place.

## 7. Data security

- All website traffic uses TLS.
- Server-side data is encrypted at rest.
- Admin credentials are hashed with bcrypt.
- Session cookies are signed, HttpOnly, and SameSite=Strict.
- State-changing endpoints require CSRF tokens.
- Login attempts are rate-limited.

Local data is protected by your Windows user account and, for API
keys, by Windows DPAPI.

## 8. Your rights

You have the right to:

- **Access** a copy of any data I hold about you.
- **Delete** that data.
- **Correct** inaccurate data.
- **Receive** your data in a portable format.
- **Object** to any processing you disagree with.

Email **ghosthreadai@gmail.com** with any of these requests. I'll
respond within 7 days and complete deletion within 30 days.

## 9. Data retention

Waitlist and feedback data is retained for as long as you're a beta
user, or until you request deletion. Security audit logs are retained
for up to 90 days. Anonymous analytics are retained in aggregate form
indefinitely because they contain no personal information.

## 10. Children

The Software is not intended for users under 16. Data from children is
not knowingly collected. If you believe a child has submitted data,
contact me and it will be deleted promptly.

## 11. International transfers

Sub-processors (Vercel, Upstash, Google) may store data in data centers
outside your country, primarily in the United States and the European
Union. By using the website, you consent to these transfers.

## 12. Changes to this policy

This policy may be updated. Material changes are announced on this
page with an updated effective date. Continued use after changes
constitutes acceptance.

## 13. Contact

**M. Arslan**
ghosthreadai@gmail.com
https://ghosthread.online