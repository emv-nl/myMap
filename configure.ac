AC_COPYRIGHT([Copyright (c) 2025 Eric Vissers])
AC_INIT([Openstreetmapviewer], [0.1], [https://github.com/emv-nl/myMap/])
AC_PREREQ([2.72])

dnl *** Initialize automake
AM_INIT_AUTOMAKE([])
AC_CONFIG_HEADERS=[config.h])
AM_MAINTAINER_MODE()
AM_SILENT_RULES=([yes])

dnl *** Check UNIX variants
AC_USE_SYSTEM_EXTENSIONS
AC_MSG_CHECKING([platform])
case "$host" in
  *-*-mingw*|*-*-cygwin*)
    platform="win32"
    NO_UNDEFINED=-no-undefined
    ;;
  *-apple-darwin*)
    platform="os x"
    ;;
  *)
    platform="unix"
    ;;
esac
AM_CONDITIONAL(PLATFORM_WIN32, test "$platform" = "win32")
AM_CONDITIONAL(PLATFORM_OSX, test "$platform" = "os x")
AC_SUBST(NO_UNDEFINED)

dnl *** Baisc programs
AC_PROG_CC()
LT_PATH_LD([])

dnl *** Check required libraries
XDT_CHECK_PACKAGE([GTK3], [gtk+-3.0], [3.24.0])
XDT_CHECK_PACKAGE([WEBKIT2GTK], [webkit2-gtk-4.0], [2.44.2])

dnl *** Platform flags
AC_MSG_CHECKING([PLATFORM_CPPFLAGS])
AC_MSG_RESULT([$PLATFORM_CPPFLAGS])
AC_SUBST([PLATFORM_CPPFLAGS])
AC_MSG_CHECKING([PLATFORM_CFLAGS])
AC_MSG_RESULT([$PLATFORM_CFLAGS])
AC_SUBST([PLATFORM_CFLAGS])
AC_MSG_CHECKING([PLATFORM_LDFLAGS])
AC_MSG_RESULT([$PLATFORM_LDFLAGS])
AC_SUBST([PLATFORM_LDFLAGS])

dnl *** Generate output files
AC_CONFIG_FILES([
Makefile
config.h
])
