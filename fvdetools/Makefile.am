AM_CPPFLAGS = \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/common \
	@LIBCSTRING_CPPFLAGS@ \
	@LIBCERROR_CPPFLAGS@ \
	@LIBCDATA_CPPFLAGS@ \
	@LIBCLOCALE_CPPFLAGS@ \
	@LIBCNOTIFY_CPPFLAGS@ \
	@LIBCSPLIT_CPPFLAGS@ \
	@LIBUNA_CPPFLAGS@ \
	@LIBCFILE_CPPFLAGS@ \
	@LIBCPATH_CPPFLAGS@ \
	@LIBBFIO_CPPFLAGS@ \
	@LIBUNA_CPPFLAGS@ \
	@LIBBFIO_CPPFLAGS@ \
	@LIBFGUID_CPPFLAGS@ \
	@LIBHMAC_CPPFLAGS@ \
	@LIBCAES_CPPFLAGS@ \
	@LIBCSYSTEM_CPPFLAGS@ \
	@LIBFUSE_CPPFLAGS@ \
	@LIBFVDE_DLL_IMPORT@

AM_LDFLAGS = @STATIC_LDFLAGS@

bin_PROGRAMS = \
	fvdeinfo \
	fvdemount \
	fvdewipekey

fvdeinfo_SOURCES = \
	fvdeinfo.c \
	fvdeoutput.c fvdeoutput.h \
	fvdetools_libbfio.h \
	fvdetools_libcerror.h \
	fvdetools_libclocale.h \
	fvdetools_libcnotify.h \
	fvdetools_libcsplit.h \
	fvdetools_libcstring.h \
	fvdetools_libcsystem.h \
	fvdetools_libfvde.h \
	fvdetools_libfguid.h \
	fvdetools_libuna.h \
	info_handle.c info_handle.h

fvdeinfo_LDADD = \
	@LIBFGUID_LIBADD@ \
	@LIBCSYSTEM_LIBADD@ \
	@LIBBFIO_LIBADD@ \
	@LIBCPATH_LIBADD@ \
	@LIBCFILE_LIBADD@ \
	@LIBUNA_LIBADD@ \
	@LIBCSPLIT_LIBADD@ \
	@LIBCDATA_LIBADD@ \
	../libfvde/libfvde.la \
	@LIBCNOTIFY_LIBADD@ \
	@LIBCLOCALE_LIBADD@ \
	@LIBCERROR_LIBADD@ \
	@LIBCSTRING_LIBADD@ \
	@LIBINTL@

fvdemount_SOURCES = \
	fvdemount.c \
	fvdeoutput.c fvdeoutput.h \
	fvdetools_libbfio.h \
	fvdetools_libcerror.h \
	fvdetools_libclocale.h \
	fvdetools_libcnotify.h \
	fvdetools_libcsplit.h \
	fvdetools_libcstring.h \
	fvdetools_libcsystem.h \
	fvdetools_libfvde.h \
	fvdetools_libuna.h \
	mount_handle.c mount_handle.h

fvdemount_LDADD = \
	@LIBFUSE_LIBADD@ \
	@LIBCSYSTEM_LIBADD@ \
	@LIBBFIO_LIBADD@ \
	@LIBCPATH_LIBADD@ \
	@LIBCFILE_LIBADD@ \
	@LIBUNA_LIBADD@ \
	@LIBCSPLIT_LIBADD@ \
	@LIBCDATA_LIBADD@ \
	../libfvde/libfvde.la \
	@LIBCNOTIFY_LIBADD@ \
	@LIBCLOCALE_LIBADD@ \
	@LIBCERROR_LIBADD@ \
	@LIBCSTRING_LIBADD@ \
	@LIBINTL@

fvdewipekey_SOURCES = \
	fvdewipekey.c \
	fvdeoutput.c fvdeoutput.h \
	fvdetools_libbfio.h \
	fvdetools_libcerror.h \
	fvdetools_libclocale.h \
	fvdetools_libcnotify.h \
	fvdetools_libcstring.h \
	fvdetools_libcsystem.h \
	fvdetools_libuna.h \
	wipekey_handle.c wipekey_handle.h

fvdewipekey_LDADD = \
	@LIBCAES_LIBADD@ \
	@LIBCRYPTO_LIBADD@ \
	@LIBDL_LIBADD@ \
	@LIBCSYSTEM_LIBADD@ \
	@LIBBFIO_LIBADD@ \
	@LIBCPATH_LIBADD@ \
	@LIBCFILE_LIBADD@ \
	@LIBUNA_LIBADD@ \
	@LIBCSPLIT_LIBADD@ \
	@LIBCDATA_LIBADD@ \
	../libfvde/libfvde.la \
	@LIBCNOTIFY_LIBADD@ \
	@LIBCLOCALE_LIBADD@ \
	@LIBCERROR_LIBADD@ \
	@LIBCSTRING_LIBADD@ \
	@LIBINTL@

MAINTAINERCLEANFILES = \
	Makefile.in

distclean: clean
	/bin/rm -f Makefile

splint:
	@echo "Running splint on fvdeinfo ..."
	-splint -preproc -redef $(DEFS) $(DEFAULT_INCLUDES) $(INCLUDES) $(AM_CPPFLAGS) $(fvdeinfo_SOURCES)
	@echo "Running splint on fvdemount ..."
	-splint -preproc -redef $(DEFS) $(DEFAULT_INCLUDES) $(INCLUDES) $(AM_CPPFLAGS) $(fvdemount_SOURCES)

