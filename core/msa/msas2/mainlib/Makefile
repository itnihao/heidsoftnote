prefix = /app/msa/
bindir = /app/msa/bin
libdir = /app/msa/msas2/lib
srcdir = /app/msa/msas2
sqldir = /app/sqldb/include
publicdir = /app/msa/publiclib

CFLAGS:= -O2 -nostartfiles   -Wall -Wunused  -Iinclude -I${publicdir}/include -I${srcdir}/include \
-I${sqldir} -I/usr/include/libxml2/ -DNO_SHARED_LIBS=1

all: msasPubUtil.o
	ar rv ${libdir}/mainlib.a  *.o

clean: 
	rm -f  ${libdir}/mainlib.a *.o
	
msasPubUtil.o: msasPubUtil.c
	gcc -c  msasPubUtil.c  $(CFLAGS)
