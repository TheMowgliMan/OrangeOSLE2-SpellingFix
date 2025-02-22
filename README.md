# Orange OS LE 2
Orange OS LE 2 - Electric Boogaloo.

A revival of Orange OS.

This OS will have all major AT projects included as links on the desktop or apps.

# Development Preview

Download the latest iso in the releases section, then boot it up. 
Due to a temporary problem with archinstall, you should run
```
sed -i 's|pacman-init|reflector|g' /usr/lib/python3.11/site-packages/archinstall/examples/guided.py
```
After that, run
```
chmod +x /usr/local/bin/orangeinstall
orangeinstall
```

This will start the installer.

Answer the questions, then it should start.

After it's done, reboot by running 
```
reboot -h now
```
Then reboot, login with the account you just made and run
```
sudo curl https://raw.githubusercontent.com/Orange-OS-LE/OrangeOSLE2/main/postinstall.py > postinstall.py && sudo python3 postinstall.py && rm postinstall.py
```
when that's completed, run
```
sudo reboot -h now
```
And Orange OS LE 2 should be installed. Make an issue if something doesn't work or goes wrong.

# Nightly Version

To test the nightly version, download the latest arch linux ISO [here](https://archlinux.org/download/), boot it, then
due to a temporary problem with archinstall, you should run
```
sed -i 's|pacman-init|reflector|g' /usr/lib/python3.11/site-packages/archinstall/examples/guided.py
```
after that, run
```
curl https://raw.githubusercontent.com/Orange-OS-LE/OrangeOSLE2/main/install.py > install.py && python3 install.py
```
And after the install, reboot, log in then run this: 
```
sudo curl https://raw.githubusercontent.com/Orange-OS-LE/OrangeOSLE2/main/postinstall.py > postinstall.py && sudo python3 postinstall.py && rm postinstall.py
```
This is very much a work in progress. Make an issue if something doesn't work or goes wrong.
