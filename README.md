android-openssl
===============

Android NDK openssl build script for original repository(https://www.openssl.org/)

modified version of setenv-android.sh and build script support all architectures in the android NDK

see details : http://wiki.openssl.org/index.php/Android

### Set Up Android NDK
#### Download Android NDK
| Platform | Package URL |
|:--|:--|
| Windows 32-bit | https://dl.google.com/android/repository/android-ndk-r10e-windows-x86.zip |
| Windows 64-bit | https://dl.google.com/android/repository/android-ndk-r10e-windows-x86_64.zip |
| Mac OS X | https://dl.google.com/android/repository/android-ndk-r10e-darwin-x86_64.zip |
| Linux 64-bit (x86) | https://dl.google.com/android/repository/android-ndk-r10e-linux-x86_64.zip |
ex) Mac OS X
```
$ curl -O https://dl.google.com/android/repository/android-ndk-r10e-darwin-x86_64.zip
```

#### Unzip Android NDK
ex) Mac OS X
```
$ unzip android-ndk-r10e-darwin-x86_64.zip
```

#### Set Env ANDROID_NDK_ROOT
```
$ export ANDROID_NDK_ROOT=android-ndk-r10e
```

### Build the OpenSSL
#### Clone the Build Sources
```
$ git clone https://github.com/h-yama37/android-openssl.git
$ cd android-openssl
```

#### Donwload the OpenSSL Sources
ex) openssl-1.0.1
```
$ curl -O https://www.openssl.org/source/openssl-1.0.1t.tar.gz
```

#### Edit OPENSSL_VERSION
ex) openssl-1.0.1
```
$ vim build-all-arch.sh
OPENSSL_VERSION="1.0.1t"
```

#### Build the OpenSSL
```
$ ./build-all-arch.sh
```
