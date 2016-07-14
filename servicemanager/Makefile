all: servicemanager bctest

servicemanager: binder.o service_manager.o
	gcc-4.9 -o $@ $^

bctest: bctest.o binder.o
	gcc-4.9 -o $@ $^

clean:
	rm -f *.o servicemanager bctest
	
%.o: %.c
	gcc-4.9 -I.. $(CFLAGS) -c -o $@ $<
