all: libTimer.a

cpu             = MSP430G2553
cflags          = -MMCU=${cpu}



#SWITCH THE COMPILER (FOR THE INTERNAL MAKE RULES)
cc              = MSP430-ELF-GCC
as              = MSP430-ELF-AS
ar              = MSP430-ELF-AR


LIBtIMER.A: CLOCKStIMER.O SR.O
	$(ar) CRS $@ $^



INSTALL: LIBtIMER.A
	MKDIR -P ../H ../LIB
	MV $^ ../LIB
	CP *.H ../H


CLEAN:
	RM -F TIMERlIB.A *.O
