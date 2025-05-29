v0.8.2 (2025-05-29)

### Misc
- modifications to JWKS public keys

v0.8.1 (2025-05-28)

### Documentation

- Minor updates to kdoc

v0.8.0 (2025-05-28)

### Features

- Adds the ability to create a tap transfer

### Fixes

- fix for issue where createTapAuthorization would always return UnknownError

v0.7.0 (2025-05-13)

### :warning: Breaking Changes

-	refactor of terminal configuration to match the updated model returned by the Moov API

v0.6.2 (2025-05-13)
-------------------

- use Application context

v0.6.1 (2025-04-29)
-------------------

-	minor bugfixes in coroutine processing

v0.6.0 (2025-04-21)
-------------------

### :warning: Breaking Changes

-	refactor of concurrency handling, including the `Terminal` API for a better developer experience

v0.5.1 (2025-03-24)
-------------------

### Documentation

-	updates verbiage of the `TerminalApplication` instructions

v0.5.0 (2025-03-24)
-------------------

### Features

-	implements `createTapAuthorization`

### Documentation

-	updates documentation to include information about `TerminalApplication` registration, which is a prerequisite to get the `TerminalConfig` for initializing the SDK

### :warning: Breaking Changes

-	renames `EMVMessage` to `UserInterfaceRequestData` to more accurately reflect the information included in the messages (and matches the name in the EMV spec)
	-	converts the base type from an `enum` to a model, containing a `type` among the other required fields
	-	cleans up some of the type enum values to match the EMV spec better
