CFLAGS = -Wall -fno-stack-protector -Wno-unused-function

.PHONY: all clean

all: piece_of_pie

piece_of_pie: piece_of_pie.o

piece_of_pie.o: piece_of_pie.c

clean:
	-rm -f *~ *.o
	-rm -f piece_of_pie

public: piece_of_pie
	cp piece_of_pie ../public/
