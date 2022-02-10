<h1 align="center">GhostJS - To Evaluate JavaScript in Android</h1>

<p align="center">
    <a href="https://jitpack.io/#whoisjeeva/ghostjs"><img src="https://img.shields.io/jitpack/v/github/whoisjeeva/ghostjs?style=for-the-badge" alt="Release"></a>
    <a href="https://travis-ci.com/whoisjeeva/ghostjs"><img src="https://img.shields.io/travis/com/whoisjeeva/ghostjs/master?style=for-the-badge" alt="Build Status"></a>
    <a href="https://github.com/whoisjeeva/ghostjs/blob/master/LICENSE.txt"><img src="https://img.shields.io/github/license/whoisjeeva/ghostjs.svg?style=for-the-badge" alt="License"></a>
<!--     <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/whoisjeeva/ghostjs?logo=GitHub&style=for-the-badge"> -->
    <img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/whoisjeeva/ghostjs?logo=GitHub&style=for-the-badge">
    <a href="https://github.com/whoisjeeva/ghostjs/issues"><img alt="GitHub open issues" src="https://img.shields.io/github/issues/whoisjeeva/ghostjs?style=for-the-badge"></a>
</p>

### Getting Started

Add it in your root build.gradle at the end of repositories

```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

Add the dependency

```gradle
implementation "com.github.whoisjeeva:ghostjs:$ghost_version"
```

Create an icecream instance

```kotlin
val ghostjs = Ghostjs()
```

### Usage

```kotlin
ghostjs.executeFile("test.js")
scope.launch {
    val output: String? = ghostjs.eval("""return dio;""")
    Log.d("Ghostjs", output.toString())
}
```

```kotlin
ghostjs.loadUrl("https://www.google.com")
```
