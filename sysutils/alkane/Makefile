PORTNAME=	alkane
PORTVERSION=	0.3.2
CATEGORIES=	sysutils

MAINTAINER=	dereckson@gmail.com
COMMENT=	Deploy a website on the Nasqueron PaaS Alkane
WWW=		https://agora.nasqueron.org/Operations_grimoire/Alkane

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	${PREFIX}/share/public_suffix_list/public_suffix_list.dat:dns/public_suffix_list

USES=		cargo
USE_GITHUB=	yes
GH_ACCOUNT=	nasqueron
GH_TAGNAME=	v${PORTVERSION}

CARGO_CRATES=	aho-corasick-1.1.4 \
		anstream-1.0.0 \
		anstyle-1.0.14 \
		anstyle-parse-1.0.0 \
		anstyle-query-1.1.5 \
		anstyle-wincon-3.0.11 \
		atomic-waker-1.1.2 \
		axum-0.8.9 \
		axum-core-0.5.6 \
		bitflags-1.3.2 \
		bytes-1.12.0 \
		clap-4.6.1 \
		clap_builder-4.6.0 \
		clap_derive-4.6.1 \
		clap_lex-1.1.0 \
		colorchoice-1.0.5 \
		defmt-1.1.1 \
		defmt-macros-1.1.1 \
		defmt-parser-1.0.0 \
		env_filter-2.0.0 \
		env_logger-0.11.11 \
		equivalent-1.0.2 \
		form_urlencoded-1.2.2 \
		futures-channel-0.3.32 \
		futures-core-0.3.32 \
		futures-task-0.3.32 \
		futures-util-0.3.32 \
		hashbrown-0.17.1 \
		heck-0.5.0 \
		http-1.4.2 \
		http-body-1.0.1 \
		http-body-util-0.1.3 \
		httparse-1.10.1 \
		httpdate-1.0.3 \
		hyper-1.10.1 \
		hyper-util-0.1.20 \
		indexmap-2.14.0 \
		is_terminal_polyfill-1.70.2 \
		itoa-1.0.18 \
		jiff-0.2.31 \
		jiff-static-0.2.31 \
		lazy_static-1.5.0 \
		libc-0.2.186 \
		limiting-factor-axum-0.1.0 \
		limiting-factor-core-1.0.0 \
		log-0.4.33 \
		matchit-0.8.4 \
		memchr-2.8.2 \
		mime-0.3.17 \
		mio-1.2.1 \
		once_cell-1.21.4 \
		once_cell_polyfill-1.70.2 \
		percent-encoding-2.3.2 \
		pin-project-lite-0.2.17 \
		portable-atomic-1.13.1 \
		portable-atomic-util-0.2.7 \
		proc-macro2-1.0.106 \
		quote-1.0.46 \
		regex-1.12.4 \
		regex-automata-0.4.14 \
		regex-syntax-0.8.11 \
		ryu-1.0.23 \
		serde-1.0.228 \
		serde_core-1.0.228 \
		serde_derive-1.0.228 \
		serde_json-1.0.150 \
		serde_path_to_error-0.1.20 \
		serde_urlencoded-0.7.1 \
		serde_yaml-0.9.34+deprecated \
		slab-0.4.12 \
		smallvec-1.15.2 \
		socket2-0.6.4 \
		strsim-0.11.1 \
		syn-2.0.118 \
		sync_wrapper-1.0.2 \
		thiserror-2.0.18 \
		thiserror-impl-2.0.18 \
		tokio-1.52.3 \
		tokio-macros-2.7.0 \
		tower-0.5.3 \
		tower-layer-0.3.3 \
		tower-service-0.3.3 \
		tracing-0.1.44 \
		tracing-core-0.1.36 \
		unicode-ident-1.0.24 \
		unsafe-libyaml-0.2.11 \
		utf8parse-0.2.2 \
		wasi-0.11.1+wasi-snapshot-preview1 \
		windows-link-0.2.1 \
		windows-sys-0.61.2 \
		zmij-1.0.21

PLIST_FILES=	bin/alkane etc/rc.d/alkane

pre-build:
	${MKDIR} ${WRKSRC}/src/data
	${CP} ${PREFIX}/share/public_suffix_list/public_suffix_list.dat ${WRKSRC}/src/data/public_suffix_list.dat

post-install:
	${INSTALL_SCRIPT} ${WRKSRC}/support/freebsd/rc.d/alkane ${STAGEDIR}${PREFIX}/etc/rc.d

.include <bsd.port.mk>
