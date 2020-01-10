# xserver-xorg_7.7-19ubuntu12-1_amd64.deb_modification_experemental_ubuntu_19.10_fix_not_tearing
xserver-xorg_7.7+19ubuntu12-1_amd64.deb linux ubuntu_fix_not_tearing

sudo rm  -Rfv /etc/X11/xorg.conf.d && sudo rm /etc/X11/xorg.conf /etc/X11/xorg.conf.failsafe /usr/share/X11/xorg.conf.d/20-intel.conf

sudo cp libexpat.la /usr/lib/x86_64-linux-gnu

sudo dpkg -i xserver-xorg_7.7+19ubuntu12-1_amd64.deb

exit session and reboot , run benchmark programm hardinfo -> GPU Drawing 

____________________________________________________________________________________________

About example libexpat version example ubuntu version 19.10

libexpat.la library_names='libexpat.so.1.6.9 libexpat.so.1 libexpat.so' ubuntu 19.10

Replace xorg , xserver-xorg , xserver-xorg-core , xwayland , xserver-common

При установке должны быть удалены различные xorg.conf , xorg.conf.failsafe /etc/X11 и папка xorg.conf.d из /etc/X11 и если интел то и конфиг для интел в основном помечается как 20-intel.conf который может быть в /usr/share/X11 должен быть удалён из всех возможных мест в основе эти места , данный xserver-xorg уже имеет ускорение на борту что ему даже конфиги не нужны ибо с ними он просто не стартанет из черного экрана т.е если ранее я предлагал такое решение то теперь оно наоборот сделает экран черным и не загружаемым и это решение лежало тут https://github.com/Griggorii/linux_xorg_glamor_perfomance_uxa_tearing_fix_intel-nouveau 
теперь я понял еще одну вещь obs-studio надо пересобирать потому что тиринг в самом захватчике obs и убедится в том что именно в этом xorg тиринга нет можно убедится просмотрев это видео https://www.youtube.com/watch?v=0RvIbVmCOxg так же можно использовать для захвата видео другой захватчик видео и проверить наличие диагональной черты тем самым будет точно понятно , так как компьютеры разные и процессоры и все остальное то просьба проверить мою версию , а то я ранее думал что это драивер интела когда выставлен в xorg давал этот тиринг хотя в браузерах его не было , а значит драивер интела может быть и не виноват.
