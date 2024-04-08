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

- Google Android
- Chrome
- iOS
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
- wasm
- x86\_64

Legacy support exists for:

- x86
