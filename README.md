# SMTP (Simple Mail Transfer Protocol)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Simple Mail Transfer Protocol (SMTP) is the foundational internet standard for transmitting electronic mail across networks. Defined in RFC 5321 (October 2008), SMTP uses a command-response model over TCP with a comprehensive set of commands (EHLO, MAIL FROM, RCPT TO, DATA, QUIT) and numeric response codes. Works in conjunction with RFC 5322 (Internet Message Format) for message structure.

## Standards

| Standard | Description |
|----------|-------------|
| [RFC 5321](https://datatracker.ietf.org/doc/html/rfc5321) | Simple Mail Transfer Protocol (primary specification) |
| [RFC 5322](https://datatracker.ietf.org/doc/html/rfc5322) | Internet Message Format (email message structure) |

## Artifacts

### JSON Schema
- [smtp-message-schema.json](json-schema/smtp-message-schema.json) — Email message schema (RFC 5321/5322)
- [smtp-session-schema.json](json-schema/smtp-session-schema.json) — SMTP session and commands schema

### JSON Structure
- [smtp-message-structure.json](json-structure/smtp-message-structure.json) — Email message object structure

### JSON-LD
- [smtp-context.jsonld](json-ld/smtp-context.jsonld) — Linked data context mapping SMTP concepts to schema.org

### Examples
- [smtp-session-example.json](examples/smtp-session-example.json) — Complete SMTP session command/response flow
- [smtp-message-example.json](examples/smtp-message-example.json) — RFC 5322 message with MIME attachment

### Vocabulary
- [smtp-vocabulary.yml](vocabulary/smtp-vocabulary.yml) — Complete SMTP vocabulary: commands, response codes, extensions, ports

## Protocol Overview

**Standard Ports:**
- Port 25: Server-to-server transfer (MTA to MTA)
- Port 587: Client submission (MUA to MTA, authentication required)
- Port 465: SMTP over TLS (implicit)

**Key ESMTP Extensions:** STARTTLS, AUTH, SIZE, 8BITMIME, PIPELINING, SMTPUTF8, DSN

## Related Standards

- [RFC 5322](https://datatracker.ietf.org/doc/html/rfc5322) — Internet Message Format
- [RFC 3207](https://datatracker.ietf.org/doc/html/rfc3207) — STARTTLS extension
- [RFC 4954](https://datatracker.ietf.org/doc/html/rfc4954) — AUTH extension
- [RFC 7208](https://datatracker.ietf.org/doc/html/rfc7208) — Sender Policy Framework (SPF)
- [RFC 6376](https://datatracker.ietf.org/doc/html/rfc6376) — DKIM
- [RFC 7489](https://datatracker.ietf.org/doc/html/rfc7489) — DMARC
