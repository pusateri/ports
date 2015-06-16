# Created by: "Tom Pusateri" <pusateri@bangj.com>
# $FreeBSD$

PKGNAMEPREFIX=	lib
PKGNAMESUFFIX=	content

MAINTAINER=	pusateri@bangj.com
COMMENT=	Shared library build of Atom's Chromium Content module

USE_GITHUB=	nodefault
GH_PROJECT=	libchromiumcontent:libchromiumcontent
GH_ACCOUNT=	atom:libchromiumcontent
GH_TAGNAME=	v43.0.2357.65-atom-2:libchromiumcontent

MASTERDIR=	${.CURDIR}/../chromium
DESCR=		${.CURDIR}/pkg-descr
DISTINFO_FILE=	${.CURDIR}/distinfo

# Apply port patches if any from slave
.if exists(${.CURDIR}/files)
EXTRA_PATCHES+=	${.CURDIR}/files/patch-*
.endif

.include "${MASTERDIR}/Makefile"

