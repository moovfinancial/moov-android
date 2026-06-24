# v0.23.1 (2026-06-24)

## Misc

- dependency upgrades (bugfix/security)

# v0.23.0 (2026-06-23)

## :warning: Breaking Changes

- `TapAuthorizationParams` now takes a single `TapAmount` instead of separate `amount`, `currency`, and `surchargeAmount` parameters

## :sparkles: Features

- tip support for tap authorizations and transfers
- tip and surcharge are now recorded on the resulting transfer via `amountDetails`

# v0.22.1 (2026-06-16)

## Misc

- dependency upgrades (bugfix/security)

# v0.22.0 (2026-04-28)

## :sparkles: Features
- surcharge fee support

## Misc
- major dependency upgrades
- moov kotlin [v0.7.0](https://central.sonatype.com/artifact/io.moov/kotlin-sdk/0.7.0)

# v0.21.2 (2026-03-03)

## :bug: Fixes

- fixes a crash caused by a dependency update

# v0.21.1 (2026-02-19)

- dependency upgrades (bugfix/security)

# v0.21.0 (2026-02-16)

## :warning: Breaking Changes

- Replaced `UUID` types with `MID` type

# v0.20.0 (2026-01-20)

## :sparkles: Test mode

- test mode support

# v0.19.0 (2026-01-09)

## :sparkles: Features

- handle attestation failures by including an error tracking ID, enabling Moov support to assist with issue investigation.

# v0.18.2 (2026-01-09)

## Misc

- dependency upgrades (bugfix/security)

# v0.18.1 (2025-12-23)

- improve attestation failure handling

# v0.18.0 (2025-12-11)

- handle attestation failures during authorization sessions

# v0.17.3 (2025-11-19)

- improvement of the fix in v0.17.1

# v0.17.1 (2025-11-18)

- bugfix in [createTerminal](https://moovfinancial.github.io/moov-android/moov-android/io.moov.sdk/-moov-s-d-k/-factory/index.html#859028225%2FFunctions%2F275946699)

# v0.17.0 (2025-11-07)

## :sparkles: Features

- Handle attestation failures during terminal create
  - New terminal creation result: DeviceAttestationFailed, learn [more](https://moovfinancial.github.io/moov-android/moov-android/io.moov.sdk.models/-terminal-creation-result/-device-attestation-failed/index.html) in the documentation

# v0.16.0 (2025-11-04)

## Misc

- dependency upgrades (bugfix/security)

# v0.15.2 (2025-10-29)

## Misc

- dependency upgrades (bugfix/security)


# v0.15.1 (2025-10-28)

## Misc

- dependency upgrades (bugfix/security)

# v0.15.0 (2025-09-25)

## :sparkles: Features

- add OpenTelemetry
- automatic discovery of terminal application

# v0.14.1 (2025-09-22)

## Misc

- dependency upgrades (bugfix/security)

# v0.14.0 (2025-09-17)

## :sparkles: Features
- 16KB page size for native libraries

## Misc
- upgrade dependencies

# v0.13.0 (2025-09-12)

## :sparkles: Features
- adds new type: `CreateTapAuthorizationEvent.AuthorizationFailed` to indicate a
  backend failure to process. This replaces several instances where an
  `UnknownFailure` would previously be emitted

## :note: Documentation
- fully document Tap events
- document error handling and `SDKLogger` usage

# v0.12.2 (2025-07-30)

## :bug: Fixes

- fixes for AMEX transaction processing
- initialization fixes
- dependency upgrades

# v0.12.1 (2025-07-16)

## :bug: Fixes

- fixes to event mapping for CDCVM

# v0.12.0 (2025-06-26)

## :warning: Breaking Changes

-	refactor of tap authorization events to simplify

# v0.11.0 (2025-06-18)

## :sparkles: Features

- add logger to capture production crash logs
- add production endpoint support

# v0.10.0 (2025-06-09)

## Other
- EMV kernel upgrade

# v0.9.0 (2025-06-05)

## Features
- adds first-class support for late initialization of the SDK

# v0.8.2 (2025-05-29)

## Misc
- modifications to JWKS public keys

# v0.8.1 (2025-05-28)

## Documentation

- Minor updates to kdoc

# v0.8.0 (2025-05-28)

## Features

- Adds the ability to create a tap transfer

## Fixes

- fix for issue where createTapAuthorization would always return UnknownError

# v0.7.0 (2025-05-13)

## :warning: Breaking Changes

-	refactor of terminal configuration to match the updated model returned by the Moov API

# v0.6.2 (2025-05-13)

- use Application context

# v0.6.1 (2025-04-29)

-	minor bugfixes in coroutine processing

# v0.6.0 (2025-04-21)

## :warning: Breaking Changes

-	refactor of concurrency handling, including the `Terminal` API for a better developer experience

# v0.5.1 (2025-03-24)

## Documentation

-	updates verbiage of the `TerminalApplication` instructions

# v0.5.0 (2025-03-24)

## Features

-	implements `createTapAuthorization`

## Documentation

-	updates documentation to include information about `TerminalApplication` registration, which is a prerequisite to get the `TerminalConfig` for initializing the SDK

## :warning: Breaking Changes

-	renames `EMVMessage` to `UserInterfaceRequestData` to more accurately reflect the information included in the messages (and matches the name in the EMV spec)
	-	converts the base type from an `enum` to a model, containing a `type` among the other required fields
	-	cleans up some of the type enum values to match the EMV spec better
