#
# $FreeBSD$
#

.include <bsd.own.mk>

GLIB_DISTDIR?= ${.CURDIR}/../../../contrib/glib-2.0

LIB=	glib-2.0

.PATH:		${GLIB_DISTDIR}/glib
SRCS=		\
		garray.c gasyncqueue.c gatomic.c gbacktrace.c		\
		gbase64.c gbitlock.c gbookmarkfile.c gbytes.c		\
		gcharset.c gchecksum.c gconvert.c gdataset.c		\
		gdate.c gdatetime.c gdir.c genviron.c gerror.c		\
		gfileutils.c ggettext.c ghash.c ghmac.c ghook.c		\
		ghostutils.c giochannel.c gkeyfile.c glib-init.c	\
		glib-private.c glib-unix.c glist.c gmain.c gmappedfile.c\
		gmarkup.c gmem.c gmessages.c gnode.c goption.c		\
		gpattern.c gpoll.c gprimes.c gprintf.c gqsort.c gquark.c\
		gqueue.c grand.c gregex.c gscanner.c gsequence.c	\
		gshell.c gslice.c gslist.c gstdio.c gstrfuncs.c		\
		gstring.c gstringchunk.c gtestutils.c gthread-posix.c	\
		gthread.c gthreadpool.c gtimer.c gtimezone.c		\
		gtrashstack.c gtree.c gunibreak.c gunicollate.c		\
		gunidecomp.c guniprop.c gurifuncs.c gutf8.c gutils.c	\
		gvariant-core.c gvariant-parser.c gvariant-serialiser.c \
		gvariant.c gvarianttype.c gvarianttypeinfo.c gversion.c \
		gwakeup.c

.PATH:		${GLIB_DISTDIR}/glib/deprecated
SRCS+=		\
		gallocator.c gcache.c gcompletion.c grel.c		\
		gthread-deprecated.c

WARNFLAGS=	-Wall -Wstrict-prototypes				\
		-Werror=implicit-function-declaration -Werror=init-self \
		-Werror=format-security -Werror=missing-include-dirs -Wno-error

OPTIONS=	-DHAVE_CONFIG_H -DG_LOG_DOMAIN=\"GLib\"		\
		-DG_DISABLE_CAST_CHECKS -DGLIB_COMPILATION -DPCRE_STATIC

CFLAGS+=	-I${.CURDIR}						\
		-I${.CURDIR}/..						\
		-I${GLIB_DISTDIR}					\
		-I${GLIB_DISTDIR}/glib					\
		-I${GLIB_DISTDIR}/glib/deprecated			\
		-I/usr/local/include					\
		${OPTIONS} ${WARNFLAGS} -pthread 

.include <bsd.lib.mk>
.include <bsd.subdir.mk>
