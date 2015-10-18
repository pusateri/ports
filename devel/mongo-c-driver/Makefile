# Created by: "Waitman Gobble" <uzimac@da3m0n8t3r.com>
# $FreeBSD$

PORTNAME=	mongo-c-driver
PORTVERSION=	1.1.9
CATEGORIES=	devel

MAINTAINER=	waitman@waitman.net
COMMENT=	C Driver for MongoDB

LICENSE=	APACHE20

BUILD_DEPENDS=	${LOCALBASE}/lib/libbson-1.0.so:${PORTSDIR}/devel/libbson
LIB_DEPENDS+=	libsasl2.so:${PORTSDIR}/security/cyrus-sasl2

CONFIGURE_ARGS+=	--enable-sasl=yes

USE_GITHUB=	yes
GH_ACCOUNT=	mongodb

USES=		gmake pkgconfig autoreconf libtool
GNU_CONFIGURE=	yes

LDFLAGS+=       -pthread
INSTALL_TARGET=	install-strip
USE_LDCONFIG=	yes

MAKE_ARGS=      pkgconfigdir="${PREFIX}/libdata/pkgconfig"

.include <bsd.port.mk>
