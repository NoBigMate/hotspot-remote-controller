# ⭐ **Project Title**

**Hotspot Remote Controller – Local Web-Based Android Screen Mirroring & Control (No Root)**

---

# 📌 **Short Description (GitHub tagline)**

A fully local and secure Android tool that hosts a private webpage over your phone’s hotspot, streams the device screen (MJPEG), and allows tap/swipe control through an AccessibilityService. No root, no internet, no external servers.

---

# 📖 **Long Description (GitHub README summary)**

**Hotspot Remote Controller** is an Android-based remote-control system that works **entirely offline**.
Your phone hosts a **local web server** bound to its hotspot IP (e.g., `192.168.43.1`), and when your laptop connects to the hotspot, you can open a private webpage such as:

```
http://192.168.43.1:8080/
```

This webpage shows your phone’s live screen (via MJPEG stream) and lets you interact with it through taps, swipes, and text input using an **AccessibilityService**.
Everything is executed **locally**, with zero cloud components.

---

# 🔐 **Key Features**

* 📴 **Works completely offline** — only over your phone’s hotspot
* 🔒 **Private by design** — no internet, no external servers
* 📱 **Live screen streaming** (MJPEG)
* 🖱️ **Remote control**: tap, swipe, and input actions via browser
* 🧩 **No root required**
* 🤝 **Simple lightweight built-in HTTP server**
* 🛠️ **Fully customizable** — edit the webpage/UI however you want

---

# 🛠️ **How It Works**

1. The app requests:

   * Screen capture permission (MediaProjection)
   * Accessibility control permission
2. It starts:

   * A screen-capture service
   * An embedded local HTTP server
3. Your laptop loads a webpage served from your phone
4. The page displays the MJPEG stream and sends control commands
5. The AccessibilityService executes gestures on the phone

---

# 📁 **Repository Structure**

```
app/
 └─ src/
     └─ main/
         ├─ AndroidManifest.xml
         ├─ java/com/example/hotspotremote/
         │   ├─ MainActivity.kt
         │   ├─ ScreenStreamer.kt
         │   ├─ WebServer.kt
         │   ├─ InputAccessibilityService.kt
         │   ├─ AccessibilityBridge.kt
         │   └─ WebAssets.kt
         └─ res/
             └─ xml/accessibility_service_config.xml
```

---

# 🚀 **Usage**

1. Build the APK in Android Studio
2. Install on phone
3. Connect your laptop to your phone’s hotspot
4. Open:

   ```
   http://192.168.43.1:8080/
   ```
5. View and control your phone directly in the browser

---

# ⚠️ **Security Notes**

* The server binds only to the hotspot interface
* No exposure to the public internet
* You may add a token/key in the webpage and server for extra protection

---

# 📌 **License**

MIT

