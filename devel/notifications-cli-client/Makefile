# Created by: Dereckson <dereckson@gmail.com>
# $FreeBSD$
#
# This port is a part of Nasqueron operations FreeBSD internal ports tree.

PORTNAME=	notifications-cli-client
PORTVERSION=0.3.0
CATEGORIES=	devel
DISTNAME=	${PORTNAME}

MAINTAINER=	dereckson@gmail.com
COMMENT=	Prints notifications to the console

LICENSE=	BSD2CLAUSE

RUN_DEPENDS=	${PYTHON_SITELIBDIR}/pika/amqp_object.py:${PORTSDIR}/devel/py-pika

USE_GITHUB=	yes
GH_ACCOUNT=	nasqueron
GH_TAGNAME=	v${PORTVERSION}

USES=		python:3.4+
NO_BUILD=	yes
PLIST_FILES=	bin/notifications

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/notifications ${STAGEDIR}${PREFIX}/bin/

.include <bsd.port.mk>
