---
Type:            article
Title:           Installing dependencies on Debian
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

Installing dependencies on Debian
=================================

The following instructions are for [Debian](https://www.debian.org) 11 Bullseye.

Basic requirements to run commands:

- curl
- sudo (for normal user accounts)

Dependencies:

- appstream
- autoconf
- automake
- autopoint
- build-essential
- cmake
- git
- libass-dev
- libbz2-dev
- libfontconfig1-dev
- libfreetype6-dev
- libfribidi-dev
- libharfbuzz-dev
- libjansson-dev
- liblzma-dev
- libmp3lame-dev
- libnuma-dev
- libogg-dev
- libopus-dev
- libsamplerate-dev
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
- python
- tar
- zlib1g-dev

Intel Quick Sync Video dependencies (optional):

- libva-dev
- libdrm-dev

Graphical interface dependencies:

- intltool
- libdbus-glib-1-dev
- libglib2.0-dev
- libgstreamer1.0-dev
- libgstreamer-plugins-base1.0-dev
- libgtk-3-dev
- libgudev-1.0-dev

Install dependencies.

    sudo apt-get update
    sudo apt-get install appstream autoconf automake autopoint build-essential cmake git libass-dev libbz2-dev libfontconfig1-dev libfreetype6-dev libfribidi-dev libharfbuzz-dev libjansson-dev liblzma-dev libmp3lame-dev libnuma-dev libogg-dev libopus-dev libsamplerate-dev libspeex-dev libtheora-dev libtool libtool-bin libturbojpeg0-dev libvorbis-dev libx264-dev libxml2-dev libvpx-dev m4 make meson nasm ninja-build patch pkg-config python tar zlib1g-dev

To build with Intel Quick Sync Video support, install the QSV dependencies.

    sudo apt-get install libva-dev libdrm-dev

To build the GTK [GUI](abbr:Graphical User Interface), install the graphical interface dependencies.

    sudo apt-get install intltool libdbus-glib-1-dev libglib2.0-dev libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgtk-3-dev libgudev-1.0-dev

Debian is now prepared to build HandBrake. See [Building HandBrake for Linux](build-linux.html) for further instructions.
