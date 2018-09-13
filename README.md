# systemic-install
installing systemic rv software on linux

Install debian 9.5 with MATE GUI in a virtual box VM

Get the systemic 2 package

http://www.stefanom.org/d/systemic2/

move the Systemoc directory to /usr/local

apt-get update

apt-get install build-essential fakeroot devscripts

apt-get install gfortran f2c gsl-bin libgsl0-dev

apt-get install r-base r-base-dev

apt-get install default-jdk


start R, run:

install.packages("rdyncall",repos="http://R-Forge.R-project.org")


moving the lines

#define X 1
#define Y 2
#define Z 3
from systemic.h to integration.c

build systemic

move Systemic directory to /usr/local

then:

make -f Makefile.linux

