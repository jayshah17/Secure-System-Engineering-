# Lecture 8

# 9. Access Control Issues – Part 1

When we open the adb logcat and click on the button, we can find the activity name. 

> Command – logcat | grep -i “APICredActivity”
 
So we run the following command:

adb shell am start –n jakhar.aseem.diva/.APICredsActivity

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/b47eb10a-fa16-4617-be0a-eda40d5a5f6f)

and confirm that when we run the following command with the device on the screen with the button.And it automatically shows the screen with the credentials without restrictions, like we had pressed the button.
