#
# $FreeBSD$
#

.include <bsd.own.mk>

GLIB_DISTDIR?= ${.CURDIR}/../../../contrib/glib-2.0

LIB=	gmodule-2.0

.PATH:		${GLIB_DISTDIR}/gmodule
SRCS=		\
		gmodule.c

WARNFLAGS=	-Wall -Wstrict-prototypes				\
		-Werror=implicit-function-declaration -Werror=init-self \
		-Werror=format-security -Werror=missing-include-dirs -Wno-error

OPTIONS=	-DHAVE_CONFIG_H -DG_LOG_DOMAIN=\"GModule\"		\
		-DG_DISABLE_CAST_CHECKS -DG_DISABLE_DEPRECATED

CFLAGS+=	-I${.CURDIR}						\
		-I${.CURDIR}/..						\
		-I${.CURDIR}/../glib					\
		-I${GLIB_DISTDIR}					\
		-I${GLIB_DISTDIR}/glib					\
		-I${GLIB_DISTDIR}/glib/deprecated			\
		-I/usr/local/include					\
		${OPTIONS} ${WARNFLAGS} -pthread 

.include <bsd.lib.mk>
.include <bsd.subdir.mk>
