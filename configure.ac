#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.


AC_PREREQ(2.52)

AC_INIT([apertium-fin-olo], [0.0.1], [flammie@iki.fi], [apertium-fin-olo], [https://wiki.apertium.org/wiki/apertium-fin-olo])
AM_INIT_AUTOMAKE([-Wall -Werror -Wno-portability foreign])
AC_PROG_LN_S
AC_PROG_AWK

m4_define([required_apertium_version], [3.3.0])
PKG_CHECK_MODULES(APERTIUM, apertium >= required_apertium_version, [], [PKG_CHECK_MODULES(APERTIUM, apertium-3.2 >= required_apertium_version)])

AC_ARG_ENABLE([trim],
              [AS_HELP_STRING([--enable-trim],
                              [remove entries from dictionaries at whim @<:@default=yes@:>@])],
                              [enable_trim=$enableval], [enable_trim=yes])
AM_CONDITIONAL([WANT_TRIMMED], [test x$enable_trim != xno])

AC_PATH_PROG([HFSTLEXC], [hfst-lexc], [false], [$PATH$PATH_SEPARATOR$with_hfst_lexc/bin])
AS_IF([test x$HFSTLEXC = xfalse], [AC_MSG_ERROR([You don't have hfst-lexc installed])])

AC_PATH_PROG([HFSTTWOLC], [hfst-twolc], [false], [$PATH$PATH_SEPARATOR$with_hfst_twolc/bin])
AS_IF([test x$HFSTTWOLC = xfalse], [AC_MSG_ERROR([You don't have hfst-twolc installed])])

AC_PATH_PROG([CGCOMP], [cg-comp], [false], [$PATH$PATH_SEPARATOR$with_cg_comp/bin])
AS_IF([test x$CGCOMP = xfalse], [AC_MSG_ERROR([You don't have cg-comp installed])])

AC_PATH_PROG([CGPROC], [cg-proc], [false], [$PATH$PATH_SEPARATOR$with_cg_proc/bin])
AS_IF([test x$CGPROC = xfalse], [AC_MSG_ERROR([You don't have cg-proc installed])])

AC_PATH_PROG([CGRELABEL], [cg-relabel], [false], [$PATH$PATH_SEPARATOR$with_cg_relabel/bin])
AS_IF([test x$CGRELABEL = xfalse], [AC_MSG_ERROR([You don't have cg-relabel installed; please upgrade your vislcg3])])

AC_PATH_PROG([LRXCOMP], [lrx-comp], [false], [$PATH$PATH_SEPARATOR$with_lrx_comp/bin])
AS_IF([test x$LRXCOMP = xfalse], [AC_MSG_ERROR([You don't have lrx-comp installed])])

AC_PATH_PROG([LRXPROC], [lrx-proc], [false], [$PATH$PATH_SEPARATOR$with_lrx_proc/bin])
AS_IF([test x$LRXPROC = xfalse], [AC_MSG_ERROR([You don't have lrx-proc installed])])

AC_PATH_PROGS(ZCAT, [gzcat zcat], [false])
AS_IF([test x$ZCAT = xfalse], [AC_MSG_ERROR([You don't have zcat nor gzcat installed])])

m4_ifdef([AP_CHECK_LING],[],[AC_MSG_ERROR([AP_CHECK_LING not defined, is apertium.m4 in ACLOCAL_PATH? See: https://wiki.apertium.org/wiki/Installation_troubleshooting])])

AP_CHECK_LING([1], [apertium-fin])
AP_CHECK_LING([2], [giella-olo])

AC_PATH_PROGS([SAXON], [saxon9-transform], [false])
AM_CONDITIONAL([CAN_SAXON], [test x$SAXON != xfalse])

AP_MKINCLUDE

AC_OUTPUT([Makefile docs/Makefile])

