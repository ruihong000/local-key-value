PHONY: clean

CFLAGr  := -O3 -Wall -Wno-unused-result -Werror
LD      := gcc
LDFLAGS := ${LDFLAGS} -lrdmacm -libverbs -lrt -lpthread

APPS    := main

all: ${APPS}

main: common.o conn.o main.o crc64.o
	${LD} -O2 -o $@ $^ ${LDFLAGS}

clean:
	rm -f *.o ${APPS}
