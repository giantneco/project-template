SUBDIRS = src test

.PHONY: all test $(subdirs)

all:
	@ for subdir in $(SUBDIRS) ; do \
		(cd $$subdir && $(MAKE) $@) ;\
	done

check:
	@ for subdir in $(SUBDIRS) ; do \
		(cd $$subdir && $(MAKE) $@) ;\
	done

clean:
	@ for subdir in $(SUBDIRS) ; do \
		(cd $$subdir && $(MAKE) $@) ;\
	done
