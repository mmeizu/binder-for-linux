all: libbinder.a ~/lib/libbinder.so

include cutils/Makefile
include utils/Makefile
include binder/Makefile

CFLAGS := -I.. -Iinclude -DHAVE_PTHREADS -DHAVE_SYS_UIO_H -DHAVE_ENDIAN_H -DHAVE_ANDROID_OS=1 -std=c++11 -fPIC

libbinder.a: $(objects)
	ar cr $@ $^

~/lib/libbinder.so: $(objects)
	g++  --shared -o $@ $^ -lpthread

clean:
	rm -f  libbinder.a `find -name \*.o`

%.o : %.cpp
	gcc-4.9 $(CFLAGS) -c -o $@ $<
%.o : %.c
	gcc-4.9 $(CFLAGS) -c -o $@ $<
