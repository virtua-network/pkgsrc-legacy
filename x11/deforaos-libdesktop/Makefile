# $NetBSD: Makefile,v 1.26 2017/04/13 00:48:38 khorben Exp $
#

DISTNAME=	libDesktop-0.2.2
PKGNAME=	deforaos-libdesktop-0.2.2
CATEGORIES=	x11
MASTER_SITES=	http://www.defora.org/os/download/download/4447/

MAINTAINER=	khorben@defora.org
HOMEPAGE=	http://www.defora.org/
COMMENT=	DeforaOS desktop library

LICENSE=	2-clause-bsd

USE_TOOLS+=	pkg-config

MAKE_FLAGS+=	DESTDIR=${DESTDIR}
MAKE_FLAGS+=	PREFIX=${PREFIX}
MAKE_FLAGS+=	CFLAGS=${CFLAGS:Q}
MAKE_FLAGS+=	LDFLAGS=${LDFLAGS:Q}
AUTO_MKDIRS=	yes

.include "../../mk/bsd.prefs.mk"

.if ${PKGMANDIR} != "share/man"
post-install:
	${MV} ${DESTDIR}${PREFIX}/share/man/html1/widget.html ${DESTDIR}${PREFIX}/${PKGMANDIR}/html1/widget.html
	${MV} ${DESTDIR}${PREFIX}/share/man/man1/widget.1 ${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/widget.1
	${RMDIR} ${DESTDIR}${PREFIX}/share/man/html1
	${RMDIR} ${DESTDIR}${PREFIX}/share/man/man1
	${RMDIR} ${DESTDIR}${PREFIX}/share/man
.endif

.include "../../devel/deforaos-libsystem/buildlink3.mk"
BUILDLINK_API_DEPENDS.gtk-doc+=	gtk-doc>=1.20
.include "../../x11/gtk2/buildlink3.mk"
.include "../../textproc/gtk-doc/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
