#
# Makefile
# licj, 2015-09-09 15:19
#
version := 0.0.1
#CC=gcc
CC= /home/licj/prj/buildroot-lr9g25/output/host/usr/bin/arm-unknown-linux-uclibcgnueabi-gcc

DSOURCES = main.c ctl_socket_server.c
INCLUDE = -I ../include
LIBPATH = -L ../lib

DOBJECTS = $(DSOURCES:.c=.o)

CFLAGS += -Wall -g -DNO_DAEMON $(INCLUDE)

LDFLAGS += $(LIBPATH) \
		   -lmstp 


all: mstpd

mstpd:$(DOBJECTS)
	$(CC) $(DOBJECTS) $(CFLAGS) $(LDFLAGS) -o $@ 


.PHONY : clean

clean:
	rm mstpd $(DOBJECTS)







