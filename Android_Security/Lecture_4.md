# Intents in Android 

Intents are messaging objects used to request an action from another app component. They 
are a fundamental aspect of Android development, allowing for communication between 
different components of an application or between different applications. 

# Implicit Intent 

Definition: An implicit intent does not specify the component to receive the intent. 
Instead, it declares a general action to perform, which allows a component from 
another app to handle it. 

* Usage: The Android OS determines which component(s) can handle the intent based 
on the action specified and any data associated with it.
* Example: If you want to open a webpage, you create an intent with the action 
Intent.ACTION_VIEW and the URL. The OS will then decide which activity (e.g., a web 
browser) can handle this intent.

* Example xml: 

Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse("http://www.example.com")); 
startActivity(intent); 
 
# Explicit Intent 

Definition: An explicit intent specifies the exact component (activity, service, or 
broadcast receiver) to handle the intent. This is done by providing the component's 
class name. 
* Usage: It is used within the same application when you know the exact activity or 
service that should respond to the intent. 
* Example: Starting an activity within the same app by explicitly mentioning its class. 

* Example xml:
  
Intent intent = new Intent(this, TargetActivity.class); 
startActivity(intent);
