## What the script does?

It's a Linux/Unix Shell script which automatically builds and install android apk from a gradle based project.

Also, it can download android project from github repository and builds the debug apk and then install it in android device via adb.

*This is just a simple script which install debug apk obtained by running ./gradlew script of the project. If there is exception in building which doesn't produce apk, then you have to handle the exception and rerun the script.*

## Commands

`./grdl`	 - if pwd is a gradle based system then builds and installs apk.

`./grdl <url>` - If a github url is passed as the argument then the script first clones the repo then builds debug apk and installs it on the adb device.


## Requirement before running the script

1. Edit the Sdk location in the script in the $sdk variable. Path should be absolute.
2. Check one adb device is connected to install the apk by running `adb devices`. If installation fails due to adb device not found or permission failed, then connect a device via adb first and then rerun the script. 

## Sample

* If already inside a gradle based android project:

```bash
$ ./grdl
```

* If you want to build and install a gradle based android project from github:

```bash
$ ./grdl https://github.com/amitshekhariitbhu/RxJava2-Android-Samples
```

, which is similar to:  

```bash
$ git clone https://github.com/amitshekhariitbhu/RxJava2-Android-Samples
$ cd RxJava2-Android-Samples
$ ./grdl
```
