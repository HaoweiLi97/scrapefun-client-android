<div align="center">
  <img src="./docs/images/client-icon.png" alt="ScrapeFun Client" width="80" />
  <h1>ScrapeFun Client for Android</h1>
  <p><a href="./README.md">简体中文</a> · <strong>English</strong></p>
  <p><a href="https://scrapefun.com/?lang=en">Website</a> · <a href="https://github.com/HaoweiLi97/scrapefun-client-android/releases/latest">Download</a> · <a href="https://github.com/HaoweiLi97/scrapefun-client-android/releases">All releases</a> · <a href="https://scrapefun.com/?lang=en#/docs">Documentation</a></p>
</div>

> Updated: 2026-11-03. Versions and assets below are the stable releases checked on this date. Follow the corresponding Release for later changes.

Android client for connecting to an existing ScrapeFun Server and browsing and playing media on a mobile device. Server can run in Docker, on macOS, or on Windows; Server manages libraries and users.

**Updating:** 0.5.2 retains the official 0.5.0 signing identity and can update 0.5.0 in place while preserving data. Clients from before 0.5.0 that use the previous signing identity cannot be updated in place; do not uninstall the existing app to bypass a signing mismatch.

0.5.2 fixes danmaku jitter while videos load, pause or play.

0.5.1 improves remote connection stability during long playback sessions and after inactivity, maintaining connections while the app runs and automatically attempting to reconnect when a connection stops responding.

## Downloads and device architecture

| Item | Current stable release |
| --- | --- |
| Version | [0.5.2](https://github.com/HaoweiLi97/scrapefun-client-android/releases/tag/v0.5.2) |
| 64-bit ARM | `scrapefun-android-0.5.2-stable-arm64-v8a.apk` |
| 32-bit ARM | `scrapefun-android-0.5.2-stable-armeabi-v7a.apk` |
| Checksums and update information | `.sha256`, `SHA256SUMS`, release manifest |

Get the APK matching your device ABI from the [stable download page](https://github.com/HaoweiLi97/scrapefun-client-android/releases/latest). This release does not provide x86 / x86_64 packages. Android version requirements follow the system installer's checks and the release information.

## Installation and connection

1. Download the official APK and follow Android's prompts to allow installation from the current download source.
2. After installation, open ScrapeFun and enter the Server address, such as `http://192.168.1.10:8096`.
3. Sign in with your Server account.

On a phone, `localhost` refers to the phone itself. For LAN access, use Server's actual IP and port and confirm that the devices can reach each other.

## Updates and data

The app can check Releases and verify the published checksum information, then invoke Android's system installer. You can also manually install a newer APK with the same signature and application ID over the current version.

If Android reports a signature mismatch, do not immediately uninstall to work around it. Verify the package source, save local configuration, and contact support first. Uninstalling may clear local client settings. Back up Server's business data separately on Server.

## File verification

On Linux, run in the directory containing the APK and `SHA256SUMS`:

```bash
sha256sum --check --ignore-missing SHA256SUMS
```

On macOS, calculate the digest with `shasum -a 256 FILE.apk` and compare it with that APK's `.sha256` file. File verification does not replace Android installation signature checks.

<details>
<summary>Troubleshooting</summary>

For installation issues, include Android version, device ABI, complete APK filename, and system message. For connection or playback problems, also include Server version and minimal reproduction steps.

</details>

## Support and licensing

This repository provides platform installation instructions and official release assets. Submit usage questions and feature requests to the [main repository Issues](https://github.com/HaoweiLi97/ScrapeFun/issues). For accounts, activation, or private logs, contact `scrapefun@outlook.com`. Report security issues privately according to the [security instructions](./SECURITY.en.md).

See the new [commercial license statement](./LICENSE.en.txt) and full [software license agreement](./EULA.en.md). Ordinary personal, household, and internal organizational use is allowed. Pro requires a valid entitlement. Software redistribution, resale, customer delivery, and paid hosting require separate written authorization. The statement does not retroactively change existing licenses; existing assets follow their supplied licenses, and third-party components retain their own licenses.

[Releases and compatibility](https://github.com/HaoweiLi97/ScrapeFun/blob/main/RELEASE_POLICY.en.md) · [Third-party components](https://github.com/HaoweiLi97/ScrapeFun/blob/main/THIRD_PARTY_NOTICES.en.md) · [Support](./SUPPORT.en.md)
