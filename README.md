# zebraCapacitor
Capacitor plugin for Zebra printers (ios and android)

## Limitations
Currently the iOS implementation is incomplete, but you can discover connect and print.
Also, the Android implementation is not well tested and likely missing important things.
Also, the web implementation which is just a stub is broken.
Also, this is built using alpha.36 version of Capacitor

## But
I do intend to develop and support an app that uses this plugin, so this will eventually be completed and working (at least with for the printers I have access to test with).

##iOS
After installing this, you may have to drag the libZSDK_API.a library into the ZebraCapacitor target of the Pods Project. Then update your build settings Library Search Paths with: "${PODS_ROOT}/../../../node_modules/zebra-capacitor/ios/Plugin/Plugin"
I've updated the podspec so this may not be necessary anymore, but I havn't tested it yet.

Also for iOS update your apps Info.plist file with Supported external accessory protocols as an array with the value com.zebra.rawport

Add this to your plist
```
<key>UISupportedExternalAccessoryProtocols</key>
<array>
    <string>com.zebra.rawport</string>
</array>
```

I'll experiment with trying to automate this via the podspec as well.