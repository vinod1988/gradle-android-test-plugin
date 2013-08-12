Gradle Android Unit Testing Plugin
==================================

A Gradle plugin which enables good 'ol fashioned unit tests for Android builds.



Usage
-----

Add the plugin to your `buildscript`'s `dependencies` section:
```groovy
classpath 'com.squareup:gradle-android-test:0.9.+'
```
Apply the `android-test` plugin:
```groovy
apply plugin: 'android-test'
```
Add test-only dependencies using the `testCompile` configuration:
```groovy
testCompile 'junit:junit:4.10'
testCompile 'org.roboelctric:robolectric:2.1.+'
testCompile 'com.squareup:fest-android:1.0.+'
```
Write your tests in `src/test/java/`! You can also add per-build type and per-flavor tests by using
the same folder naming conventions (e.g., `src/testFree/java/`, `src/testDebug/java/`).


Testing
-------

 1. Run `./gradlew install` in the root. This will build the plugin and install it into a local Maven
    repository.
 2. In the `example/` folder, run `../gradlew clean check` to build and run the unit tests.
 3. Open `example/build/test-reports/index.html` in the browser.
