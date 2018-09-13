install fedora 26

install lxde desktop dnf groupinstall -y "LXDE Desktop"

dnf install lightdm

dnf install system-switch-displaymanager

system-switch-displaymanger lightdm

install kernel packages

dnf install kernel-devel kernel-devel-4.11.8-300.fc26.x86_64

install vm guest add ons
