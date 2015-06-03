# Created by: "Tom Pusateri" <pusateri@bangj.com>
# $FreeBSD$

PORTNAME=	libchromiumcontent
PORTVERSION=	43.0.2357.65
DISTVERSIONPREFIX=      v
DISTVERSIONSUFFIX=      -atom-1
CATEGORIES=	www

MAINTAINER=	pusateri@bangj.com
COMMENT=	Shared library build of Chromium's Content module

USE_GITHUB=	yes
GH_ACCOUNT=	atom gliaskos:freebsd_chromium
GH_PROJECT=	freebsd-chromium:freebsd_chromium
GH_TAGNAME=	b715e82:freebsd_chromium

CFLAGS+=        -isystem${LOCALBASE}/include

RUN_DEPENDS=	xdg-open:${PORTSDIR}/devel/xdg-utils

BUILD_DEPENDS=	bash:${PORTSDIR}/shells/bash \
		${LOCALBASE}/share/usbids/usb.ids:${PORTSDIR}/misc/usbids \
                yasm:${PORTSDIR}/devel/yasm

LIB_DEPENDS=	libcups.so:${PORTSDIR}/print/cups-client \
		libevent.so:${PORTSDIR}/devel/libevent2 \
		libexif.so:${PORTSDIR}/graphics/libexif \
		libFLAC.so:${PORTSDIR}/audio/flac \
		libharfbuzz.so:${PORTSDIR}/print/harfbuzz \
		libicuuc.so:${PORTSDIR}/devel/icu \
		libjpeg.so:${PORTSDIR}/graphics/jpeg \
		libjsoncpp.so:${PORTSDIR}/devel/jsoncpp \
		libnspr4.so:${PORTSDIR}/devel/nspr \
		libpci.so:${PORTSDIR}/devel/libpci \
		libpng16.so:${PORTSDIR}/graphics/png \
		libre2.so:${PORTSDIR}/devel/re2 \
		libsnappy.so:${PORTSDIR}/archivers/snappy \
		libspeechd.so:${PORTSDIR}/accessibility/speech-dispatcher \
		libspeex.so:${PORTSDIR}/audio/speex \
		libwebp.so:${PORTSDIR}/graphics/webp \
		libxml2.so:${PORTSDIR}/textproc/libxml2 \
		libxslt.so:${PORTSDIR}/textproc/libxslt


USES=		python:2

pre-configure:
	cd ${WRKSRC} && ./autogen.sh

.include <bsd.port.mk>
