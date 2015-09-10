#
# Makefile
# licj, 2015-09-09 15:19
#
version := 0.0.1
#CC=gcc
CC= /home/licj/prj/buildroot-lr9g25/output/host/usr/bin/arm-unknown-linux-uclibcgnueabi-gcc

INCLUDE = -I ../include
CTLSOURCES = ctl_main.c ctl_socket_client.c

CTLOBJECTS = $(CTLSOURCES:.c=.o)

CFLAGS += -Wall -g -DNO_DAEMON $(INCLUDE)

LDFLAGS = 


all: mstpctl

mstpctl:$(CTLOBJECTS)
	$(CC) $(CTLOBJECTS) $(CFLAGS)  $(LDFLAGS) -o $@ 


.PHONY : clean

clean:
	rm mstpctl $(CTLOBJECTS)







