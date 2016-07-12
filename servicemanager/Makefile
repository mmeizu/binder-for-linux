all: servicemanager bctest

servicemanager: binder.o service_manager.o
	gcc -o $@ $^

bctest: bctest.o binder.o
	gcc -o $@ $^

clean:
	rm -f *.o servicemanager bctest
	
%.o: %.c
	gcc -I.. $(CFLAGS) -c -o $@ $<
