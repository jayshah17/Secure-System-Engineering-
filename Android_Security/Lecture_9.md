# Lecture 9
# 11. Access Control Issues – Part 3

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/e3c4ce50-2cc5-4704-9b3a-c535faf61fd2)

Let’s Create a PIN and Access the Private Notes via the Generated PIN.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/94ae972c-74c0-4009-bddf-16397facf151)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/329009ad-fd92-4bb4-87eb-edcaab8afe5e)

Our Goal is to access the Private Notes without interacting with the application,

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/b8cef388-3d73-47c0-a4c5-3b06a32421d8)

2 Files has been logged while creating PIN and Viewing the Private Notes. Analyze the Source code in the JADX.
 
![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/f2a8e957-4f02-4865-978f-4802730c8bef)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/51c6127c-33cd-4e58-b833-dddf49ea45b7)

We can see our AccessControl3Activity stores our pin via a SharedPreferences object, which we covered way back when. When we enter the pin saved in shared_prefs, it launches the AccessControl3NotesActivity activity which validates this pin before showing the notes via
a query(NotesProvider.CONTENT_URI) content query. This content provider will dump all of the notes.
We can dump this content provider via the following command in our terminal:
adb shell content query --uri content://jakhar.aseem.diva.provider.notesprovider/notes/
