moov-android
============

Moov Android SDK

![Maven Central](https://img.shields.io/maven-central/v/io.moov/android-sdk?color=77a5ff) ![Android SDK](https://img.shields.io/badge/android_sdk-28%2B-green?logo=android) ![OpenJDK](https://img.shields.io/badge/jdk-11%2B-red?logo=openjdk)

Documentation
-------------

SDK documentation can be found [here](https://moovfinancial.github.io/moov-android/).

Usage
-----

The Moov Android SDK is published to Maven Central, so ensure it is configured in your `settings.gradle.kts`:

```
dependencyResolutionManagement {
    repositories {
        mavenCentral()
        ...
    }
}
```

Next, register the library in your `gradle/libs.versions.toml`:

```toml
[versions]
moov-sdk = "0.6.1"
...

[libraries]
moov-sdk = { group = "io.moov", name = "android-sdk", version.ref = "moov-sdk" }
...
```

Finally, add the library as a dependency to the module in your application which will be using the SDK:

```
dependencies{
    // moov SDK
    implementation(libs.moov.sdk)

    ...
}
```
