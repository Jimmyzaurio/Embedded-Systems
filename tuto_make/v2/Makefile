# Archivo makefile simple
PROYECTO = muestreo
CFLAGS = -Wall
LDFLAGS = -lm
CC = gcc
DESTDIR = /usr/local/bin 
objects := $(patsubst %.c,%.o,$(wildcard *.c))

all: $(PROYECTO)

$(PROYECTO): $(objects)
	$(CC) $^ -o $@ $(LDFLAGS)

.PHONY: clean

install: all
	if [ ! -d $(DESTDIR)]; then \
		sudo mkdir $(DESTDIR); \
	fi; \
	sudo cp $(PROYECTO) $(DESTDIR) 
uninstall:
	rm $(DESTDIR)/$(PROYECTO) 

clean:  
	rm -f *.o $(PROYECTO) 
	
