# TOT

### Hey there!
### Make sure to install all the software mentioned below to get the environment setup ready. 


| Software      | Link/Command/version           |
| ------------- |:-------------:|
| Android studio/Android SDK      | [Android Studio](https://developer.android.com/studio?gclid=CjwKCAjwr56IBhAvEiwA1fuqGtsFGKAqttKRoMXfKzNpxb1yjTVvlvKJl1uJjwZ22lk5oepp8O8XRxoCy14QAvD_BwE&gclsrc=aw.ds#downloads) |
| Xcode 12.5+ (macOS only)     | [Xcode](https://apps.apple.com/us/app/xcode/id497799835?mt=12)      |
| NodeJS v14.17.3 | [NodeJS](https://nodejs.org/download/release/v14.17.3/)      |
| Cordova | `npm i -g cordova@11.1.0`      |
| ionic (v5.4.16) | `npm i -g ionic@5.4.16`      |
| native-run | `npm i -g native-run`      |
| JDK  | version 11      |
| cocoapods (macOS only)  | latest version      |


# Environment variables

Now set path for Java, Android home and Platform-tools

ex on macOS: 
```sh
export ANDROID_HOME=/home/pc1125/Android/Sdk
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64
PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```
On Windows please follow the steps mentioned in this link: [Windows environment variables](https://docs.oracle.com/en/database/oracle/machine-learning/oml4r/1.5.1/oread/creating-and-modifying-environment-variables-on-windows.html#GUID-DD6F9982-60D5-48F6-8270-A27EC53807D0)


# Commands to setup repository.

Run these commands in root of repository.

1. Install node modules.
```
npm i
```
2. Install the platforms.

```sh
ionic cordova platform add android@11 --save
```
If you are on macOS then install iOS 
```sh
ionic cordova platform add ios --save
```

Above commands should automatically install all plugins listed in `package.json`, so no need to install them individually.

# Running on device/emulator.

First let us run build command to make sure all the code written is fine with syntax.

```sh
ionic cordova build android # ios or android based on platform usage
```

Once the build is successful, then we shall proceed on running devices, emulator or simulators(iOS virtual devices).

Following command can be used to run on the device connected to system. we can specify target also while running it on devices [more info](https://ionicframework.com/docs/cli/commands/cordova-run) 

```sh
ionic cordova run android # ios or android based on platform usage
```

# Here are some useful commands.

```sh
native-run --list # This will list all the avaialable devices, this include simulator and emulators.
adb devices # This will list all android devices connected to system.
ionic info # This gives overall information about this ionic project.
ionic cordova plugin add pluginName or pluginID # To add new plugin.
ionic cordova plugin rm pluginName or pluginID # To remove installed plugin.
ionic cordova platform add platformName # To add support for mentioned platform.
ionic cordova platform rm platformName # To remove support for mentioned platform.
```

# Importand links:

1. [Ionic V3](https://ionicframework.com/docs/v3/)
2. [Cordova plugins](https://cordova.apache.org/plugins/)
