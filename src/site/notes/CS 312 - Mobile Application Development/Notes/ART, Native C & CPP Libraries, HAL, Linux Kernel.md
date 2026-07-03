---
{"dg-publish":true,"permalink":"/cs-312-mobile-application-development/notes/art-native-c-and-cpp-libraries-hal-linux-kernel/","created":"2026-07-03T17:19:26.163+08:00","updated":"2026-07-03T20:25:34.742+08:00","dg-note-properties":{}}
---


---

#### Android Runtime (ART)

> [!summary]
> - **Executes your app's code**; ART replaces **Dalvik VM** (predecessor).
> - Uses **ahead-of-time compilation** – **improves performance** and **battery life**.
>  - Developer Role: You don't code here directly, rather your Java/Kotlin code is **converted** into bytecode and run by ART.

**Android Runtime (ART) is the virtual machine that runs applications on Android**. In simple terms, ART is responsible for converting application source code into **executable code** capable of interacting with the device's hardware. It replaced Dalvik as the primary runtime environment and has continued to evolve in later versions of the operating system.

ART introduces the use of **ahead-of-time (AOT) compilation** by compiling the most performance-critical parts of applications (previously, the entire app) into native machine code upon their installation. This way, ART improves the **overall execution efficiency** and **reduces power consumption**, which results in improved battery autonomy on **mobile devices**. At the same time, ART brings faster execution of applications, improved **memory allocation** and **garbage collection** (GC) mechanisms, new applications debugging features, and more accurate high-level profiling of applications.

#### Native C & C++ Libraries

> [!summary]
> - Written in C/C++, these provide **low-level functionality** like graphics, databases, and web rendering.
> - Examples are **SQLite** (database), **OpenGL ES** (graphics), **Web Kit** (browser-engine).
> - Developer Role: You can tap into these using the NDK (Native Development Kit) if you need **high-performance code** (like for games).
> - Purpose: C++ is closer to the hardware than Java/Kotlin (relies on JVM); Existing C/C++ libraries that is **open-source proprietary** instead of making code again on Java/Kotlin, you can use **NDK** on Android.

#### Hardware Abstraction Layer (HAL)

> [!summary]
> - Acts as **translator** between Android and the Phone's hardware.
> - Examples include HAL module for **Camera**, **GPS**, **Bluetooth**, etc.
> - Developer Role: Normally you don't touch this but **hardware manufacturers** customize this layer for their devices.
> - Each manufacturers has their own design; If HAL doesn't exist, you'll have to code each phone models separately.
> - Provides a **standardized interface** that allows the Android framework to **communicate** with the underlying hardware **without needing to understand the specific details of that hardware**. So the developers won't have to worry about each phone models when developing.


A **hardware abstraction** is a **software layer** that provides access to hardware in a way that hides details that might otherwise make using the hardware difficult. Typically, access is provided via a **software interface** that allows devices that share a level of similarity to be accessed via the same software actions even though the devices provide different hardware interfaces. A hardware abstraction can support the development of **cross-platform applications**.

#### Linux Kernel

> [!summary]
> - The core of the system — **manages hardware** (CPU, Memory, Drivers, Security).
> - Developer Role: App developers doesn't modify the kernel – it is **maintained by device manufacturers and Google**.