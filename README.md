This plugin used to be deprecated, but we need to reinstate it since iOS 13 broke the autoFocus selector again. This means that the previously integrated changes in the official plugins (e.g. `cordova-plugin-wkwebview-engine` version `1.2.1`) no longer work on iOS 13 so the same focus bug has regressed. Apply this plugin temporarily until the issue is fixed in the main repositories.

## Usage

Add this to your `package.json`:
```
{
  "dependencies": {
    "cordova-plugin-wkwebview-inputfocusfix-ios13": "git+https://github.com/uofa/cordova-plugin-wkwebview-inputfocusfix-ios13"
  },
  "cordova": {
    "plugins": {
      "cordova-plugin-wkwebview-inputfocusfix-ios13": {}
    },
  }
}
```
Then just clean your `platforms/ios` directory and rebuild.

Once the main `wkwebview` fixes this issue for iOS 13 as well (see links below), you can stop using this plugin.

### THIS PLUGIN IS DEPRECATED!

This plugin was introduced as a temporary fix for the input focusing issue raised on main WKWebView repositories of Apache and Ionic. As the changes are merged to the main repositories - https://github.com/apache/cordova-plugin-wkwebview-engine/pull/37/ and https://github.com/ionic-team/cordova-plugin-wkwebview-engine/pull/171, the plugin is deprecated and has no effect on fixing any focus issues anymore. 

### If you're facing issues with the input focusing, simply upgrade your wkwebview cordova plugin to it's latest version. And if your issue still exists after the upgrade, open an issue on the main wkwebview cordova repo: https://github.com/apache/cordova-plugin-wkwebview-engine/issues.  
