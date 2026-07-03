---
{"dg-publish":true,"permalink":"/cs-312-mobile-application-development/notes/activity-lifecycle-basics/","created":"2026-07-03T18:32:16.925+08:00","updated":"2026-07-03T20:24:47.827+08:00","dg-note-properties":{}}
---


---

#### Activity
Represents a **single screen** in your app.

Each activity goes through a series of **lifecycle states** as the user interacts with the app or switches between apps. Proper management of these states ensures efficient resource usage, smooth user experience, and preservation of user data.

Lifecycle states:
- `onCreate()` - first time activity is created
- `onStart()`- activity becomes visible
- `onResume()`- activity is in the foreground
- `onPause()`- partially hidden
- `onStop()`- completely hidden
- `onDestroy()`- activity is destroyed

##### Camera Lifecycle
1. `onCreate()`- Opening of camera app from home screen
2. `onStart()`- UI of camera app is now visible on the screen. Only partially active.
3. `onResume()`- App can now be used, interacted, can press capture buttons, and more. Active state.
4. `onPause()`- Using the app, taking pictures when suddenly a notification popup intrudes the screen from above. App is still visible but it changed to Unfocused mode (not active).
5. `onStop()`- App is no longer visible, interactable after clicking the notification (changing apps). It is still loaded into memory, *only requiring to be navigated back to resume process.*
6. `onRestart()`- From the other app, loading back to the camera app.
7. `onDestroy()`- App closed by the user, memory released.