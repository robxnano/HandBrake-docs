---
Type:            article
Title:           Installing dependencies on Ubuntu
Project:         HandBrake
Project_URL:     https://handbrake.fr/
Project_Version: Latest
Language:        English
Language_Code:   en
Authors:         [ Bradley Sepos <bradley@bradleysepos.com> (BradleyS) ]
Copyright:       2023 HandBrake Team
License:         Creative Commons Attribution-ShareAlike 4.0 International
License_Abbr:    CC BY-SA 4.0
License_URL:     https://handbrake.fr/docs/license.html
---

Installing dependencies on Ubuntu
=================================

The following instructions are for [Ubuntu](https://www.ubuntu.com) 22.04 (Jammy Jellyfish) and 20.04 (Focal Fossa).

Basic requirements to run commands:

- sudo (for normal user accounts)

Dependencies:

- autoconf
- automake
- build-essential
- cmake
- git
- libass-dev
- libbz2-dev
- libfontconfig-dev
- libfreetype-dev
- libfribidi-dev
- libharfbuzz-dev
- libjansson-dev
- liblzma-dev
- libmp3lame-dev
- libnuma-dev
- libogg-dev
- libopus-dev
- libsamplerate0-dev
- libspeex-dev
- libtheora-dev
- libtool
- libtool-bin
- libturbojpeg0-dev
- libvorbis-dev
- libx264-dev
- libxml2-dev
- libvpx-dev
- m4
- make
- meson
- nasm
- ninja-build
- patch
- pkg-config
- tar
- zlib1g-dev

Intel Quick Sync Video dependencies (optional):

- libva-dev
- libdrm-dev

Dolby Vision dependencies (optional):

- cargo
- cargo-c
- rustc

Graphical interface dependencies:

- appstream
- desktop-file-utils
- gettext
- gstreamer1.0-libav
- gstreamer1.0-plugins-good
- libgstreamer-plugins-base1.0-dev
- libgtk-3-dev

Install dependencies.

    sudo apt-get update
    sudo apt-get install autoconf automake build-essential cmake git libass-dev libbz2-dev libfontconfig-dev libfreetype-dev libfribidi-dev libharfbuzz-dev libjansson-dev liblzma-dev libmp3lame-dev libnuma-dev libogg-dev libopus-dev libsamplerate0-dev libspeex-dev libtheora-dev libtool libtool-bin libturbojpeg0-dev libvorbis-dev libx264-dev libxml2-dev libvpx-dev m4 make meson nasm ninja-build patch pkg-config tar zlib1g-dev

To build with Intel Quick Sync Video support, install the QSV dependencies.

    sudo apt-get install libva-dev libdrm-dev

To build with Dolby Vision support, install the libdovi dependencies.

    # Ubuntu 22.04 and below:
    sudo apt-get install libssl-dev
    curl -sSf https://sh.rustup.rs | sh -s -- --profile minimal
    source "$HOME/.cargo/env"
    cargo install cargo-c

    # Ubuntu 23.04 and above:
    sudo apt-get install cargo cargo-c rustc

To build the GTK [GUI](abbr:Graphical User Interface), install the graphical interface dependencies.

    sudo apt-get install appstream desktop-file-utils gettext gstreamer1.0-libav gstreamer1.0-plugins-good libgstreamer-plugins-base1.0-dev libgtk-3-dev

Ubuntu is now prepared to build HandBrake. See [Building HandBrake for Linux](build-linux.html) for further instructions.
