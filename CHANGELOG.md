# Changelog

## 1.0.1

- personal data sent by operation `emails.send`: SendEmailRequest.from to the address its connection gives
- personal data sent by operation `emails.send`: SendEmailRequest.html to the address its connection gives
- personal data sent by operation `emails.send`: SendEmailRequest.subject to the address its connection gives
- personal data sent by operation `emails.send`: SendEmailRequest.text to the address its connection gives
- personal data sent by operation `emails.send`: SendEmailRequest.to to the address its connection gives

Checked against Resend's documentation for sending an email. The sender and
recipients are now counted as contact details, and the subject and both bodies
as personal data, so an app's personal-data report lists what it sends to
Resend. Nothing an app writes changes.

## 1.0.0

- first release

Sends the app's email through Resend's API as the `email` capability: each
email rendered by Jadpo goes as one message, its attachments in base64.
