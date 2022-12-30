
.PHONY: all
all: seneye

seneye: main.o
	$(CXX) -Wall -o seneye main.o -lncurses -lhidapi-hidraw -lhidapi-libusb

main.o: main.cpp
	$(CXX) -Wall -c -o main.o main.cpp

.PHONY: install
install: seneye
	install -m755 seneye $(PREFIX)/usr/bin

.PHONY: clean
clean:
	rm -f seneye main.o

