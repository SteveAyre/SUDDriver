
.PHONY: all
all: seneye

seneye: main.o linux/hid.o
	$(CXX) -Wall -o seneye main.o linux/hid.o -ludev -lncurses -lrt

main.o: main.cpp
	$(CXX) -Wall -c -o main.o main.cpp

linux/hid.o: linux/hid.c
	$(CXX) -c -o linux/hid.o linux/hid.c

.PHONY: install
install: seneye
	install -m755 seneye $(PREFIX)/usr/local/bin

.PHONY: clean
clean:
	rm -f seneye main.o linux/hid.o

