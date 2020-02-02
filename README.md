# Manage environments and build types in React Native   

Init new RN application.
Create app folder.
Move App.js to app folder.
Modify the path to App.js in index.js file.
Create config.js file in app folder. We are going to leave this file empty for the moment.

```
$ react-native init RNInitApp
$ mkdir app
$ mv App.js app/App.js
$ touch app/config.js
``` 

Open RNConfigApp/ios/RNConfigApp.xcworkspace with XCode.
Delete tvOS target
Duplicate Target
In the new target General settings change the 'Display name' and 'Bundle identifier'.
When you create a new target Xcode will make a copy of the info.plist for the new target. We don't need two different info.plist files. Select the duplicated target and go to Build Settings, in Packaging change 'Info.plist file' to point to the original info.plist file.
Delete the info.plist file generated when duplicating the target.





In config.js file import NativeModules from react-native and call RNConfig module to get the application env vars.



I want to achieve:
- Get different env vars depending on the selected environment (ex.: staging and production).
- Once the configuration is done, adding or modifing an env var to the system will be as easy as setting a new key=value pair in a config file or modifing an existing one.
- Protect 


Extras
- Get buildType (ex.: debug and release) as a config parameter.
- Env vars are also available in Android and iOS environments, so you can use them for example from a Native component.

