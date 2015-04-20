To create an app like this:

1. Install cordova cli
2. `cordova create appname`
3. Adjust config.xml so it looks like ours
4. `cordova platform add ios`
5. Add plugins we use:
  - com.telerik.plugins.wkwebview 0.3.5 "WKWebView Polyfill"
  - org.apache.cordova.console 0.2.13 "Console"
  - org.apache.cordova.device 0.3.0 "Device"
  - org.apache.cordova.inappbrowser 0.6.0 "InAppBrowser"
  - org.apache.cordova.statusbar 0.1.10 "StatusBar
  - To add a plugin run `cordova plugin add <plugin name>`
6. In your cordova app:
  - `rm -r www`
  - `ln -s ../PATH_TO_REAPP_APP/build/ios www`
7. In your reapp app:
  - Build for ios: `reapp build ios && (cd ~/PATH_TO_YOUR_CORDOVA_APP && cordova prepare)`
8. Open the .xcodeproj in Xcode (it's in your platforms folder)
9. Build using xcode
10. Make splash screens and icons:
  - splash: https://github.com/elistone/ios-splashscreen-template-v2
  - icon: http://appicontemplate.com/


Extra reading:

 - WKWebView
   - cordova plugin add https://github.com/Telerik-Verified-Plugins/WKWebView
   - http://stackoverflow.com/questions/25017933/cordova-how-to-remove-push-notification-on-ios
 - statusTap (couldnt get working) https://github.com/triceam/cordova-statusTap
 - screenshots http://stackoverflow.com/questions/25756863/full-resolution-screenshots-for-iphone-6-and-6
 - iOS8 scroll events change http://developer.telerik.com/featured/scroll-event-change-ios-8-big-deal/
