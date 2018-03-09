# fluidsynth-android-opensles
This is a sample project which strives to use fluidsynth as a native android library with OpenSL ES support


The original fluidsynth repository can be found here: [FluidSynth/fluidsynth](https://github.com/FluidSynth/fluidsynth)

Adjustments, or better yet additions, to build fluidsynth for the Android platform where made by VolcanoMobile in this repository: [VolcanoMobile/fluidsynth-android](https://github.com/VolcanoMobile/fluidsynth-android)

I set up a fresh Android project via AndroidStudio, simply copied over all relevant files from [VolcanoMobile/fluidsynth-android](https://github.com/VolcanoMobile/fluidsynth-android) and referenced the `android/CMakeLists.txt` within the app's `build.gradle`. That works in the sense that it compiles and fluidsynth can be used within the app (i.e. JNI). But in order to be able to build fluidsynth for Android VolcanoMobile exluded all Audio-Driver classes, thus removing the ability to actually hear any MIDI events.

To enable audio with fluidsynth on Android with the OpenSL ES audio framework [atsushieno](https://github.com/atsushieno) made independent changes to fluidsynth in his own fluidsynth [fork](https://github.com/atsushieno/fluidsynth). I was not able to build that project. But, since I was able to build VolcanoMobiles version of fluidsynth I thought it might be possible to only include atsushienos changes into VolcanoMobiles version. This project tries to do exactly that.
