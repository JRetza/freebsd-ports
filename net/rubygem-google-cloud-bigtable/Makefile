# Created by: Po-Chuan Hsieh <sunpoet@FreeBSD.org>
# $FreeBSD$

PORTNAME=	google-cloud-bigtable
PORTVERSION=	0.8.0
CATEGORIES=	net rubygems
MASTER_SITES=	RG

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Official library for Cloud Bigtable API

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	rubygem-google-cloud-core>=1.1<2:net/rubygem-google-cloud-core \
		rubygem-google-gax>=1.8<2:devel/rubygem-google-gax \
		rubygem-googleapis-common-protos-types>=1.0.4<2.0:devel/rubygem-googleapis-common-protos-types \
		rubygem-googleapis-common-protos>=1.3.9<2.0:devel/rubygem-googleapis-common-protos \
		rubygem-grpc-google-iam-v1>=0.6.9<0.7:devel/rubygem-grpc-google-iam-v1

USES=		gem
USE_RUBY=	yes

NO_ARCH=	yes

.include <bsd.port.mk>
