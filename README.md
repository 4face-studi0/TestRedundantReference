# TestRedundantReference

#### [Issue tracker](https://issuetracker.google.com/issues/130329181)

## How to crash the OS 

#### and see your Android device rebooting

Simply run the app / install the APK and run it

## How to reproduce in development

**AndroidManifest.xml**

```xml
android:theme="@style/AppTheme"
```

**styles.xml**

```xml
<style name="AppTheme" ...>
    <item name="android:windowBackground">@drawable/crash</item>
</style>
```

**crash.xml**

```xml
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:drawable="?attr/background"/>
</layer-list>
```

## Expected result

**Runtime Exception**

## Current result

**OS crashes and phone suddently reboot**

