Apart from the general `BUILDING.md` there are certain things that have
to be done by Signal-iOS maintainers.

For transperancy and bus factor, they are outlined here.

## Dependencies

Keeping cocoapods based dependencies is easy enough.

`pod update`

### WebRTC

We don't currently have an automated build (cocoapod/carthage) setup for
the WebRTC.framework. Instead, read the WebRTC upstream source and build
setup instructions here:

https://webrtc.org/native-code/ios/

Once you have your build environment set up and the WebRTC source downloaded:

    cd webrtc
    # build a fat framework
    src/webrtc/build/ios/build_ios_libs.sh
    # Put it in our frameworks search path
    mv src/webrtc/ios_libs_out/WebRTC.framework ../Signal-iOS/Carthage/Builds

## Translations

Read more about translations in [TRANSLATIONS.md](signal/translations/TRANSLATIONS.md)
