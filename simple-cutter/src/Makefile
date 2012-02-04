.SUFFIXES:

stack.out:stack.c
	gcc -Wextra -o stack.out stack.c

stack.lo: stack.c
	libtool	--mode=compile gcc -Wextra -c stack.c -o stack.lo

libstack.la: stack.lo
	libtool	--mode=link gcc -Wextra -c stack.lo -o libstack.la

test: libstack.la

check: test

clean:
	rm -rf *.out *.lo *.o *.la