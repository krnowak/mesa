include Makefile.sources
include $(top_srcdir)/src/gallium/Automake.inc

# XXX: check if we need the gallium/winsys include
AM_CFLAGS = \
	-I$(top_srcdir)/src/loader \
	-I$(top_srcdir)/src/gallium/winsys \
	$(GALLIUM_PIPE_LOADER_DEFINES) \
	$(GALLIUM_CFLAGS) \
	$(VISIBILITY_CFLAGS)

noinst_LTLIBRARIES = libpipe_loader.la

libpipe_loader_la_SOURCES = \
	$(COMMON_SOURCES)

if HAVE_DRM_LOADER_GALLIUM
AM_CFLAGS += \
	$(LIBDRM_CFLAGS)

libpipe_loader_la_SOURCES += \
	$(DRM_SOURCES)

libpipe_loader_la_LIBADD = \
	$(top_builddir)/src/loader/libloader.la

endif

