install centos from live cd

install mate desktop 

yum groupinstall -y "MATE Desktop"

dnf install lightdm

dnf install system-switch-displaymanager

system-switch-displaymanger lightdm

install kernel packages

dnf install kernel-devel kernel-devel-4.11.8-300.fc26.x86_64

install vm guest add ons

dnf install java-1.8.0-openjdk-devel f2c wget 2ping libssh R-core R-devel openssh-clients rsync gcc gcc-gfortran emacs gsl-devel R-reshape2 R-stringi R-htmltools R-rmarkdown R-markdown R-gplots R-rlang

start R

install.packages("rdyncall", repos="http://R-Forge.R-project.org")

copy patched version of SYstemic from server

patched to fix a number of issues

moved #DEFINE X,Y,Z lines from Systemic.h to integration.c

added gd.o and gd.c lines to Makefile
