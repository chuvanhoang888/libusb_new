# libusb_new

Dart wrapper via `dart:ffi` for https://github.com/libusb/libusb 
Dart wrapper via `libusb` for https://github.com/woodemi/libusb.dart
Dart wrapper via `libusb` for https://github.com/wfinken/libusb.dart

## Environment

- Windows(10)
- macOS
- Linux(Ubuntu 18.04 LTS)

## Usage

Checkout example

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: http://example.com/issues/replaceme

## Build

### Prepare llvm(9+)

- Windows: `winget install -e --id LLVM.LLVM`
- macOS: `brew install llvm`
- Linux: `sudo apt install libclang-10-dev`

### Build libusb_xxx.dart

- Windows/Linux:

```
pub run ffigen
move lib/libusb_new.dart lib/libusb64.dart
```

Refactor `timeval` to `timeval64`

- macOS:

```
pub run ffigen
mv lib/libusb_new.dart lib/libusb32.dart
```

Refactor `timeval` to `timeval32`

## Contribute

### Prepare libusb.h

Download `xxx` verion from `https://github.com/libusb/libusb/releases` and extract `libusb.h`

### Prepare libusb-1.0 dynamic library

- Windows:

Download `xxx` version from https://github.com/libusb/libusb/releases and extract

```
copy libusb-1.0.23\MS64\dll\libusb-1.0.dll libusb-1.0\
```

- macOS:

Download `xxx` version from https://homebrew.bintray.com/bottles/libusb-1.0.23.catalina.bottle.tar.gz and extract

```
cp libusb/1.0.23/lib/libusb-1.0.dylib libusb-1.0/
```

- Linux:

Download `xxx` version from http://old.kali.org/kali/pool/main/libu/libusb-1.0/ and install

```
cp /lib/x86_64-linux-gnu/libusb-1.0.so.0.xxx libusb-1.0/libusb-1.0.so
```