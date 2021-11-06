# Android Studio wo/ using Android Studio 📱
Simple template for Android Studio Projects for be used in other enviroments

## Requirements
1. Android SDK [and all its set up]()
2. JDK
3. Code editor
4. Know how to use the terminal (Recomendation)
5. Preferably use a physical device (Recomendation)
6. [Android Visualizer](https://labs.udacity.com/android-visualizer/) way to see this stuff you're designing in the XML (Optial)

## How to Use
**To get started,** click here > [Use this template](https://github.com/simmxns/apk-template/generate)
### Visual Studio Code way
1. Install [Android (by adelphes)](https://marketplace.visualstudio.com/items?itemName=adelphes.android-dev-ext)
2. Install Java Support [Language Support for Java(TM) by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)

*then* <br>
Open the terminal and put this inside
```bash
.\gradlew build
.\gradlew assembleDebug
```
And finally compile your apk.<br>
<b>⚠️WARN:</b> <i>Each time you wanna compile it, before, you must have to run the second comand.</i>

### (Neo)Vim way
Put this in your init.vim
```vim
Plug "hsanson/vim-android"
```
With [COC](https://github.com/neoclide/coc.nvim) install Java. (I personally recommend this way because with LSP you need to do things that coc do more easier) <br>
`:CocInstall coc-java`

### CMD way
In your terminal build the project then just install the apk and open it.
```bash
.\gradlew build
.\gradlew installDebug
```
<b>⚠️WARN:</b> <i>I think it's a bit obvious, but before all this, you should link your devices with ADB</i> 
1) Connect your device
2) Run `adb devices`
3) And yeah, that's it

## SDK set up
1) Install SDK Tools package https://developer.android.com/studio<br>
Go to the bottom of the page, then in "Command line tools only" dowload the cmdline-tools of your preference, (win in my case).
3) Unzip the downloaded package, create a folder named "AndroidSDK" or however you want, and put the unzipped folder into it.
4) Into cmdline-tools create other folder named "tools" and put the content of cmdline-tools into.
5) Open a terminal on the root folder for then run this (command by command).<br>
(Powershell)
```bash
cd .\cmdline-tools\tools\bin
.\sdkmanager.bat "platform-tools" "build-tools;30.0.2" "platforms;android-25"
```
platforms;android-25 is android 7 change it for whatever you want [SDK Platform Release Notes](https://developer.android.com/studio/releases/platforms)<br>
6) Replace the created folder "tools" with this version [tools@25.2.5](https://dl-ssl.google.com/android/repository/tools_r25.2.5-windows.zip) it's just for you can use the android.bat, for me is useful, downloading or not it's up to your.
7) Set the enviroments variables.<br>
<b>Account variables:</b><br>
<table>
  <tr>
    <th>Variable</th>
    <th>Values</th>
  </tr>
  <tr>
    <td>ANDROID_HOME</td>
    <td>C:\AndroidSDK</td>
  </tr>
  <tr>
    <td>ANDROID_SDK_ROOT</td>
    <td>C:\AndroidSDK</td>
  </tr>
</table>

<b>PATH variables:</b><br>
```
%ANDROID_HOME%\cmdline-tools\tools\bin
%ANDROID_HOME%\emulator
%ANDROID_HOME%\platform-tools
%ANDROID_HOME%\tools
```
Considering the location of the Android SDK is at the root of disk C:\
8) Done!
