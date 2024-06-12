# Input Validation Issues- Part 1

We explore the application by entering values in the search EditText field

We observe the decompiled source code in the JADX.

 ![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/ebcd2c51-9b72-43ef-ad2e-b67401b55360)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/3a5ace72-cc57-4227-92ed-d4c68a6e9aaa)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/5950665d-aa16-480d-b471-d31ff4a437ef)

We understand that for this Task an activity called SQLInjectionActivity is used.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/4b68873c-32ce-4980-946d-b4cef9bad653)

We enter 1' OR 1=1-- so that the above SQL query becomes

SELECT * FROM sqliuser WHERE user ='1' OR 1=1--'

The WHERE clause condition gets evaluated to FALSE or TRUE which is equivalent to TRUE, hence all the records in the database are displayed in the Toast message.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/3b87410b-7e66-4370-9e80-3be53b1470c5)

Input Validation Issues- Part 2

We explore the application by entering values in the URL EditText field.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/0814c748-abf8-4adb-9016-3267aebc1f73)

We enter a sensitive path like
file:///data/data/jakhar.aseem.diva/shared_prefs/jakhar.aseem.diva_preferences.xml
Which only the application has access to and normal user of the device does not have access to. We observe that the file contents are displayed in the WebView.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/4f8f3d87-7a54-4cc3-8d0a-dc725b1918cb)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/7fd8f4d7-016c-487d-8b41-f4cf5088deca)
 
We observe the decompiled source code and open the InputValidation2URISchemeActivity in the JADX.
We observe that the user input value in the EditText field is used directly to load in the WebView without any sanitization or validation.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/ba3d9fe6-ff0f-482e-bdae-f0311b9cd7ca)
