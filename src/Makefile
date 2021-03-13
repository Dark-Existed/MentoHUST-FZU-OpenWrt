include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/package.mk

CC = gcc
#CC = mips-openwrt-linux-gcc
CFLAGS = -Wall -Os
#CFLAGS = -Wall -g -O2
INC_DIR= $(STAGING_DIR)/usr/include -I$(BUILD_DIR)/libpcap-*/ipkg-install/usr/include
LINK_DIR= $(STAGING_DIR)/usr/lib -L$(BUILD_DIR)/libpcap-*/ipkg-install/usr/lib
LIBS= $(BUILD_DIR)/libpcap-*/ipkg-install/usr/lib/libpcap.a
#LDFLAGS =

#OBJ = byte_order.o checkV4.o dlfunc.o md5.o mentohust.o mycheck.o myconfig.o myfunc.o myini.o mystate.o rjmd5.o rjripemd128.o rjsha1.o rjtiger.o rjtiger_sbox.o rjwhirlpool.o rjwhirlpool_sbox.o
.PHONY: all

all: mentohust

DEPS = $(wildcard *.h)

SRC = $(wildcard *.c)

OBJ = $(patsubst %.c, %.o, $(SRC))

%.o: %.c $(DEPS)
	$(CC) $(CFLAGS) -c $< -I$(INC_DIR)
#	$(CC) -c -o $@ $< $(CFLAGS)

mentohust: $(OBJ)
	$(CC) $(CFLAGS) -o $@ $(OBJ) $(LIBS) -I$(INC_DIR) -L$(LINK_DIR) $(LDFLAGS)

#.PHONY: clean

clean :
	rm -f mentohust *.o
#        rm -v $(OBJ) mentohust
