# Screen Share in Android
**Learn how to implement Screen Share on Android**
In this guide we'll show you how to share your Android application screen with other participants connected to the Room. 

**Using the Screen Capturer API**
The [ScreenCapturer](https://media.twiliocdn.com/sdk/android/video/releases/1.0.0-beta6/docs/) class is used to provide video frames for a `[LocalVideoTrack](https://media.twiliocdn.com/sdk/android/video/releases/1.0.0-beta6/docs/com/twilio/video/LocalVideoTrack.html)` from a device's screen. The frames are provided via the `MediaProjection` api. This capturer is only compatible with `Build.VERSION_CODES.LOLLIPOP` or higher.

**Build a Permission model to enable Screen Share**
Implement a UI layout with menu items to let the user Start/Stop Screen Share.
<Link to Screen Shot>

**Request Screen Capture permission** 
Get an instance of the [MediaProjectionManager](https://developer.android.com/reference/android/media/projection/MediaProjectionManager.html) service. Call the [createScreenCaptureIntent] method in a new activity. This initiates a prompt dialog for the user to confirm screen projection.

<Code snippet link>


**Start Screen share when permission received** 
Initialize the [ScreenCapturer] class, after permission is received from the user. Add the local media video track to the [LocalVideoTrack](https://media.twiliocdn.com/sdk/android/video/releases/1.0.0-beta6/docs/com/twilio/video/LocalVideoTrack.html) object and pass the `ScreenCapturer` object to pass the captured local video frames. Set the [VideoView] object to [Visible] . Call the `addRender` method on the [LocalVideoTrack] object and pass the [VideoView] object to begin receiving the screen capture video. 

<Code snippet link>