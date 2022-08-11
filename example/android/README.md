# TDLib Android example

This is an example of building `TDLib` for Android.
You need a Bash shell on Linux, macOS, or Windows with some common tools, a C++ compiler, cmake, JDK, PHP, and gperf pre-installed.

## Building TDLib for Android

* Run the script `./check-environment.sh` to check that you have all required Unix tools and Java utilities. If the script exits with an error message, install the missing tool.
* Run the script `./fetch-sdk.sh` to download Android SDK to a local directory.
* Run the script `./build-openssl.sh` to download and build OpenSSL for Android.
* Run the script `./build-tdlib.sh` to build TDLib for Android.
* The built libraries are now located in the `tdlib/libs` directory, corresponding Java code is located in the `tdlib/java` directory, and standalone Java documentation can be found in the `tdlib/javadoc` directory. You can also use archives `tdlib/tdlib.zip` and `tdlib/tdlib-debug.zip`, which contain all aforementioned data.

If you already have installed Android SDK and NDK, you can skip the second step and specify existing Android SDK root path and Android NDK version as parameters to the subsequent scripts. Make sure that the SDK includes android-33 platform.

If you want to update TDLib to a newer version, you need to run only the script `./build-tdlib.sh`.

You can specify different OpenSSL version as a third parameter to the script `./build-openssl.sh`. By default OpenSSL 1.1.1 is used because of much smaller binary footprint then newer OpenSSL versions.