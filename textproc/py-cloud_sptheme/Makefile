# Created by: Horia Racoviceanu <horia@racoviceanu.com>
# $FreeBSD$

PORTNAME=	cloud_sptheme
PORTVERSION=	1.9.4
CATEGORIES=	textproc python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Sphinx theme

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

# sphinx.util.fileutil was added in sphinx 1.5
BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}sphinx>=1.5:textproc/py-sphinx@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}sphinxcontrib-fulltoc>=1.1:textproc/py-sphinxcontrib-fulltoc@${PY_FLAVOR}
RUN_DEPENDS:=	${BUILD_DEPENDS}

USES=		python
USE_PYTHON=	autoplist distutils
PYDISTUTILS_BUILDARGS=	build_sphinx -E
NO_ARCH=	yes

DOCSDIR=	${PREFIX}/share/doc/py-${PORTNAME}
PORTDOCS=	*

OPTIONS_DEFINE=	DOCS

post-install-DOCS-on:
	${MKDIR} ${STAGEDIR}${DOCSDIR}/
	${INSTALL_DATA} ${WRKSRC}/README ${WRKSRC}/CHANGES ${STAGEDIR}${DOCSDIR}/
	cd ${WRKSRC}/build/sphinx/ && ${COPYTREE_SHARE} html ${STAGEDIR}${DOCSDIR}/

.include <bsd.port.mk>
