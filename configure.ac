dnl Process this file with autoconf to produce a configure script.

AC_PREREQ(2.59)
AC_INIT([FULL-PACKAGE-NAME], [VERSION], [BUG-REPORT-ADDRESS])

AC_CONFIG_HEADERS([config.h])
AC_DEFINE([USE_MYMATH], [1], [Use my math library])
AC_DEFINE([Tutorial_VERSION_MAJOR], [1], [Major version])
AC_DEFINE([Tutorial_VERSION_MINOR], [0], [Minor version])

#AC_CANONICAL_SYSTEM
AM_INIT_AUTOMAKE()
AC_PROG_RANLIB

AC_PROG_CXX
AC_PROG_CC

AC_CHECK_FUNCS([log])
AC_CHECK_FUNCS([exp])

AC_CONFIG_FILES(Makefile src/Makefile lib/Makefile)
AC_OUTPUT

