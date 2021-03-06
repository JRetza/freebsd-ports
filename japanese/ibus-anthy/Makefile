# Created by: Daichi GOTO <daichi@FreeBSD.org>
# $FreeBSD$

PORTNAME=	ibus-anthy
PORTVERSION=	1.2.7
PORTREVISION=	7
CATEGORIES=	japanese
MASTER_SITES=	https://github.com/ibus/ibus-anthy/releases/download/${PORTVERSION}/
PKGNAMEPREFIX=	ja-

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Anthy engine for IBus

BUILD_DEPENDS=	swig3.0:devel/swig30
LIB_DEPENDS=	libanthy.so:japanese/anthy \
		libibus-1.0.so:textproc/ibus
RUN_DEPENDS=	${PYTHON_SITELIBDIR}/gtk-2.0/pynotify/_pynotify.so:devel/py-notify

GNU_CONFIGURE=	yes
USES=		gettext gmake gnome libtool pkgconfig python:2.7
USE_GNOME=	intltool pygtk2
BINARY_ALIAS=	swig=swig3.0

LOCALBASE_REPLACE_FILES= \
		engine/engine.py \
		setup/anthyprefs.py \
		setup/main.py

INCLUDEDIR_REPLACE_FILES= \
		engine/Makefile.am \
		engine/Makefile.in

post-patch:
	cd ${WRKSRC} && \
                ${REINPLACE_CMD} "s,@@LOCALBASE@@,${LOCALBASE},g" \
                ${LOCALBASE_REPLACE_FILES} && \
                ${REINPLACE_CMD} "s,@@INCLUDEDIR@@,${INCLUDEDIR},g" \
                ${INCLUDEDIR_REPLACE_FILES}

post-install:
	${STRIP_CMD} ${STAGEDIR}${PYTHON_SITELIBDIR}/_anthy.so

.include <bsd.port.mk>
