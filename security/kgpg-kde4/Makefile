# Created by: Martin Wilke <miwi@FreeBSD.org>
# $FreeBSD$

PORTNAME=	kgpg
PORTVERSION=	${KDE4_VERSION}
PORTREVISION=	2
CATEGORIES=	security kde kde-kde4

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Encryption tool for KDE

RUN_DEPENDS=	gpg2:security/gnupg

USES=		cmake:outsource kde:4 qt:4 tar:xz
USE_KDE=	automoc4 kdelibs pimlibs
USE_QT=		qmake_build moc_build rcc_build uic_build

.include <bsd.port.mk>
