Name: Jay Shah
Roll No: CB.SC.P2CYS23009

Hands On ADB Commands 

* Android Debug Bridge (adb) is a versatile command-line tool that lets you communicate with a device.
* The adb command facilitates a variety of device actions, such as installing and debugging apps. adb provides access to a Unix shell that you can use to run a variety of commands on a device.
* It is a client-server program that includes three components:
  * A client, which sends commands. The client runs on your development machine. You can invoke a client from a command-line terminal by issuing an adb command.
  * A daemon (adbd), which runs commands on a device. The daemon runs as a background process on each device. The daemon on the Android device connects with the server on the host PC over USB or TCP, which connects to the client that is used by the end-user over TCP.
  * A server, which manages communication between the client and the daemon. The server runs as a background process on your development machine. The default port number on which the adb server runs is 5037.


> adb is included in the Android SDK Platform Tools package, which is installed at ${ANDROID_HOME}/platform-tools/.
* If the Android SDK is not installed in the system, we can use the sudo apt install android-tools-adb command to install adb as a system package.
* After the PATH environment variable is set appropriately, we verify the program execution by typing adb in the terminal.
