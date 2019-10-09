GPTL := ${HOME}/software/gptl

FFLAGS += -I$(GPTL)/include

LDFLAGS += -L$(GPTL)/lib -lgptl

%.o: %.F90
	$(FC) $(FFLAGS) -c $<

%: %.o
	$(FC) $(FFLAGS) -o $@ $^ $(LDFLAGS)

test_gptl: timing.o test_gptl.o

test_gptl.o: timing.o

clean:
	rm *.o *.mod
