# xserver-xorg_7.7-19ubuntu12-1_amd64.deb_modification_experemental_ubuntu_19.10_fix_not_tearing
xserver-xorg_7.7+19ubuntu12-1_amd64.deb linux ubuntu_fix_not_tearing

Пока не ставьте если вы не разработчик потому что оно то не работает то работает т.е вы должны принять все риски разбираться если не заработает уметь откатить удалить и тому подобное.

Только для Ubuntu версии 19.10. Устанавливать нужно сразу два пакета дабы избежать поломки системы!

sudo apt install hardinfo -> GPU Drawing test screenshot save

inpack arhive in folder terminal run

sudo rm  -Rfv /etc/X11/xorg.conf.d && sudo rm /etc/X11/xorg.conf /etc/X11/xorg.conf.failsafe /usr/share/X11/xorg.conf.d/20-intel.conf && sudo apt purge intel-microcode va-driver-all xserver-xorg-video-intel i965-va-driver -y

sudo cp libexpat.la /usr/lib/x86_64-linux-gnu

sudo dpkg -i *.deb

exit session and reboot , run benchmark programm hardinfo -> GPU Drawing

Для тех у кого видео карта не интел можете удалить xserver-xorg-video-intel

Вообщем что отличает этот драивер от простого манипулирования конфигами , он стабилен и не будет запущенная игра из wine 
вдруг неожиданно зависать на мертво.

Demo xorg-server prototip ubuntu 19.10 structure no xorg.conf https://radikal.ru/video/iqiN0DqFDBg
____________________________________________________________________________________________

About example libexpat version example ubuntu version 19.10

libexpat.la library_names='libexpat.so.1.6.9 libexpat.so.1 libexpat.so' ubuntu 19.10

Replace xorg , xserver-xorg , xserver-xorg-core , xwayland , xserver-common

При установке должны быть удалены различные xorg.conf , xorg.conf.failsafe /etc/X11 и папка xorg.conf.d из /etc/X11 и если интел то и конфиг для интел в основном помечается как 20-intel.conf который может быть в /usr/share/X11 должен быть удалён из всех возможных мест в основе эти места , данный xserver-xorg уже имеет ускорение на борту что ему даже конфиги не нужны ибо с ними он просто не стартанет из черного экрана т.е если ранее я предлагал такое решение то теперь оно наоборот сделает экран черным и не загружаемым и это решение лежало тут https://github.com/Griggorii/linux_xorg_glamor_perfomance_uxa_tearing_fix_intel-nouveau 
теперь я понял еще одну вещь obs-studio надо пересобирать потому что тиринг в самом захватчике obs и убедится в том что именно в этом xorg тиринга нет можно убедится просмотрев это видео https://www.youtube.com/watch?v=0RvIbVmCOxg так же можно использовать для захвата видео другой захватчик видео и проверить наличие диагональной черты тем самым будет точно понятно , так как компьютеры разные и процессоры и все остальное то просьба проверить мою версию , а то я ранее думал что это драивер интела когда выставлен в xorg давал этот тиринг хотя в браузерах его не было , а значит драивер интела может быть и не виноват. Во всяком случае если это obs то кто разбирается есть даже не очень блобовый исходный код xserver-xorg-video-intel-debian-unstable тогда получается некий графический исходник подправить надо именно в этом проекте.
