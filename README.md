# PhoneGap App

## Development environment

### Prerequisites

 - node.js http://nodejs.org/
 - npm https://npmjs.org/

Once npm is installed, install PhoneGap using

    sudo npm install -g phonegap

#### MacOS X

The stack is easier to install in MacOS X using Homebrew: http://brew.sh/, a useful guide can be found in in http://shapeshed.com/setting-up-nodejs-and-npm-on-mac-osx/


### iOS

#### Set-up

Prerequisites:

 - Xcode
 - Xcode command-line tools
 - iOS emulator

Make sure to have installed xcode and the command-line tools. To validate, run: 

    xcodebuild -version

#### Build

To compile the app for iOS use:

    $ phonegap local build ios
    [phonegap] detecting iOS SDK environment...
    [phonegap] using the local environment
    [phonegap] compiling iOS...

#### Run

To run the app use:

    phonegap run ios

#### Troubleshooting

If "[error] An error occurred while emulating/deploying the ios project. Cordova needs ios-sim version 1.7 or greater, you have version 1.5.1." is gotten, upgrade ios-sim using

    brew upgrade ios-sim


### Android

#### Set-up

Prerequisites:

 - JDK
 - Ant
 - Android SDK

Make sure to have installed a copy of the Android SDK. Phonegap only supports API17, use the `android` command to install it if necessary

JAVA_HOME variable has to be defined; Android SDK tools and platform-tools have to be in the PATH. 

##### MacOS X

In MacOS X the PATH and other environment variables can be modified by editing the file .bash_profile in the user's home folder. For example:

    export JAVA_HOME=$(/usr/libexec/java_home)
    export PATH=$PATH:/path/android-sdk-macosx/tools:/path/opt/android-sdk-macosx/platform-tools

**Tip**

Installing Ant in MacOS X is easy with Brew, just do:

    brew install ant

#### Build

To build the app for Android use:

    $ phonegap local build android
    [phonegap] adding the Android platform...
    [phonegap] compiling Android...
    [phonegap] successfully compiled Android app
    [phonegap] successfully compiled iOS app

#### Run

To run the app use, better if an Android device is connected to the computer USB (in debug mode):

    $ phonegap run android
    [phonegap] detecting Android SDK environment...
    [phonegap] using the local environment
    [phonegap] compiling Android...
    [phonegap] successfully compiled Android app
    [phonegap] trying to install app onto device
    [phonegap] no device was found
    [phonegap] trying to install app onto emulator
    [phonegap] successfully installed onto emulator

## Project Development

The project is largely supported by Foundation http://foundation.zurb.com/, to modify existing look of the library and minify the current JS and CSS code two 

### Requirements

You'll need to have the following items installed before continuing:

 - npm https://npmjs.org/

Go to the 'www' directory and do `npm install`. Once done this, run `bower install` to pull the rest of the dependencies

### Work

While you're working on your project, cd to the 'www' folder and run:

`grunt`

And you're set!

### Directory Structure

  - `scss/_settings.scss`: Foundation configuration settings go in here
  - `scss/app.scss`: Application styles go here


