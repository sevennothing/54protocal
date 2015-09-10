#
# Makefile
# licj, 2015-09-09 15:19
#
version := 0.0.1
#CC=gcc
CC= /home/licj/prj/buildroot-lr9g25/output/host/usr/bin/arm-unknown-linux-uclibcgnueabi-gcc


LIBSOURCES = mstp.c hmac_md5.c bridge_track.c packet.c \
			 libnetlink.c driver_deps.c \
			 epoll_loop.c brmon.c \
			 netif_utils.c

LIBOBJECTS = $(LIBSOURCES:.c=.o)

CFLAGS += -Wall -g -DNO_DAEMON -fPIC

LDFLAGS += -shared


all: libmstp.so

libmstp.so:$(LIBOBJECTS)
	$(CC) $(LIBOBJECTS) $(CFLAGS) $(LDFLAGS) -o $@ 


.PHONY : install

install:libmstp.so
	cp libmstp.so ../lib/libmstp.so


.PHONY : clean

clean:
	rm libmstp.so $(LIBOBJECTS)







