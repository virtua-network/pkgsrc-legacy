# $NetBSD: Makefile,v 1.6 2017/01/01 14:44:05 wiz Exp $

VERSION=	0.9.8
DISTNAME=	PyWebDAV-${VERSION}
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:tl}
CATEGORIES=	www python
MASTER_SITES=	http://pywebdav.googlecode.com/files/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://code.google.com/p/pywebdav/
COMMENT=	Standards compliant Python WebDAV server and library
LICENSE=	gnu-gpl-v2

DOCDIR=			share/doc/${PKGBASE}

PLIST_SUBST+=	DOCDIR=${DOCDIR:Q}

INSTALLATION_DIRS+=	${DOCDIR}

PYTHON_VERSIONS_INCOMPATIBLE=	34 35 36 # not yet ported as of 0.9.8

post-install:
	${INSTALL_DATA} ${WRKSRC}/README ${DESTDIR}${PREFIX}/${DOCDIR}
	${INSTALL_DATA} ${WRKSRC}/VERSION ${DESTDIR}${PREFIX}/${DOCDIR}
	${INSTALL_DATA} ${WRKSRC}/doc/* ${DESTDIR}${PREFIX}/${DOCDIR}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
