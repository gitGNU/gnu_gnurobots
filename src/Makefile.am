## Copyright (C) 2008 Bradley Smith <brad@brad-smith.co.uk>
##
## src/Makefile.am
##
## GNU Robots is free software: you can redistribute it and/or modify
## it under the terms of the GNU General Public License as published by
## the Free Software Foundation, either version 3 of the License, or
## (at your option) any later version.
##
## GNU Robots is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU General Public License for more details.
##
## You should have received a copy of the GNU General Public License
## along with GNU Robots.  If not, see <http://www.gnu.org/licenses/>.

bin_PROGRAMS = gnurobots

AM_CFLAGS = -pedantic-errors -Werror -Wall

INCLUDES = $(GUILE_CFLAGS) $(READLINE_CFLAGS) $(GTK2_CFLAGS) \
	$(VTE_CFLAGS) $(GTHREAD2_CFLAGS) \
	-I$(top_builddir)/include \
   	-DPKGLIBDIR=\"$(pkglibdir)\" \
   	-DABS_TOP_BUILDDIR=\"$(abs_top_builddir)\" \
   	-DPKGDATADIR=\"$(pkgdatadir)\" \
   	-DMAPS_PATH=\"$(mapsdir)\" \
   	-DSCRIPTS_PATH=\"$(schemedir)\"

gnurobots_SOURCES = main.c api.c map.c grobot.c \
	ui-window.c ui-cmdwin.c ui-arena.c
gnurobots_LDFLAGS = $(GUILE_LDFLAGS) $(READLINE_LIBS) $(GTHREAD2_LIBS) \
	$(GTK2_LIBS) $(VTE_LIBS) -lutil
