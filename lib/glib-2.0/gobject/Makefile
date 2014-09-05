#
# $FreeBSD$
#

.include <bsd.own.mk>

GLIB_DISTDIR?= ${.CURDIR}/../../../contrib/glib-2.0

LIB=	gobject-2.0

.PATH:		${GLIB_DISTDIR}/gobject
SRCS=		\
		gatomicarray.c		\
		gbinding.c		\
		gboxed.c		\
		gclosure.c		\
		genums.c		\
		gmarshal.c		\
		gobject.c		\
		gparam.c		\
		gparamspecs.c		\
		gsignal.c		\
		gsourceclosure.c	\
		gtype.c			\
		gtypemodule.c		\
		gtypeplugin.c		\
		gvalue.c		\
		gvaluearray.c		\
		gvaluetransform.c	\
		gvaluetypes.c

WARNFLAGS=	-Wall -Wstrict-prototypes				\
		-Werror=implicit-function-declaration -Werror=init-self \
		-Werror=format-security -Werror=missing-include-dirs -Wno-error

OPTIONS=	-DHAVE_CONFIG_H -DG_LOG_DOMAIN=\"GLib-GObject\"		\
		-DG_DISABLE_CAST_CHECKS -DGOBJECT_COMPILATION

CFLAGS+=	-I${.CURDIR}/..						\
		-I${.CURDIR}/../glib					\
		-I${GLIB_DISTDIR}					\
		-I${GLIB_DISTDIR}/glib					\
		-I${GLIB_DISTDIR}/glib/deprecated			\
		-I/usr/local/include					\
		-I/usr/local/lib/libffi-3.0.13/include			\
		${OPTIONS} ${WARNFLAGS} -pthread 

.include <bsd.lib.mk>
.include <bsd.subdir.mk>
