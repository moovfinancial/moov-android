## v0.5.0 (2025-03-24)

### Features
- implements `createTapAuthorization`
- updates documentation to include information about `TerminalApplication` registration, which is a prerequisite to get the `TerminalConfig` for initializing the SDK

### :warning: Breaking Changes
- renames `EMVMessage` to `UserInterfaceRequestData` to more accurately reflect the information included in the messages (and matches the name in the EMV spec)
    - converts the base type from an `enum` to a model
    - cleans up some of the type enum values to match the EMV spec better
