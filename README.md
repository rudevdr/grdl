## What the script does?

Automatically builds debug android apk, by running `./gradlew` script in an existing gradle based project and then installs in an android device connected via adb.

Also, if a github url is provided then it clones the repo of the android project, then builds and installs apk via adb.

*This is just a simple script which install debug apk obtained by running ./gradlew script of the project. If  build fails, then you have to handle the exception and rerun the script.*

## Commands

`./grdl`	   - If current working directory is a gradle based system then builds and installs apk.

`./grdl <url>` - If a github url is passed as the argument then the script first clones the repo then builds debug apk and installs it on the adb device.


## Requirements before running the script

1. Edit the Sdk location in the script in the `$sdk` variable (in line 4). Path should be absolute like `/home/example/.Sdk` and not `~/.Sdk`

2. Check that only one adb device is connected to install the apk by running `adb devices`. If installation fails due to adb device not found or permission denied then connect a device via adb first and then rerun the script. 

## Sample

* If current working directory has a gradle based android project:

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
