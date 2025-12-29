BalloonPopup
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9-blue?logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![API](https://img.shields.io/badge/API-24%2B-orange)](#)
---

A lightweight, view-based Tooltip / Balloon Popup library for Android (Kotlin)

BalloonPopup is a simple, customizable, and view-based tooltip library built using PopupWindow.
It helps you show contextual hints, tips, or messages attached to any view — without Compose and without heavy dependencies.

### Features

- View-based (XML + Kotlin)
- Show tooltip TOP / BOTTOM / LEFT / RIGHT
- Auto-flip when there’s no screen space
- Custom background color
- Custom text color
- Arrow color automatically matches background
- Tap outside to dismiss
- X / Y offset support
- Clean, fluent Kotlin API
- Lightweight & library-friendly

### Preview

<p align="center">
<table>
  <tr>
    <td align="center">
      <img src="assets/image1.jpg" width="360" />
    </td>
    <td align="center">
      <img src="assets/image2.jpg" width="360" />
    </td>
  </tr>
</table>
</p>

---

## Installation (JitPack)

### 1️⃣ Add JitPack to your **root `settings.gradle` or `build.gradle`**

```gradle
dependencyResolutionManagement {
    repositories {
        google()
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```
### Add Dependency
```
dependencies {
	        implementation 'com.github.Excelsior-Technologies-Community:Android_BalloonPopup:1.0.0'
	}
```

---

### Basic Usage

```kotlin
BalloonPopup(this)
    .setText("Welcome to the app 🎉")
    .setTextColor(Color.WHITE)
    .setBackgroundColor(Color.parseColor("#03DAC5"))
    .setArrowPosition(ArrowPosition.BOTTOM)
    .setOffset(0, 8)
    .enableAutoFlip(true)
    .show(binding.btnStart)
```


### Example Usage

**XML**

```xml
<Button
        android:id="@+id/btnShowTooltip"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        android:text="Show Tooltip" />
```

**Kotlin**
```
binding.btnShowTooltip.setOnClickListener {
            BalloonPopup(this)
                .setText("Hello from Balloon Library 🎈")
                .setArrowPosition(ArrowPosition.BOTTOM)
                .setBackgroundColor(Color.parseColor("#6200EE"))
                .setTextColor(Color.YELLOW)
                .show(binding.btnShowTooltip)
        }
```

---

### License

```
MIT License

Copyright (c) 2025 Excelsior Technologies 

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
