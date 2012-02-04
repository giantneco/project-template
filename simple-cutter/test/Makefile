CUTTER = /usr/bin/cutter
CUTTER_CFLAGS = -I/usr/include/cutter  
CUTTER_LIBS = -lcutter  

CFLAGS = $(CUTTER_CFLAGS) -I../src
CLIBS = $(CUTTER_LIBS) -L../src

TESTS = libtest-stack.la

.SUFFIXES:

test-stack.lo: test-stack.c
	libtool --mode=compile gcc -c $(CFLAGS) -o $@ $<

libtest-stack.so: test-stack.lo
	libtool --mode=link gcc --shared $(CLIBS) -lstack -o $@ $< 

test: libtest-stack.so

check: test
	cutter -v v ./

clean:
	rm -rf *.o *.lo *.la *.so