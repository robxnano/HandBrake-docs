---
Type:            article
Title:           Installing dependencies on FreeBSD
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

Installing dependencies on FreeBSD
==================================

The following instructions are for [FreeBSD](https://www.freebsd.org) 12 and 13.

Basic requirements to run commands:

- sudo (for normal user accounts)

Dependencies:

- autoconf
- automake
- bzip2
- cmake
- flac
- fontconfig
- freetype2
- fribidi
- git
- gmake
- harfbuzz
- jansson
- lame
- libass
- libiconv
- libjpeg-turbo
- libogg
- libsamplerate
- libtheora
- libtool
- libvorbis
- libvpx
- libx264
- libxml2
- lzma
- m4
- meson
- nasm
- ninja
- opus
- patch
- pkgconf
- python
- speex

Intel Quick Sync Video dependencies (optional):

- intel-media-sdk

Graphical interface dependencies:

- atk
- cairo
- dbus
- dbus-glib
- desktop-file-utils
- gdk-pixbuf2
- gettext
- glib
- gstreamer1-plugins-gdkpixbuf
- gtk3
- pango

Install dependencies.

    sudo pkg install autoconf automake bzip2 cmake flac fontconfig freetype2 fribidi git lzma gmake harfbuzz jansson lame libass libiconv libjpeg-turbo libogg libsamplerate libtheora libtool libvorbis libvpx libx264 libxml2 m4 meson nasm ninja opus patch pkgconf python speex

To build with Intel Quick Sync Video support, install the QSV dependencies.

    sudo pkg install intel-media-sdk

To build the GTK [GUI](abbr:Graphical User Interface), install the graphical interface dependencies.

    sudo pkg install atk cairo dbus dbus-glib desktop-file-utils gdk-pixbuf2 gettext glib gstreamer1-plugins-gdkpixbuf gtk3 pango

FreeBSD is now prepared to build HandBrake. See [Building HandBrake for BSD](build-bsd.html) for further instructions.
