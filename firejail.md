### To compile firejail with apparmor enabled:

sudo apt install libapparmor-dev<br />
./configure -prefix=/usr --enable-apparmor

### To run Google Chrome with FIDO U2F working
firejail google-chrome-stable --noprofile

### To run KeePassXC with yubikey challenge mode
firejail --ignore=private-dev --ignore=protocol keepassxc
