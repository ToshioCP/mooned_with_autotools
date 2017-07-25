applicationsdir = $(datadir)/applications
nodist_applications_DATA = mooned.desktop

icon48dir = $(datadir)/icons/hicolor/48x48/apps
dist_icon48_DATA = mooned.png

EXTRA_DIST = mooned.desktop.in

CLEANFILES = mooned.desktop

mooned.desktop : mooned.desktop.in
	rm -f $@ $@.tmp
	sed 's|@datadir[@]|$(datadir)|g' $(srcdir)/$@.in >$@.tmp
	mv $@.tmp $@
