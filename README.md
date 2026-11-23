# Seamless

Seamless is an Android starter app for playing locally stored audio with an AMOLED-style interface.

## Create the GitHub repository
1. Create a repository named `Seamless`.
2. Extract this ZIP. Upload **the contents** of this folder to the repository root (so `.github` and `app` are at the top level).
3. Commit to `main`. The workflow starts on push, or use Actions → Build Seamless APK → Run workflow.
4. Download the `Seamless-APK` artifact from a successful run.

## Build requirements
- Android Gradle Plugin 8.7.3
- Gradle 8.9
- JDK 17
- Android SDK platform 35 and build-tools 35.0.0

The workflow deliberately does not invoke `android-actions/setup-android` or `sdkmanager`, because the supplied failure log shows that action failing while `sdkmanager` computes updates. It checks whether the hosted runner already has the required SDK packages and fails with a clear message if not.

## Current app scope
- AMOLED-style black interface
- Browse and play local audio files
- Play/pause, previous/next, seek bar
- Simple accent-colour selection
- Resizable home-screen widget shell

## Not yet implemented / not certified
This is a starter application, not a finished Spotify-equivalent player. Accurate word-by-word lyric synchronization, Whisper transcription, crossfade/gapless playback, beat-reactive visualization, full theme studio, and reliable background playback/media-session integration are not complete. The widget's Next control is not a full background playback transport implementation. Device testing is required.
