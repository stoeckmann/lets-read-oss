# Scopes

It is impossible to read every single open source code in existence.
Defining scopes helps to narrow down possible targets. But which
criteria should be used?

## Software

The Let's Read Open Source Software project focuses on widely used
consumer software products. For this, the software products shipped by
gatekeepers as specified by the [EU Digital Markets Act
(DMA)](https://digital-markets-act.ec.europa.eu/gatekeepers_en) are
inspected:

- Chrome
- Google Android
- iOS
- iPadOS
- Messenger
- Safari
- Whatsapp
- Windows PC OS

Next, critical software products identified by
[FOSSEPS](https://joinup.ec.europa.eu/collection/fosseps/news/fosseps-critical-open-source-software-study-report)
are added, if the product in question can be assumed to be run on
consumer devices:

- Firefox
- LibreOffice
- Thunderbird
- VLC

In general, specific versions are ignored. Instead, latest development
versions are used within the project.

## Hardware

The following platforms have been identified to be of relevance:

- arm64
- riscv64
- x86\_64

Legacy support exists for:

- x86

### Reasoning for Hardware Platforms

The platforms arm64 and x86\_64 are supported by Windows. Also the
[build instructions of Chromium](https://chromium.googlesource.com/chromium/src/+/main/docs/windows_build_instructions.md)
for Windows indicate support for both platforms explicitly.

The [rustc platform support](https://doc.rust-lang.org/nightly/rustc/platform-support.html)
lists arm64, x86 and x86\_64 as tier 1.

Android's [bionic](https://android.googlesource.com/platform/bionic/+/refs/heads/main/libc/)
contains explicit optimizations for arm64, riscv64, x86, and x86\_64. Also its
[continuous integration](https://ci.android.com/builds/branches/aosp-main/grid?legacy=1)
covers arm64, riscv64, x86, and x86\_64.
