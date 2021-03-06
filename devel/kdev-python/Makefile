# $FreeBSD$

PORTNAME=	kdev-python
DISTVERSION=	5.4.4
CATEGORIES=	devel kde
MASTER_SITES=	KDE/stable/kdevelop/${DISTVERSION}/src
DIST_SUBDIR=	KDE/kdevelop

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Python support for KDevelop

BUILD_DEPENDS=	kdev-pg-qt:devel/kdevelop-pg-qt
LIB_DEPENDS=	libkdevcmakecommon.so:devel/kdevelop

USES=		cmake compiler:c++11-lib kde:5 python:3.4+ qt:5 tar:xz
USE_KDE=	attica auth codecs completion config configwidgets coreaddons \
		ecm i18n itemmodels jobwidgets kio newstuff parts service \
		sonnet texteditor textwidgets threadweaver widgetsaddons xmlgui
USE_QT=		concurrent core dbus gui network widgets xml \
		buildtools_build qmake_build

# Versioning values, to reduce plist churn (match with devel/kdevelop)
PLATFORM_VER=	32
PLIST_SUB+=	PLATFORM_VER=${PLATFORM_VER}

# Does not build with jobs.
MAKE_JOBS_UNSAFE=	yes

.include <bsd.port.mk>
