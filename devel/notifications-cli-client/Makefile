PORTNAME=	notifications-cli-client
PORTVERSION=	0.4.0
CATEGORIES=	devel
DISTNAME=	${PORTNAME}

MAINTAINER=	dereckson@gmail.com
COMMENT=	Prints notifications to the console
WWW=	https://github.com/nasqueron/notifications-cli-client

LICENSE=	BSD2CLAUSE

RUN_DEPENDS=	${PYTHON_SITELIBDIR}/pika/amqp_object.py:devel/py-pika@${PY_FLAVOR}

USES=		python:3.4+ shebangfix
USE_GITHUB=	yes
GH_ACCOUNT=	nasqueron
GH_TAGNAME=	v${PORTVERSION}

NO_BUILD=	yes
SHEBANG_FILES=	notifications
PLIST_FILES=	bin/notifications

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/notifications ${STAGEDIR}${PREFIX}/bin/

.include <bsd.port.mk>
