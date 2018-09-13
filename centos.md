install centos from live cd

yum install epel-release

install mate desktop 

yum groupinstall -y "MATE Desktop"

systemctl disable gdm.service

systemctl enable lightdm.service


install kernel packages

yum install kernel-devel kernel-devel-3.10.0-862.el7.x86_64

yum groupinstall 'Development Tools'

install vm guest add ons

yum install dkms

dnf install java-1.8.0-openjdk-devel f2c wget 2ping libssh  emacs gsl-devel 

R-core R-devel openssh-clients rsync gcc gcc-gfortran

R-reshape2 R-stringi R-htmltools R-rmarkdown R-markdown R-gplots R-rlang

start R

install.packages("rdyncall", repos="http://R-Forge.R-project.org")

copy patched version of SYstemic from server

patched to fix a number of issues

moved #DEFINE X,Y,Z lines from Systemic.h to integration.c

added gd.o and gd.c lines to Makefile
