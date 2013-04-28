lib_LTLIBRARIES =
bin_PROGRAMS =
CLEANFILES =

lib_LTLIBRARIES += libapplypatch.la
libapplypatch_la_CFLAGS = $(MINCRYPT_CFLAGS)
libapplypatch_la_LDFLAGS = $(MINCRYPT_LIBS)
libapplypatch_la_SOURCES = \
	applypatch/applypatch.c \
	applypatch/bsdiff.c \
	applypatch/bspatch.c \
	applypatch/freecache.c \
	applypatch/imgdiff.c \
	applypatch/imgpatch.c \
	applypatch/utils.c

BUILT_SOURCES = edify/parser.h
AM_YFLAGS = -d
lib_LTLIBRARIES += libedify.la
libedify_la_SOURCES = \
	edify/expr.c \
	edify/parser.y \
	edify/lexer.l
CLEANFILES += \
	edify/parser.c \
	edify/parser.h \
	edify/lexer.c

lib_LTLIBRARIES += libminelf.la
libminelf_la_SOURCES = minelf/Retouch.c
libminelf_la_CFLAGS = $(MINCRYPT_CFLAGS)
libminelf_la_LDFLAGS = $(MINCRYPT_LIBS)

lib_LTLIBRARIES += libminzip.la
libminzip_la_CFLAGS = $(SAFE_IOP_CFLAGS) -D_GNU_SOURCE
libminzip_la_LDFLAGS = $(SAFE_IOP_LIBS)
libminzip_la_SOURCES = \
	minzip/DirUtil.c \
	minzip/Hash.c \
	minzip/Inlines.c \
	minzip/SysUtil.c \
	minzip/Zip.c

lib_LTLIBRARIES += libmtdutils.la
libmtdutils_la_SOURCES = \
	mtdutils/mtdutils.c \
	mtdutils/mounts.c

bin_PROGRAMS += updater/updater
updater_updater_SOURCES = \
	updater/install.c \
	updater/updater.c
updater_updater_LDADD = \
	libapplypatch.la \
	libedify.la \
	libminelf.la \
	libminzip.la \
	libmtdutils.la
updater_updater_CFLAGS = $(MINCRYPT_CFLAGS)
updater_updater_LDFLAGS = $(MINCRYPT_LIBS) -lz -lbz2 -lselinux
