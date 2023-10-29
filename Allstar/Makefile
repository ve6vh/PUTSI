
INCDIR= -I/home/repeater/allstarlink/ASL-Asterisk/asterisk/include
WOPTS= -Wall -Wstrict-prototypes -Wmissing-prototypes -Wmissing-declarations
MAPOPTS = -MD -MT app_rpt.o -MP

all:	app_rpt.so

app_rpt.so:	app_rpt.c
		gcc -o app_rpt.o -c app_rpt.c -pthread $(INCDIR) -pipe $(WOPTS) -g3 -lpthread -Wno-unused-result -O6 -fPIC -DAST_MODULE=\"app_rpt\" $(MAPOPTS)
		gcc -o app_rpt.so -pthread   -shared -Xlinker -x app_rpt.o  -ltonezone -lm -lcurl

clean:		app_rpt.c
		rm *.o *.so .*.o.d *.d
