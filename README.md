# RDR1 Arabic — Official Update Channel

قناة التحديثات الرسمية لتطبيق **«مثبّت تعريب RDR1»** (تعريب Red Dead Redemption
للأندرويد — تعريب ونشر: حسن).

This repository is the official update channel for the **RDR Arabic Installer**
Android app. It contains no game files — only the signed update manifest and,
for future localization releases, the small entry-level update patches the
manifest points to.

## version.json

`version.json` is the update manifest the app fetches from:

```
https://raw.githubusercontent.com/ha8083938-create/rdr1-arabic-updates/main/version.json
```

It is **RSA-signed** (SHA256withRSA) with the installer key. The app verifies
the signature against the embedded installer certificate
(SHA-256 `FC846A44F273C740FA2EC34C244B1A7DA519692FE26158179F40683DDEA0E38A`)
before trusting any field, and verifies the SHA-256 of every downloaded patch
and of every patched game file. A modified or re-hosted manifest is rejected
by the app.

## Trust / الأصالة

- The only official source of the installer app and its updates is Hassan's
  official channel. Copies of the app signed with any other key are
  unofficial — the app itself detects that and disables its update channel.
- Localization updates install **in place** over an install made by this
  installer (same signing key): no uninstall, no save loss.

المصدر الرسمي الوحيد للتطبيق وتحديثاته هو قناة حسن الرسمية. أي نسخة من
التطبيق موقّعة بمفتاح آخر ليست أصلية — والتطبيق نفسه يكشف ذلك ويعطّل
قناة التحديثات فيها.
