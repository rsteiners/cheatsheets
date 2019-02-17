### To compile firejail with apparmor enabled:

sudo apt install libapparmor-dev<br />
./configure -prefix=/usr --enable-apparmor

### To run Google Chrome with FIDO U2F working
firejail --apparmor --ignore=private-dev --ignore=nodbus google-chrome-stable

### To run KeePassXC with yubikey challenge mode
firejail --apparmor --ignore=private-dev --ignore=protocol keepassxc

### To create symbolic links
sudo firecfg

### To remove symbolic links
sudo firecfg --clean
