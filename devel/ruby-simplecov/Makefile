# $NetBSD: Makefile,v 1.17 2017/03/20 12:32:45 taca Exp $

DISTNAME=	simplecov-0.14.1
CATEGORIES=	devel

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://github.com/colszowka/simplecov
COMMENT=	Code coverage for Ruby 1.9
LICENSE=	mit

DEPENDS+=	${RUBY_PKGPREFIX}-simplecov-html>=0.10.0<0.11:../../devel/ruby-simplecov-html
DEPENDS+=	${RUBY_PKGPREFIX}-docile>=1.1.0<1.2:../../devel/ruby-docile

USE_LANGUAGES=	# none

RUBY_JSON_REQD=	1.8

.include "../../lang/ruby/gem.mk"
.include "../../mk/bsd.pkg.mk"
