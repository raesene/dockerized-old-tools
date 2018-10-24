FROM ubuntu:14.04

LABEL Maintainer="rorym@mccune.org.uk"

RUN apt update && apt install -y libatk1.0-0 libc6 libcairo-gobject2 libcairo2 libdbus-1-3 libdbus-glib-1-2 libfontconfig1 libfreetype6 libgcc1 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libpango-1.0-0 libpangocairo-1.0-0 libstartup-notification0 libstdc++6 libx11-6 libx11-xcb1 libxcb-shm0 libxcb1 libxcomposite1 libxdamage1 libxext6 libxfixes3 libxrender1 libxt6 wget libgtk2.0-dev libasound2 libasound2-data libcanberra0 libdbusmenu-glib4 libdbusmenu-gtk3-4   libogg0 libtdb1 libvorbis0a libvorbisfile3 sound-theme-freedesktop xul-ext-ubufox && rm -rf /var/lib/apt/lists/*

#Set FFox Version Here
ARG version=40.0.3

RUN wget http://ftp.mozilla.org/pub/firefox/releases/${version}/linux-x86_64/en-GB/firefox-${version}.tar.bz2 && tar -xjvf firefox-${version}.tar.bz2 && rm -f firefox-${version}.tar.bz2

WORKDIR /firefox

ENTRYPOINT ["./firefox"]