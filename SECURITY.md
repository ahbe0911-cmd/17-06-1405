# Security policy

## API credentials

Never commit, paste into an issue, or attach to a build log any Telegram API ID or API hash.
Build scripts intentionally contain neutral placeholders only. The runtime onboarding stage will
accept the values on the user's device and protect them with Android Keystore-backed encryption.
Until that stage is complete, Telegram sign-in is intentionally unavailable.

## Signing material

Production keystores and their passwords must never be committed. Release signing will use
protected CI secrets, while local development uses a developer-owned debug key outside the
repository.

Service-specific files such as `google-services.json` also stay outside version control.

## Reporting a vulnerability

Do not include account credentials, phone numbers, login codes, session files, or private logs in
public reports. Contact the repository owner privately before disclosing a security issue.
