---
{"dg-publish":true,"permalink":"/cs-312-mobile-application-development/notes/api-levels-application-programming-interface/","created":"2026-07-03T18:46:58.748+08:00","updated":"2026-07-03T20:25:37.191+08:00","dg-note-properties":{}}
---


---

**API Levels** - internal number that identifies the Android Version.

> [!info] Google Answer
> An **API level** is an integer value that uniquely identifies the **framework API revision** offered by a version of the Android platform.

- It is very important since every API levels has **newer features/revisions** that is **not supported** on **older versions**.
- Every Android version release provides **newer API Levels** which offers newer API Features, **older features may be deprecated**.
- API Level is what **SDKs and Gradle Build relies on** when checking which **target Android version** is required.
	Example: If the `minSdkVersion` = 23 – the app is not supported on Android version 5.0 (API 21) and below.
* **Higher API Level** = Newer features on Android.