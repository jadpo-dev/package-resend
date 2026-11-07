# Changelog

## 2.0.0

- changed package `Resend.v2`
- retyped type `SendEmailRequest`
- personal data sent by operation `emails.send`: SendEmailRequest.html to the address its connection gives
- personal data sent by operation `emails.send`: SendEmailRequest.subject to the address its connection gives
- personal data sent by operation `emails.send`: SendEmailRequest.text to the address its connection gives
- personal data sent by operation `emails.send`: Email to the address its connection gives

Checked against Resend's documentation for sending an email. The sender and
recipient are now `Email`, the standard type, so an address is checked as one
before it is sent and counted as contact details; the subject and both bodies
are marked as personal data, so an app's personal-data report lists what it
sends to Resend. Jadpo 0.4.0 refuses a provider package whose email addresses
are plain text, so 1.0.0 can't be installed there. An app that sends through
the `email` capability changes only its package, `Resend.v1` to `Resend.v2`;
one that calls `emails.send` itself gives `from` and `to` as `Email`.

## 1.0.0

- first release

Sends the app's email through Resend's API as the `email` capability: each
email rendered by Jadpo goes as one message, its attachments in base64.
