# Singleton_Class

Singleton_Class

- A singleton class can only have exactly one instance through the entire application lifecycle.
- That single instance is only accessible through a static property and the initialized object is usually shared globally.

# The UIApplication Object

- Every iOS app has exactly one instance of UIApplication. (or, very rarely, a subclass of UIApplication). 
- When the app is launch the system calls a function named: **UIApplicationMain(_:_:_:_:)**.
# - **UIApplicationMain(_:_:_:_:)** creates an Singleton UIApplication object.
- After you access the object UIApplication with the method shared class method.
- The UIApplication class defines a delegate that conforms to the **UIApplicationDelegate** protocol and must implement some of the protocol’s methods. 

# The application delegate

- Your "App Delegate" is the starting point of your application, and every iOS application has one
- The single instance of AppDelegate is responsible for processing events and coordinate the work of other objects in the app.
- When an iOS is launched, there is alot of behind the scenes.
- During this phase , an instance of  UIApplication is created to control your Application's state and act as liason.

### What is liason ? One that maintains communication.

- UIKit automatically creates an instance of the app delegate class provided by Xcode and uses it to execute the first bits of custom code in your app.
# The app delegate is effectively the root object of your app. 
- Like the UIApplication object itself, the app delegate is a singleton object and is always present at runtime. 
- Although the UIApplication object does most of the underlying work to manage the app, you decide your app’s overall behavior by providing appropriate implementations of the app delegate’s methods.
- Although most methods of this protocol are optional, you should implement most or all of them.

- During the launching also is created an instance of AppDelegate and set as the delegate of the UIApplication instance. This is why the name of "app delegate"
- while the application is being launched, it is not ready for work or input.
- when this changes the UIApplication instance sends its delegate the message **application:didFinishLaunchingWithOptions**.
  * Important! Put everything that needs to happen or needs to be in place before the user interacts with the application.
  
