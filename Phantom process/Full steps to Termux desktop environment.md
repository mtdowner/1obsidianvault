[[Full steps to Termux desktop environment]]

# Setting up desktop environment all steps included

## Disable phantom process killer

1. Install Termux using F-Droid or GitHub.
2. Open Termux and allow access to storage:

```bash
termux-setup-storage
```

3. Change the mirror group (I chose the default under single, but I typically stick with all mirror groups in all regions):

```bash
termux-change-repo
```

4. Update packages and choose `y` if prompted:

```bash
sudo pkg update
```

```bash
sudo pkg upgrade
```

Or, you can do what I do:

```shell
sudo apt update -y && sudo apt upgrade
```
5.  Install `abd` toolkit

```bash
pkg install android-tools
```

6. Go to Settings and select About on phone or tablet. 
7. Under About, hit the build number 7 times to activate Developer options. 
8. Go back to Settings, and select System. 
9. Under System, select Developer options. 
10. Under Developer options, select Wireless debugging. Make sure WiFi is on before turning this on. Using your phone or tablet data will not work. 
11. Toggle Wireless debugging on and new options will appear below. 
12. At this point, this screen needs to stay up while running the next command in Termux. There are two options (that I know).
Either:
	1. Split the screen and open up Termux, or
	2. Download Termux Float and have that open.

13. Now select Pair device with pairing code under the Wireless debugging options.
14. A new window pops up with the pairing code, IP address, and port number. 
15. In Termux, pair the device with `adb pair` using the IP address and port number as listed followed by the WiFi pairing code.

```bash
adb pair <ip-address:port-number pairing-code>
```

Take note:
1. the semi-colon separating the IP address and port number without space, and
2. the space between the IP address:port number and the pairing code. For example:

```bash
adb pair 100.76.229.106:40085 617337
```

16. Now connect:

```bash
adb connect <ip-address:port-number>
```

For example:

```bash
adb connect 100.76.229.106:40085
```

17. Verify connection:

```bash
adb devices 
```

18. Now disable the phantom process killer!! Enter these next commands one after the other.

```bash
adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"
```

```bash
adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"
```

```bash
adb shell settings put global settings_enable_monitor_phantom_procs false
```

19. Enter these next commands to verify it's disabled:

```bash
adb shell "/system/bin/dumpsys activity settings | grep max_phantom_processes"
```

```bash
adb shell "/system/bin/device_config get activity_manager max_phantom_processes"
```

20. If `2147483647` was returned, the phantom process killer has successfully been disabled.


## Install desktop using `proot-distro`
1. Install  `proot-distro`:

```bash
pkg install proot-distro
```

2. View available distros, and switch over to it after installation:

```bash
proot-distro list
proot-distro install <alias>
# proot-distro install ubuntu-lts
proot-distro login <alias>
# proot-distro login ubuntu-lts
```

3. Update packages

```bash
cat /etc/os-release
apt update
apt upgrade
apt install sudo nano
```

4. Enter command to add a new user followed by the desired username:

```bash
adduser <username>
#adduser missy
```

5. Follow the prompts. Nothing will indicate a password is being typed which is normal.
6. Open the `sudoers` file:

```bash
nano /etc/sudoers
```

7. Edit `sudoers` file to give new user root privileges. 
8. Find the section stating `# User privilege specification` to add the new user underneath the `root` entry:

```bash
# User privilege specification
root    ALL=(ALL:ALL) ALL
missy   ALL=(ALL:ALL) ALL
```

1. Save the file without changing the file's name by typing `ctrl + X` to exit then `y` to save followed by pressing enter to keep the name the same.
2. Switch over to new user, and update packages:

```bash
su missy
sudo apt update && sudo apt upgrade -y
```

3. Enter password when prompted. 
4. Install packages needed for the desktop environment:

```bash
apt install xfce4 xfce4-goodies tightvncserver
```

5. Choose keyboard layout by entering the number associated. 
6. Create `.vnc` directory with a file called `xstartup`

```bash
mkdir .vnc
cd .vnc
touch xstartup
nano xstartup
```

7. Add the following line to `xstartup`:

```bash
xfce4-session &
```

8. Exit and save the modified file.
9. Make the file executable by running:

```bash
chmod +x xstartup
```

10. Start the vnc server:

```bash
vncserver -localhost
```

12. Provide a password if a password wasn't set earlier. Password has a maximum of 8 characters.
13. 
14.
