*Checking for spyware in your android phone using linux...*
[]: # Path: README.md
Using the mvt tool built with python...

*Mobile Verification Toolkit*

[]: # Path: README.md

Mobile Verification Toolkit (MVT) is a collection of utilities to simplify and automate the process of gathering forensic traces helpful to identify a potential compromise of Android and iOS devices.

Find more information about the toolkit below.

[Github](https://github.com/mvt-project/mvt).

[]: # Path: README.md

Warning: MVT is a forensic research tool intended for technologists and investigators. Using it requires understanding the basics of forensic analysis and using command-line tools. This is not intended for end-user self-assessment. If you are concerned with the security of your device please seek expert assistance.

*Installation*

MVT can be installed from sources or from PyPi (you will need some dependencies, check the documentation):

        pip3 install mvt

[]: # Path: README.md

You need the blow tool to use it on android phones.

**How to setup ADB on Linux**

[]: # Path: README.md

Download the Android SDK Platform Tools ZIP file for Linux.

Extract the ZIP to an easily-accessible location (like the Desktop for example).
Open a Terminal window.

Enter the following command: cd /path/to/extracted/folder/
This will change the directory to where you extracted the ADB files.

So for example: cd /Users/Doug/Desktop/platform-tools/
Connect your device to your Linux machine with your USB cable. Change the connection mode to “file transfer (MTP)” mode. This is not always necessary for every device, but it’s recommended so you don’t run into any issues.

Once the Terminal is in the same folder your ADB tools are in, you can execute the following command to launch the ADB daemon: ./adb devices

Back on your smartphone or tablet device, you’ll see a prompt asking you to allow USB debugging. Go ahead and grant it.

Finally, re-enter the command from step #8. If everything was successful, you should now see your device’s serial number in the Terminal window output.

**ADB COMMNADS**

[]: # Path: README.md

Below, you’ll find a list of example commands which you can do on your device:

Print a list of connected devices: 

        adb devices

Kill the ADB server:

         adb kill-server

Install an application: 

        adb install <path_to_the_APK_file>

Set up port forwarding: 

        adb forward tcp:6100 tcp:7100

Copy a file/directory from the device:

         adb pull <path_to_the_remote_object> <path_to_the_local_destination>

Copy a file/directory to the device: 

        adb push <path_to_the_local_object> <path_to_the_remote_destination>

Initiate an ADB shell: 

        adb shell

# NOTE

The guide above will certainly work for you, but those own a Debian or Fedora/SUSE-based distro of Linux can skip steps 1 and 2 of the guide above and use one of the following commands:

Debian-based Linux users can type the following command to install ADB:

        sudo apt-get install android-tools-adb

Fedora/SUSE-based Linux users can type the following command to install ADB:

        sudo yum install android-tools
