fedora_builder
==============

fedora 20, 21 apps and tweaks for HP 9470m


Add:  
`acpi_osi=Linux acpi_backlight=vendor`  
to:  
`/etc/default/grub (the line GRUBCMDLINELINUX=" ..... "`  
then:  
`grub2-mkconfig -o /boot/grub2/grub.cfg`  

```
su -c 'yum localinstall --nogpgcheck http://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm http://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm'

su -c "curl http://satya164.github.io/fedy/fedy-installer -o fedy-installer && chmod +x fedy-installer && ./fedy-installer"

yum localinstall --nogpgcheck http://www.teamviewer.com/download/teamviewer_linux.rpm

yum localinstall --nogpgcheck https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm
yum localinstall --nogpgcheck http://dl.google.com/linux/direct/google-talkplugin_current_x86_64.rpm
rpm -ivh http://linuxdownload.adobe.com/adobe-release/adobe-release-x86_64-1.0-1.noarch.rpm
rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-adobe-linux
yum install -y flash-plugin nspluginwrapper alsa-plugins-pulseaudio libcurl vlc geany geany-themes terminator gimp snes9x pcsx2 dolphin-emu pidgin insync skype dreampie mame gmameui java-1.7.0-openjdk icedtea-web akmod-nvidia xorg-x11-drv-nvidia-libs.i686 steam libvirt-daemon-config-network cups-pdf vim autofs htop keepassx gnome-tweak-tool virt-manager libvirt p7zip p7zip-plugins audacious audacious-plugins-freeworld-mp3

yum localinstall --nogpgcheck http://www.skype.com/go/getskype-linux-fc10/skype-fedora.i586.rpm
```

#.bashrc  

```
# USER
PS1="\[\e[37;1m\][\[\e[32;1m\]\u\[\e[33;1m\]@\[\e[32;1m\]\h \[\e[33;1m\]- \[\e[34;1m\]\w\[\e[37;1m\]]\[\e[32;1m\]$ \[\e[0m\]"

# ROOT
PS1="\[\e[37;1m\][\[\e[31;1m\]\u\[\e[33;1m\]@\[\e[32;1m\]\h \[\e[33;1m\]- \[\e[34;1m\]\w\[\e[37;1m\]]\[\e[31;1m\]# \[\e[0m\]"
```
