AC_PREREQ([2.68])
AC_INIT([recovery], [1.0])

AM_INIT_AUTOMAKE(subdir-objects foreign)
LT_INIT

# Checks for programs.
AC_PROG_CC
AC_PROG_CC_C_O
AM_PROG_CC_C_O
AC_PROG_YACC
AC_PROG_LEX

PKG_CHECK_MODULES([SAFE_IOP], [safe_iop])
PKG_CHECK_MODULES([MINCRYPT], [mincrypt])

AC_CONFIG_FILES(Makefile)
AC_OUTPUT
