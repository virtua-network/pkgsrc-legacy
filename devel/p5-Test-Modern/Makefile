# $NetBSD: Makefile,v 1.3 2017/06/05 14:23:44 ryoon Exp $

DISTNAME=		Test-Modern-0.013
PKGNAME=		p5-${DISTNAME}
PKGREVISION=		2
CATEGORIES=		devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Test/}

MAINTAINER=		pkgsrc-users@NetBSD.org
HOMEPAGE=		http://search.cpan.org/dist/Test-Modern/
COMMENT=		Precision testing for modern perl
LICENSE=		${PERL5_LICENSE}

BUILD_DEPENDS+=	p5-Test-API>=0.004:../../devel/p5-Test-API
BUILD_DEPENDS+=	p5-Test-Deep>=0.111:../../devel/p5-Test-Deep
BUILD_DEPENDS+=	p5-Test-Fatal>0.007:../../devel/p5-Test-Fatal
BUILD_DEPENDS+=	p5-Test-Warnings>0.009:../../devel/p5-Test-Warnings

DEPENDS+=		p5-Module-Runtime>=0.012:../../devel/p5-Module-Runtime
DEPENDS+=		p5-Exporter-Tiny>=0.030:../../devel/p5-Exporter-Tiny
DEPENDS+=		p5-Import-Into>=1.002000:../../devel/p5-Import-Into

USE_LANGUAGES=		# empty
PERL5_PACKLIST=		auto/Test/Modern/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
