# $NetBSD: Makefile,v 1.1 2017/04/19 22:36:13 minskim Exp $

DISTNAME=	actionview-${RUBY_RAILS_VERSION}
CATEGORIES=	www

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.rubyonrails.org/
COMMENT=	Simple conventions and helpers for building web pages
LICENSE=	mit

DEPENDS+=	${RUBY_ACTIVESUPPORT_DEPENDS}
DEPENDS+=	${RUBY_PKGPREFIX}-builder>=3.1:../../textproc/ruby-builder
DEPENDS+=	${RUBY_PKGPREFIX}-erubis>=2.7.0:../../www/ruby-erubis
DEPENDS+=	${RUBY_PKGPREFIX}-rails-dom-testing>=1.0.5:../../textproc/ruby-rails-dom-testing
DEPENDS+=	${RUBY_PKGPREFIX}-rails-html-sanitizer>=1.0.3:../../www/ruby-rails-html-sanitizer

RUBY_RAILS_SUPPORTED=	42
RUBY_RAILS_STRICT_DEP=	yes

.include "../../lang/ruby/gem.mk"
.include "../../mk/bsd.pkg.mk"
