# SalamaChat

**Private, resilient messaging for Kenya and East Africa — built on Briar.**

SalamaChat is a community-driven effort to adapt the open-source [Briar](https://briarproject.org/) secure messaging app for people in Kenya and the wider East African region. The aim is to make private communication more approachable through clear English-language onboarding and a distinct Kenyan visual identity—without compromising Briar's security model.

> **Project status:** Early-stage adaptation based on the upstream **Briar 1.5.21 stable release**. The `kenya-theme` branch now includes an initial SalamaChat color system, launcher icon, English-only user-facing copy, and branded app labels. It remains a test adaptation; each build must pass CI and device checks before being treated as release-ready.

## What we want to build

- **A Kenyan identity:** SalamaChat name, app icon, visual theme, and consistent in-app wording.
- **English-only experience:** clear, consistent English throughout the app, with plain-language explanations for setup, contacts, connectivity, and account recovery.
- **Accessible onboarding:** plain-language explanations of accounts, passwords, contact setup, connectivity, and the limits of account recovery.
- **Communication that works in difficult conditions:** retain Briar's peer-to-peer approach and its supported Tor-over-internet, Bluetooth, and local Wi-Fi transports. This matters when connectivity is unreliable or internet access is unavailable.
- **Privacy and security first:** preserve end-to-end encryption and the upstream security design. Do not add advertising, tracking, a central message server, or home-grown cryptography as part of rebranding.
- **Responsible maintenance:** follow stable upstream Briar releases, review security-relevant changes, and test before treating a build as ready for users.

## What SalamaChat is—and is not

SalamaChat is an adaptation project based on Briar, not a new messaging protocol. It does not currently provide a SalamaChat-operated messaging server, and it should not be described as affiliated with the Kenyan government or any institution unless that relationship is formally established.

Briar does not rely on a central server to relay messages. Devices synchronize directly. Internet synchronization uses Tor; nearby devices can synchronize using supported local transports such as Bluetooth or Wi-Fi. These transports have different range and availability constraints, and offline communication is not a guarantee that every contact can be reached at any distance.

Adding a distant contact generally requires exchanging Briar's contact link through another channel first. SalamaChat must explain this clearly rather than imply that users can automatically discover everyone.

## Development plan

1. **Stable baseline:** track the latest official stable Briar release—not alpha, beta, or development commits.
2. **Build and test:** establish a reproducible Android build and record the test results before changing app identity.
3. **Branding:** initial SalamaChat app name, launcher icon, forest-green/cream/gold visual theme, and English user-facing labels are implemented on `kenya-theme`.
4. **English copy:** audit all user-facing strings for consistent, natural English and clear privacy explanations.
5. **Kenyan usability:** test onboarding, contact exchange, data/connectivity explanations, accessibility, and background operation on real Android devices used locally.
6. **Security and release readiness:** review the full diff from upstream, run available checks, document known limitations, and publish builds only after testing.

Changes should be small enough to review, and security-sensitive upstream changes should not be skipped merely to preserve custom branding.

## Branching and upstream policy

- **`master`:** production baseline; keep it aligned with a verified upstream stable release until a tested SalamaChat release is ready.
- **`kenya-theme`:** integration branch for the planned SalamaChat branding, localization, and Kenya/East Africa usability work.
- **Upstream updates:** use official stable release tags. Do not merge alpha, beta, or development commits into the stable baseline just because they are newer.
- **Validation:** a version number or successful source update is not proof that the Android app builds or works. Record build and test results separately.

## Build and contribute

This is an Android project based on Briar's Gradle build. Use the project's Gradle wrapper and follow the build requirements documented by upstream. Do not claim a successful build until it has actually completed.

Contributions are welcome, especially:
- English-language usability feedback from Android users in Kenya and East Africa;
- usability feedback from Android users in Kenya and East Africa;
- accessibility and low-connectivity testing;
- reproducible build and test improvements;
- careful documentation and security review.

Please describe the device, Android version, app version, reproduction steps, and relevant logs when reporting a bug. **Do not publish private contact details, message contents, passwords, or other sensitive data in issues.** For suspected security vulnerabilities, use the responsible disclosure guidance provided by the upstream Briar project rather than posting exploit details publicly.

## Upstream project and licensing

SalamaChat derives from [Briar](https://briarproject.org/) and its source code: [upstream repository](https://github.com/briar/briar). Briar is free and open-source software. This fork must preserve the applicable upstream copyright notices, license terms, and third-party notices. Review the repository's license files before redistributing modified builds.

Upstream project links:
- [Briar website](https://briarproject.org/)
- [Briar user manual](https://briarproject.org/manual/)
- [Briar privacy policy](https://briarproject.org/privacy)
- [Briar source code](https://github.com/briar/briar)

---

**Our goal:** make private, resilient communication easier to understand and use in Kenya and East Africa, while respecting the security work and community behind Briar.
