#
# $FreeBSD$
#

.include <bsd.own.mk>

GLIB_DISTDIR?= ${.CURDIR}/../../../contrib/glib-2.0

LIB=	gio-2.0

.PATH:		${GLIB_DISTDIR}/gio/xdgmime
SRCS=		\
		xdgmime.c		\
		xdgmimealias.c		\
		xdgmimecache.c		\
		xdgmimeglob.c		\
		xdgmimeicon.c		\
		xdgmimeint.c		\
		xdgmimemagic.c		\
		xdgmimeparent.c

.PATH:		${GLIB_DISTDIR}/gio/kqueue
SRCS+=		\
		dep-list.c			\
		gkqueuedirectorymonitor.c	\
		gkqueuefilemonitor.c		\
		kqueue-exclusions.c		\
		kqueue-helper.c			\
		kqueue-missing.c		\
		kqueue-sub.c			\
		kqueue-thread.c			\
		kqueue-utils.c

.PATH:		${GLIB_DISTDIR}/gio/gvdb
SRCS+=		\
		gvdb-reader.c

.PATH:		${GLIB_DISTDIR}/gio
SRCS+=		\
		gappinfo.c			\
		gasynchelper.c			\
		gasyncinitable.c		\
		gasyncresult.c			\
		gbufferedinputstream.c		\
		gbufferedoutputstream.c		\
		gcharsetconverter.c		\
		gcancellable.c			\
		gconverter.c			\
		gconverterinputstream.c		\
		gconverteroutputstream.c	\
		gcredentials.c			\
		gdrive.c			\
		gdatainputstream.c		\
		gdataoutputstream.c		\
		gdummyfile.c			\
		gdummyproxyresolver.c		\
		gdummytlsbackend.c		\
		gemblem.c			\
		gemblemedicon.c			\
		gfile.c				\
		gfileattribute.c		\
		gfileenumerator.c		\
		gfileicon.c			\
		gfileinputstream.c		\
		gfileinfo.c			\
		gfilemonitor.c			\
		gfilenamecompleter.c		\
		gfileoutputstream.c		\
		gfileiostream.c			\
		gfilterinputstream.c		\
		gfilteroutputstream.c		\
		gicon.c				\
		ginetaddress.c			\
		ginetaddressmask.c		\
		ginetsocketaddress.c		\
		ginitable.c			\
		ginputstream.c			\
		gioerror.c			\
		giomodule.c			\
		gioscheduler.c			\
		giostream.c			\
		gloadableicon.c			\
		gmount.c			\
		gmemoryinputstream.c		\
		gmemoryoutputstream.c		\
		gmountoperation.c		\
		gnativevolumemonitor.c		\
		gnetworkaddress.c		\
		gnetworking.c			\
		gnetworkmonitor.c		\
		gnetworkmonitorbase.c		\
		gnetworkservice.c		\
		goutputstream.c			\
		gpermission.c			\
		gpollableinputstream.c		\
		gpollableoutputstream.c		\
		gpollableutils.c		\
		gpollfilemonitor.c		\
		gproxy.c			\
		gproxyaddress.c			\
		gproxyaddressenumerator.c	\
		gproxyresolver.c		\
		gresolver.c			\
		gresource.c			\
		gresourcefile.c			\
		gseekable.c			\
		gsimpleasyncresult.c		\
		gsimplepermission.c		\
		gsocket.c			\
		gsocketaddress.c		\
		gsocketaddressenumerator.c	\
		gsocketclient.c			\
		gsocketconnectable.c		\
		gsocketconnection.c		\
		gsocketcontrolmessage.c		\
		gsocketinputstream.c		\
		gsocketlistener.c		\
		gsocketoutputstream.c		\
		gsocketservice.c		\
		gsrvtarget.c			\
		gsimpleproxyresolver.c		\
		gtask.c				\
		gtcpconnection.c		\
		gtcpwrapperconnection.c		\
		gthreadedsocketservice.c	\
		gthemedicon.c			\
		gthreadedresolver.c		\
		gtlsbackend.c			\
		gtlscertificate.c		\
		gtlsclientconnection.c		\
		gtlsconnection.c		\
		gtlsdatabase.c			\
		gtlsfiledatabase.c		\
		gtlsinteraction.c		\
		gtlspassword.c			\
		gtlsserverconnection.c		\
		gunionvolumemonitor.c		\
		gvfs.c				\
		gvolume.c			\
		gvolumemonitor.c		\
		gzlibcompressor.c		\
		gzlibdecompressor.c		\
		gioenumtypes.c			\
		gunixfdlist.c			\
		gdesktopappinfo.c		\
		gfiledescriptorbased.c		\
		gunixconnection.c		\
		gunixcredentialsmessage.c	\
		gunixfdmessage.c		\
		gunixmount.c			\
		gunixmounts.c			\
		gunixsocketaddress.c		\
		gunixvolume.c			\
		gunixvolumemonitor.c		\
		gunixinputstream.c		\
		gaction.c			\
		gunixoutputstream.c		\
		gcontenttype.c			\
		gapplication.c			\
		gapplicationcommandline.c	\
		gapplicationimpl-dbus.c		\
		gactiongroup.c			\
		gactionmap.c			\
		gsimpleactiongroup.c		\
		gremoteactiongroup.c		\
		gactiongroupexporter.c		\
		gdbusactiongroup.c		\
		gsimpleaction.c			\
		gmenumodel.c			\
		gmenu.c				\
		gmenuexporter.c			\
		gdbusmenumodel.c		\
		gdelayedsettingsbackend.c	\
		gkeyfilesettingsbackend.c	\
		gmemorysettingsbackend.c	\
		gnullsettingsbackend.c		\
		gsettingsbackend.c		\
		gsettings.c			\
		gsettingsschema.c		\
		gsettings-mapping.c		\
		gdbusutils.c			\
		gdbusaddress.c			\
		gdbusauthobserver.c		\
		gdbusauth.c			\
		gdbusauthmechanism.c		\
		gdbusauthmechanismanon.c	\
		gdbusauthmechanismexternal.c	\
		gdbusauthmechanismsha1.c	\
		gdbuserror.c			\
		gdbusconnection.c		\
		gdbusmessage.c			\
		gdbusnameowning.c		\
		gdbusnamewatching.c		\
		gdbusproxy.c			\
		gdbusprivate.c			\
		gdbusintrospection.c		\
		gdbusmethodinvocation.c		\
		gdbusserver.c			\
		gdbusinterface.c		\
		gdbusinterfaceskeleton.c	\
		gdbusobject.c			\
		gdbusobjectskeleton.c		\
		gdbusobjectproxy.c		\
		gdbusobjectmanager.c		\
		gdbusobjectmanagerclient.c	\
		gtestdbus.c			\
		gdbusobjectmanagerserver.c	\
		glocaldirectorymonitor.c	\
		glocalfile.c			\
		glocalfileenumerator.c		\
		glocalfileinfo.c		\
		glocalfileinputstream.c		\
		glocalfilemonitor.c		\
		glocalfileoutputstream.c	\
		glocalfileiostream.c		\
		glocalvfs.c			\
		gsocks4proxy.c			\
		gsocks4aproxy.c			\
		gsocks5proxy.c

WARNFLAGS=	-Wall -Wstrict-prototypes				\
		-Werror=implicit-function-declaration -Werror=init-self \
		-Werror=format-security -Werror=missing-include-dirs -Wno-error

OPTIONS=	-DHAVE_CONFIG_H -DG_LOG_DOMAIN=\"GLib-GIO\"		\
		-DG_DISABLE_CAST_CHECKS -DGIO_COMPILATION	\
		-DGIO_MODULE_DIR=\"/usr/local/lib/gio/modules\" 

CFLAGS+=	-I${.CURDIR}/..						\
		-I${.CURDIR}/../glib					\
		-I${GLIB_DISTDIR}					\
		-I${GLIB_DISTDIR}/gio					\
		-I${GLIB_DISTDIR}/glib					\
		-I${GLIB_DISTDIR}/gmodule				\
		-I${GLIB_DISTDIR}/gvdb					\
		-I/usr/local/include					\
		${OPTIONS} ${WARNFLAGS} -pthread

.include <bsd.lib.mk>
.include <bsd.subdir.mk>
