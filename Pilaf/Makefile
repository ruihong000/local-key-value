PHONY: clean

CFLAGr  := -O3 -Wall -Wno-unused-result -g
LD      := gcc
LDFLAGS := ${LDFLAGS} -lrdmacm -libverbs -lrt -lpthread

APPS    := main

all: ${APPS}

main: common.c conn.c main.c crc64.c
	${LD} -O2 -o $@ common.c conn.c main.c crc64.c ${LDFLAGS} -g

clean:
	rm -f *.o ${APPS}
