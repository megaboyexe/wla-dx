
CC = wla-z80
CFLAGS = -x -o
LD = wlalink
LDFLAGS = -v -b -s

SFILES = setup.s main.s
IFILES = defines.i
OFILES = main.o setup.o

all: $(OFILES) makefile
	$(LD) $(LDFLAGS) linkfile linked.prg

main.o: main.s defines.i
	$(CC) $(CFLAGS) main.o main.s

setup.o: setup.s defines.i
	$(CC) $(CFLAGS) setup.o setup.s


$(OFILES): $(HFILES)


clean:
	rm -f $(OFILES) core *~ linked.prg linked.sym
