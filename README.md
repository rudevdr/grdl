## What script does?
Bash script to automatically build and install android apk from a gradle based project.

Shell script to download an android project from repo and build debug apk and install in android device via adb.

## Commands
./grdl <url> - If a github url is passed as the argument then the script first clones the repo then builds debug apk and installs it on the adb device.

./grdl		 - if pwd is a gradle based system then builds and installs apk.


## Requirement before running the script

1. Edit the Sdk location in the script in the $sdk variable. Path should be absolute.
2. Check if one adb device is connected to install by running `adb devices`. If installation fails due to adb device not found then connect a device via adb first then rerun the script. 

## Sample

* If already inside a gradle based android project:
`$ ./grdl`

* If you want to build and install a gradle based android project from github:

`$ ./grdl https://github.com/kaushikgopal/RxJava-Android-Samples`

, which is similar to:  

```bash
$ git clone https://github.com/kaushikgopal/RxJava-Android-Samples
$ cd RxJava-Android-Samples
$ ./grdl
```
