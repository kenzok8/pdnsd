SUBDIRS = src

EXTRA_DIST = version COPYING.BSD

# The sample configuration is handled in doc/Makefile.am
install-data-hook:
	$(mkinstalldirs) "$(DESTDIR)$(cachedir)"
	test -f "$(DESTDIR)$(cachedir)/pdnsd.cache" || \
	  touch "$(DESTDIR)$(cachedir)/pdnsd.cache"
	if test `whoami` = "root"; then \
	  chown $(def_id) "$(DESTDIR)$(cachedir)/pdnsd.cache"; \
	  chown $(def_id) "$(DESTDIR)$(cachedir)"; \
	fi
	chmod 0640 "$(DESTDIR)$(cachedir)/pdnsd.cache"
	chmod 0750 "$(DESTDIR)$(cachedir)"
