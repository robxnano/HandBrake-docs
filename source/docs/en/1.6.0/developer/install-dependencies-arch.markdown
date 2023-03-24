---
Type:            article
Title:           Installing dependencies on Arch
Project:         HandBrake
Project_URL:     https://handbrake.fr/
Project_Version: 1.6.0
Language:        English
Language_Code:   en
Authors:         [ Bradley Sepos <bradley@bradleysepos.com> (BradleyS) ]
Copyright:       2023 HandBrake Team
License:         Creative Commons Attribution-ShareAlike 4.0 International
License_Abbr:    CC BY-SA 4.0
License_URL:     https://handbrake.fr/docs/license.html
---

Installing dependencies on Arch
===============================

The following instructions are for [Arch](https://www.archlinux.org) 2023.03.01.

Basic requirements to run commands:

- sudo (for normal user accounts)

Dependencies:

- base-devel
- cmake
- flac
- fontconfig
- freetype2
- fribidi
- git
- harfbuzz
- jansson
- lame
- libass
- libbluray
- libjpeg-turbo
- libogg
- libsamplerate
- libtheora
- libvorbis
- libvpx
- libxml2
- meson
- nasm
- ninja
- numactl
- opus
- python2
- speex
- x264
- xz

Intel Quick Sync Video dependencies (optional):

- libva
- libdrm

Graphical interface dependencies:

- dbus-glib
- gstreamer
- gst-libav
- gst-plugins-base
- gtk3
- intltool
- libgudev

Install dependencies.

    sudo pacman -Syu base-devel cmake flac fontconfig freetype2 fribidi git harfbuzz jansson lame libass libbluray libjpeg-turbo libogg libsamplerate libtheora libvorbis libvpx libxml2 meson nasm ninja numactl opus python2 speex x264 xz

To build with Intel Quick Sync Video support, install the QSV dependencies.

    sudo pacman -Syu libva libdrm

To build the GTK [GUI](abbr:Graphical User Interface), install the graphical interface dependencies.

    sudo pacman -Syu dbus-glib gstreamer gst-libav gst-plugins-base gtk3 intltool libgudev

Arch is now prepared to build HandBrake. See [Building HandBrake for Linux](build-linux.html) for further instructions.
