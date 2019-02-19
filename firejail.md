### To compile firejail with apparmor enabled

sudo apt install libapparmor-dev<br />
./configure -prefix=/usr --enable-apparmor

### Run without exposing any file in the HOME directory (Downloads is seen, but it's always empty)
firejail --private <target_application>

### To run Google Chrome with FIDO U2F working
firejail --apparmor --ignore=private-dev --ignore=nodbus google-chrome-stable &

### Run firefox sandboxing a new window
firejail --apparmor --private firefox -no-remote &

### To run KeePassXC with yubikey challenge mode
firejail --apparmor --ignore=private-dev --ignore=protocol keepassxc &

### To create symbolic links
sudo firecfg

### To remove symbolic links
sudo firecfg --clean
