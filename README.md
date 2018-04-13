## Bash script to automatically build and install android apk from a gradle based project

##Commands
./grdl <url> - If a github url is passed as the argument then the script first clones the repo then builds debug apk and installs it on the adb device.

./grdl		 - if pwd is a gradle based system then builds and installs apk.


##Requirement before running the script

1. Edit the Sdk location in the script in the $sdk variable. Path should be absolute.
2. Check if one adb device is connected to install. If installation fails due to adb device not found then connect a device via adb first then rerun the script. 

