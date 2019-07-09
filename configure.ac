# Autoconf requirements

# Initialize, but use more options. Note parameters brackts and whitespace.
AC_INIT([SetsCalc], [1.0], [anton2920@gmail.com])

# Safety check - list a source file that wouldn't be in other directories:
AC_CONFIG_SRCDIR([src/main.c])

# Put configuration results here, so we can easily #include them:
AC_CONFIG_HEADERS([src/headers/SetsCalc_config.h])

# Put autotools auxiliary files in a subdir, so they don't clutter top dir:
AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIR([m4])

# Enable «automake» to simplify creating makefiles:
AM_INIT_AUTOMAKE
AC_CONFIG_FILES([Makefile src/Makefile doc/Makefile man/Makefile examples/Makefile])

# Look for a C (CXX) compiler:
AC_LANG([C])
AC_PROG_CC

# Check for: (more) programs, libraries, header files, types,
# structures, compiler characteristics, library functions, system services.
LT_INIT

AC_ENABLE_STATIC
AC_ENABLE_SHARED
AC_PROG_LIBTOOL

# Check for ldialog, lcursesw, lncurses and m
AC_SEARCH_LIBS([setcchar], [ncursesw curses ncurses], [], [
	AC_MSG_ERROR([libncursesw is required to compile and run this program])
	])

# AC_SEARCH_LIBS([init_dialog], [dialog], [], [
#	AC_MSG_ERROR([libdialog is required to compile and run this program])
# 	])

AC_ARG_WITH([test], [AC_HELP_STRING([--with-test], [force build with debug version of tree.c])], [have_test=yes], [have_test=no])

# Qt test for Makefile.am
AM_CONDITIONAL([HAVE_TEST], [test "x$have_test" = xyes])

# Check for essential libraries 
AC_SEARCH_LIBS([strcpy], [c], [], [
	AC_MSG_ERROR([unable to find c lib])
	])

AC_SEARCH_LIBS([sin], [m], [], [
	AC_MSG_ERROR([unable to find math lib])
	])

AC_CHECK_HEADERS([stdio.h stdlib.h string.h time.h curses.h ctype.h dialog.h], [], [
	AC_MSG_ERROR([unable to find necessary headers])
	])

 # Checks for typedefs, structures, and compiler characteristics.
AC_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_SIZE_T
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_PID_T
AC_TYPE_SIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

# Do final output.
AC_OUTPUT

echo 
echo " ---------------------------------"
echo "| Options used to compile and link:"
echo "| CC            = $CC"
echo "| CFLAGS        = $CFLAGS"
echo "| LDFLAGS       = $LDFLAGS"
echo "| ARFLAGS       = $ARFLAGS"
echo " ---------------------------------"