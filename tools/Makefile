
PREFIX ?= /usr/local
CXX ?= g++
CXXFLAGS ?= -g
CXXFLAGS += -I../include
LDFLAGS += -L../src -pthread -lz -lprotobuf-lite -losmpbf



all: osmpbf-outline

osmpbf-outline: osmpbf-outline.cpp
	$(CXX) $(CXXFLAGS) -o $@ $< $(LDFLAGS)

install:
	install -m 755 -d $(DESTDIR)$(PREFIX)/bin
	install -m 644 -s osmpbf-outline $(DESTDIR)$(PREFIX)/bin

clean:
	rm -f osmpbf-outline
