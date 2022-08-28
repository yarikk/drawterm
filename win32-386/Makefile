ROOT=..
include ../Make.config
LIB=../libmachdep.a

OFILES=\
	getcallerpc.$O\
	md5block.$O\
	sha1block.$O\
	tas.$O

OFILES=\
	getcallerpc.$O

default: $(LIB)
$(LIB): $(OFILES)
	$(AR) /out:$(LIB) $(OFILES)
	$(RANLIB) $(LIB)

.SUFFIXES: .s .spp

.s.$O:
	$(AS) -o $*.$O $*.s

#.spp.s:
#	$(CXX) $*.spp >$*.s

.spp.$O:
	$(AS) -c -o $*.$O $*.spp
