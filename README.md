# Android Studio wo/ using Android Studio 📱
Simple template for Android Studio Projects for be used in other enviroments

## Requirements
1. Android SDK (and all its set up)
2. JDK
3. Code editor
4. Know how to use the terminal (Recomendation)
5. Preferably use a physical device (Recomendation)
6. [Android Visualizer](https://labs.udacity.com/android-visualizer/) way to see this stuff you're designing in the XML (Optial)

## How to Use
**First**, click here > [Use this template](https://github.com/simmxns/apk-template/generate)
### Visual Studio Code way
1. Install [Android by adelphes](https://marketplace.visualstudio.com/items?itemName=adelphes.android-dev-ext)
2. Install Java Support [Language Support for Java(TM) by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)

*then* <br>
Open the terminal and put this inside
```bash
.\gradlew build
.\gradlew assembleDebug
```
And finally compile(Ctrl + F5) or debug(F5) your app

### (Neo)Vim way
Put this in your init.vim
```vim
Plug "hsanson/vim-android"
```
With [COC](https://github.com/neoclide/coc.nvim) install Java. (I personally recommend this way because with LSP you need to do things that coc do more easier)
<br>
`:CocInstall coc-java`
