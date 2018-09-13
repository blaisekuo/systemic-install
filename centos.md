systemic-install
installing systemic rv software on linux

Install centos from live cd

Get the systemic 2 package

http://www.stefanom.org/d/systemic2/

move the Systemoc directory to /usr/local

apt-get install build-essential fakeroot devscripts

apt-get install linux-headers-amd64 linux-headers-4.9.0-7-amd64

install virtual box guest addons

install kernel headers

apt-get install

apt-get install gfortran f2c gsl-bin libgsl0-dev

apt-get install r-base r-base-dev

apt-get install default-jdk

start R, run:

install.packages("rdyncall",repos="http://R-Forge.R-project.org")

moving the lines

#define X 1 #define Y 2 #define Z 3 from systemic.h to integration.c

apply patch

--- Makefile.linux.orig	2016-02-09 16:51:00.079545000 -0500 +++ Makefile.linux	2016-02-09 16:51:53.273322000 -0500 @@ -23,7 +23,7 @@ #UPDATE = --update --java UPDATE =

-ALLOBJECTS = objects/swift.o objects/periodogram.o objects/extras.o objects/mercury.o objects/integration.o objects/mcmc.o objects/utils.o objects/simplex.o objects/kernel.o objects/bootstrap.o objects/kl.o objects/qsortimp.o objects/lm.o objects/lm.o objects/hermite.o objects/ode.o objects/odex.o objects/sa.o objects/de.o +ALLOBJECTS = objects/swift.o objects/periodogram.o objects/extras.o objects/mercury.o objects/integration.o objects/mcmc.o objects/utils.o objects/simplex.o objects/kernel.o objects/bootstrap.o objects/kl.o objects/qsortimp.o objects/lm.o objects/lm.o objects/hermite.o objects/ode.o objects/odex.o objects/sa.o objects/de.o objects/gd.o

linux: reqs src/.c src/.h $(ALLOBJECTS) gcc -shared -o libsystemic.so objects/*.o $(LIBS) $(LIBNAMES) @@ -87,6 +87,9 @@ objects/de.o: src/de.c $(CC) $(CCFLAGS) $(SYSFLAGS) -c -o objects/de.o src/de.c

+objects/gd.o: src/gd.c

$(CC) $(CCFLAGS) $(SYSFLAGS) -c -o objects/gd.o src/gd.c
.PHONY: clean cleanreqs

clean:

build systemic

move Systemic directory to /usr/local

then:

make -f Makefile.linux

edit .bash_aliases for astrolab user and add:

export LD_LIBRARY_PATH="/usr/local/Systemic:$LD_LIBRARY_PATH"
