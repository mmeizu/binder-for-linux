all: binderAddInts  binderAddInt

binderAddInts: binderAddInts.cpp
	g++-4.9 -std=c++11 -o $@ -I../libs/include -I.. -L../libs -DHAVE_PTHREADS -DHAVE_SYS_UIO_H -DHAVE_ENDIAN_H -DHAVE_ANDROID_OS=1 $< testUtil.c -lpthread -lbinder

binderAddInt: binderAddInts.cpp
	g++-4.9 -std=c++11 -o $@ -I../libs/include -I..   -DHAVE_PTHREADS -DHAVE_SYS_UIO_H -DHAVE_ENDIAN_H -DHAVE_ANDROID_OS=1 $< testUtil.c   -lbinder
clean:
	rm -f binderAddInts binderAddInt
