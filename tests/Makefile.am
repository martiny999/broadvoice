##
## broadvoice - a library for the BroadVoice 16 and 32 codecs
##
## Makefile.am -- Process this file with automake to produce Makefile.in
##
## This program is free software; you can redistribute it and/or modify
## it under the terms of the GNU General Public License version 2, as
## published by the Free Software Foundation.
##
## This program is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU General Public License for more details.
##
## You should have received a copy of the GNU General Public License
## along with this program; if not, write to the Free Software
## Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.
##
## $Id: Makefile.am,v 1.1.1.1 2009/11/19 12:10:48 steveu Exp $

AM_CFLAGS = $(COMP_VENDOR_CFLAGS)
AM_LDFLAGS = $(COMP_VENDOR_LDFLAGS)

LIBS += $(TESTLIBS)

TESTS = regression_tests.sh

EXTRA_DIST = regression_tests.sh \
             bv16_fixed_tests.sh \
             bv32_fixed_tests.sh \
             bv16_floating_tests.sh \
             bv32_floating_tests.sh

CLEANFILES = tmp

INCLUDES = -I$(top_srcdir)/src -DDATADIR="\"$(pkgdatadir)\""

noinst_PROGRAMS = bv16_tests \
                  bv32_tests \
		  broadvoice_tests

noinst_HEADERS =  g192_bit_stream.h \
                  timing.h

bv16_tests_SOURCES = bv16_tests.c g192_bit_stream.c
bv16_tests_LDADD = ../src/libbroadvoice.la

bv32_tests_SOURCES = bv32_tests.c g192_bit_stream.c
bv32_tests_LDADD = ../src/libbroadvoice.la

broadvoice_tests_SOURCES = broadvoice_tests.c g192_bit_stream.c
broadvoice_tests_LDADD = ../src/libbroadvoice.la
