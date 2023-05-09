---
Type:            article
Title:           Installing dependencies on OpenSUSE
Project:         HandBrake
Project_URL:     https://handbrake.fr/
Project_Version: Latest
Language:        English
Language_Code:   en
Authors:         [ Rob (robxnano) ]
Copyright:       2023 HandBrake Team
License:         Creative Commons Attribution-ShareAlike 4.0 International
License_Abbr:    CC BY-SA 4.0
License_URL:     https://handbrake.fr/docs/license.html
---

Installing dependencies on OpenSUSE
=================================

The following instructions are for [OpenSUSE](https://opensuse.org) Leap 15.4 and Tumbleweed.

Basic requirements to run commands:

- sudo (for normal user accounts)

Dependencies:

- AppStream
- autoconf
- automake
- binutils
- bzip2
- cmake
- fontconfig-devel
- freetype-devel
- fribidi-devel
- gcc-c++
- git
- gzip
- harfbuzz-devel
- lbzip2
- libass-devel
- libjansson-devel
- libjpeg8-devel
- libmp3lame-devel
- libnuma-devel
- libogg-devel
- libopus-devel
- libsamplerate-devel
- libtheora-devel
- libtool
- libvorbis-devel
- libxml2-devel
- libvpx-devel
- libzimg-devel
- m4
- make
- meson
- nasm
- ninja
- patch
- pkg-config
- python
- speex-devel
- tar
- xz-devel
- zlib-devel

Additional dependencies not available in the base repository:

- libx264-devel [Packman]

Intel Quick Sync Video dependencies (optional):

- libva-devel
- libdrm-devel

Graphical interface dependencies:

- dbus-glib-devel
- gstreamer1-devel
- gstreamer1-plugins-base-devel
- gstreamer1-libav
- gtk3-devel
- libgudev1-devel

Install dependencies.

    sudo zypper in AppStream autoconf automake binutils bzip2 cmake fontconfig-devel freetype-devel fribidi-devel gcc-c++ git gzip harfbuzz-devel lbzip2 libass-devel libjansson-devel libjpeg8-devel libmp3lame-devel libnuma-devel libogg-devel libopus-devel libsamplerate-devel libtheora-devel libtool libvorbis-devel libxml2-devel libvpx-devel libzimg-devel m4 make meson nasm ninja patch pkg-config python speex-devel tar xz-devel zlib-devel
    
Install the [Packman](https://en.opensuse.org/Additional_package_repositories) Essentials repository and related additional dependencies.

    # OpenSUSE Leap
    sudo zypper ar -cfp 90 'https://ftp.fau.de/packman/suse/openSUSE_Leap_$releasever/Essentials' packman-essentials
    
    # OpenSUSE Tumbleweed
    sudo zypper ar -cfp 90 'https://ftp.fau.de/packman/suse/openSUSE_Tumbleweed/Essentials' packman-essentials
    
    sudo zypper dup --from packman-essentials --allow-vendor-change
    sudo zypper install libx264-devel

To build with Intel Quick Sync Video support, install the QSV dependencies.

    sudo zypper install libva-devel libdrm-devel

To build the GTK [GUI](abbr:Graphical User Interface), install the graphical interface dependencies.

    sudo zypper install dbus-1-glib-devel gstreamer-devel gstreamer-plugins-base-devel gstreamer-plugins-libav gtk3-devel libgudev-1_0-devel

OpenSUSE is now prepared to build HandBrake. See [Building HandBrake for Linux](build-linux.html) for further instructions.
