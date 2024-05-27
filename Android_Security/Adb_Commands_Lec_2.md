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

> adb devices

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/6acdf602-c722-4593-b2ca-37e10446cc86)

> adb -s emulator-5554 shell

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/57b23998-8d6c-4259-8b05-8e58ae7daef3)

> id


![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/a5ab19d3-ac5a-4bce-bd33-11495117f07a)

> pm list packages has various options to configure the output. -3 option is used to filter and display only
show third party packages. -s option is used to filter and display only system packages.


![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/45c06d0f-af41-465a-9e8c-d6a9428391ae)


> pm list packages | grep youtube


![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/e5dcf83d-58f6-4a04-a0df-cd6e39ea6520)


> pm list packages -3


![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/baa151a2-6ac6-49f6-8117-f6f4e8b319ee)

> To check the Process ID (PID) of the currently running applications, we use the ps -A command.
> ps -A | grep androidsecapp


![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/549d65f4-4f3e-4adb-b0ae-c6888b887911)

> pm path is used to get the path of the installed APK file.


> pm path com.example.androidsecapp

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/93eeb5dc-a4d0-44fb-a24e-5030c67e3a63)

> adb pull "Path pf the Application"

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/b7bb89e3-97d9-4e36-8ef8-ba2467a97886)

> echo "This is some random secret file" > randomfile.txt
adb push randomfile.txt /sdcard/

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/36456b34-f4be-49d0-b68c-ddf2e24ca209)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/09238df7-421a-4223-b3ac-087cdec4b457)

Find Application UID

> pm list packages -U

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/8e76eb7c-956d-4938-9f97-42c97d08cc03)


