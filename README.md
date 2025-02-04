# moov-android

Moov Android SDK

![GitHub Release](https://img.shields.io/github/v/release/moovfinancial/moov-android)
![Android SDK](https://img.shields.io/badge/android_version-29%2B-green?logo=android)


## Documentation

SDK documentation can be found [here](https://moovfinancial.github.io/moov-android/).

## Usage

To integrate the Moov Android SDK into your project, add Github as a repository to your `settings.gradle.kts`:

```
dependencyResolutionManagement {
    repositories {
        maven(url = "https://maven.pkg.github.com/moovfinancial/moov-android")
        ...
    }
}

```

Next, register the library in your `gradle/libs.versions.toml`:

```toml
[versions]
moov-sdk = "0.1.0"
...

[libraries]
moov-sdk-debug = { group = "io.moov", name = "android-sdk-debug", version.ref = "moov-sdk" }
moov-sdk = { group = "io.moov", name = "android-sdk", version.ref = "moov-sdk" }
...

```

Finally, add the library as a dependency to the module in your application which will be using the SDK:

```
dependencies{
    // moov SDK
    debugImplementation(libs.moov.sdk.debug)
    releaseImplementation(libs.moov.sdk)

    ...
}
```
