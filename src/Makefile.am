systemddir = $(systemdsystemunitdir)
scriptdir = $(libexecdir)/kubic-archive

script_SCRIPTS = mirror-openSUSE-registry mirror-openSUSE-Kubic-DVD
systemd_DATA = kubic-archive-container.service kubic-archive-container.timer \
	kubic-archive-DVD.service kubic-archive-DVD.timer

EXTRA_DIST = kubic-archive-container.service.in kubic-archive-DVD.service.in \
	mirror-openSUSE-registry.in $(SCRIPTS) $(DATA)

install-data-hook:
	mkdir -p $(DESTDIR)@sysconfdir@/kubic-archive
	echo -n "admin-password" > $(DESTDIR)@sysconfdir@/kubic-archive/secret-registry
	chmod 0600 $(DESTDIR)@sysconfdir@/kubic-archive/secret-registry

