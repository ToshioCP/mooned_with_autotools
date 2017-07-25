#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([mooned], [0.5], [lxboyjp@gmail.com],,[https://github.com/ToshioCP/mooned])
AM_INIT_AUTOMAKE([-Wall -Wno-portability -Werror foreign])

AC_CONFIG_SRCDIR([src/moonedwin.h])
AC_CONFIG_HEADERS([config.h])

PKG_CHECK_MODULES([GTK],[gtk+-3.0 >= 3.2],,AC_MSG_ERROR([Gtk+-3.0 >= 3.2 is required.]))
AC_PATH_PROG([GLIB_COMPILE_RESOURCES], [glib-compile-resources])

# Checks for programs.
AC_PROG_CC

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADERS([string.h])

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.
AC_CONFIG_FILES([Makefile src/Makefile data/Makefile])
AC_OUTPUT

