#
# Makefile for sbcast

AUTOMAKE_OPTIONS = foreign

AM_CPPFLAGS = -I$(top_srcdir) $(BG_INCLUDES)
bin_PROGRAMS = sbcast

sbcast_LDADD = 	$(top_builddir)/src/api/libslurm.o \
	$(top_builddir)/src/bcast/libfile_bcast.la \
	$(DL_LIBS) -lm

noinst_HEADERS = sbcast.h
sbcast_SOURCES = sbcast.c opts.c

force:
$(sbcast_LDADD) : force
	@cd `dirname $@` && $(MAKE) `basename $@`

sbcast_LDFLAGS = -export-dynamic $(CMD_LDFLAGS)

