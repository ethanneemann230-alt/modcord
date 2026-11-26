# Modcord

A from-scratch Discord client (gateway + REST + state cache + UI) in one file: `www/index.html`.

## Get the APK (no Android Studio needed)
1. Create a new GitHub repo and push this folder to it.
2. Open the repo's Actions tab, run "Build APK" (it also runs on every push).
3. Download the `modcord-apk` artifact, unzip it, and install `app-debug.apk` on your phone.

## Build locally instead
Needs Node 20+, JDK 21, Android SDK:
    npm install && npx cap add android && npx cap sync android
    cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

## Bot setup
Developer Portal > your app > Bot: turn on Message Content Intent, copy the token,
then invite the bot to a server (OAuth2 > URL Generator > scope "bot", permissions
View Channels, Read Message History, Send Messages).
