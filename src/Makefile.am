AUTOMAKE_OPTIONS = subdir-objects
ACLOCAL_AMFLAGS = $(ACLOCAL_FLAGS)

$(shell ./scripts/help.sh)

bin_PROGRAMS = SetsCalc

SetsCalc_SOURCES = main.c

SetsCalc_CPPFLAGS = $(CFLAGS) -Wall -Wextra -std=c90
SetsCalc_LDADD = libsetscalc_main.la
SetsCalc_LDFLAGS = $(LDFLAGS) -ldialog

include_HEADERS = headers/setscalc.h headers/SetsCalc_config.h

lib_LTLIBRARIES = libsetscalc_main.la

# libsetscalc_main.la
libsetscalc_main_la_LDFLAGS = -version-info 0:0:0 $(LDFLAGS) -ldialog
if HAVE_TEST
libsetscalc_main_la_SOURCES = libs/math.c libs/menu.c libs/menu2.c libs/menu3.c libs/tree2.c
else
libsetscalc_main_la_SOURCES = libs/math.c libs/menu.c libs/menu2.c libs/menu3.c libs/tree.c
endif
libsetscalc_main_la_CFLAGS = $(SetsCalc_CFLAGS)