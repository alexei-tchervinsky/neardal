EXTRA_DIST = neardal.pc.in

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = neardal.pc

confdir = /etc/dbus-1/system.d/
conf_DATA=org.neardal.conf

SUBDIRS = lib ncl

#Rule to generate doxygen documentation
if HAVE_DOXYGEN
doxyfile.stamp:
	$(DOXYGEN) doxygen.cfg
	echo Timestamp > doxyfile.stamp

CLEANFILES = ./doxyfile.stamp

doc: doxyfile.stamp
endif

