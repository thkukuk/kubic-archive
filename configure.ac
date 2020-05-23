dnl Process this file with autoconf to produce a configure script.
AC_INIT(kubic-archive, 1.0)
AM_INIT_AUTOMAKE
AC_PREFIX_DEFAULT(/usr)

AC_SUBST(PACKAGE)
AC_SUBST(VERSION)

PKG_CHECK_VAR([systemdsystemunitdir], [systemd], [systemdsystemunitdir], [],
	[AC_MSG_ERROR([Could not determine value for 'systemdsystemunitdir' - is the 'systemd.pc' file installed?])])

AC_PROG_INSTALL
AC_PROG_LN_S

AC_OUTPUT([Makefile src/Makefile src/kubic-archive-DVD.service \
	src/kubic-archive-container.service])
