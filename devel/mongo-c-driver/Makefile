# Created by: "Waitman Gobble" <uzimac@da3m0n8t3r.com>
# $FreeBSD: head/devel/mongo-c-driver/Makefile 381618 2015-03-19 16:44:57Z bdrewery $

PORTNAME=	mongo-c-driver
PORTVERSION=	1.1.4
CATEGORIES=	devel
MASTER_SITES=	GHL
DISTNAME=	${GH_ACCOUNT}-${GH_PROJECT}-${PORTVERSION}

MAINTAINER=	waitman@waitman.net
COMMENT=	C Driver for MongoDB

BUILD_DEPENDS=	${LOCALBASE}/lib/libbson-1.0.so:${PORTSDIR}/devel/libbson

USE_GITHUB=	yes
GH_ACCOUNT=	mongodb
GH_PROJECT=	${PORTNAME}
#GH_TAGNAME=	${PORTVERSION}

WRKSRC=		${WRKDIR}/mongodb-mongo-c-driver-0678587
USES=		gmake pkgconfig
USE_AUTOTOOLS=	autoconf automake
GNU_CONFIGURE=	yes

USE_LDCONFIG=	yes

pre-configure:
	cd ${WRKSRC} && ./autogen.sh

.include <bsd.port.mk>