To create an app like this:

1. Install cordova cli
2. `cordova new appname`
3. Adjust config.xml so it looks like ours
4. `cordova platform add ios`
5. In your reapp app:
  - Build for ios: `reapp build ios`
  - Copy assets to cordova: `rsync -av ./build/public/ ~/PATH_TO_YOUR_CORDOVA_APP/www && (cd ~/PATH_TO_YOUR_CORDOVA_APP && cordova prepare)`
6. Open the .xcodeproj in Xcode (it's in your platforms folder)
7. Build using xcode
8. Make splash screens and icons:
  - splash: https://github.com/elistone/ios-splashscreen-template-v2
  - icon: http://appicontemplate.com/