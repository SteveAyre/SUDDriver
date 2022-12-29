
.PHONY: all
all: seneye

seneye: main.o
	$(CXX) -Wall -o seneye main.o -ludev -lncurses -lhidapi-libusb

main.o: main.cpp
	$(CXX) -Wall -c -o main.o main.cpp

.PHONY: install
install: seneye
	install -m755 seneye $(PREFIX)/usr/local/bin

.PHONY: clean
clean:
	rm -f seneye main.o

