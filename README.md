# SMTP (Simple Mail Transfer Protocol)

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
