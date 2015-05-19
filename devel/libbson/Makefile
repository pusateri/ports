# Created by: "Waitman Gobble" <uzimac@da3m0n8t3r.com>
# $FreeBSD$

PORTNAME=	libbson
PORTVERSION=	1.1.4
CATEGORIES=	devel

MAINTAINER=	waitman@waitman.net
COMMENT=	A BSON utility library

USE_GITHUB=	yes
GH_ACCOUNT=	mongodb

USES=		gmake pkgconfig
USE_AUTOTOOLS=	autoconf automake
GNU_CONFIGURE=	yes

USE_LDCONFIG=	yes

pre-configure:
	cd ${WRKSRC} && ./autogen.sh

MAKE_ARGS=      pkgconfigdir="${PREFIX}/libdata/pkgconfig"

.include <bsd.port.mk>
