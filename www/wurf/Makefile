PORTNAME=	wurf
PORTVERSION=	1.0.0
CATEGORIES=	www

MAINTAINER=	dereckson@gmail.com
COMMENT=	Web Upload and Receive Files, an ad-hoc single file webserver
WWW=	https://agora.nasqueron.org/wurf

LICENSE=	GPLv2+

USES=	python shebangfix

USE_GITHUB=	yes
GH_ACCOUNT=	nasqueron
GH_TAGNAME=	v${PORTVERSION}

NO_BUILD=	yes
SHEBANG_FILES=	src/wurf.py
PLIST_FILES=	bin/wurf bin/woof share/man/man1/wurf.1.gz

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/src/wurf.py ${STAGEDIR}${PREFIX}/bin/wurf
	@(cd ${STAGEDIR}${PREFIX}/bin && ${LN} -s wurf woof)
	${INSTALL_MAN} ${WRKSRC}/doc/wurf.1 ${STAGEDIR}${PREFIX}/share/man/man1

.include <bsd.port.mk>
