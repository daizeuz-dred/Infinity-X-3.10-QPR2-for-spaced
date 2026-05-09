# Infinity-X-3.10-QPR2-for-spaced




# 🚀 Release Changelog

---

### **📺 Display & UI (New Updates!)**
* **High Refresh Rate Native Support:** Set default and peak refresh rate to **120Hz** across the system.
* **Screen Recorder Pro:** Expanded screen recording options to include **90 FPS** and **120 FPS** for high-fidelity gameplay and UI captures.
* **SurfaceFlinger Tuning:**
    * Fine-tuned idle and touch timers for better responsiveness.
    * Configured frame rate multiple thresholds for **120Hz**.
    * Enabled **Client Composition Cache** to reduce GPU overhead.
    * Set `frame_rate_category_min` to **120** to force smoothness.
* **Brightness & Blacklist:** Removed brightness thresholds for high refresh rates and cleared the refresh rate blacklist to ensure 120Hz stays active in more apps.
* **Jank Reduction:** Disabled `latch_unsignaled` and cleaned up redundant idle timers to eliminate micro-stutters.

---

### **⚙️ System & Performance**
* **Java Optimizations:** Enabled `SYSTEM_OPTIMIZE_JAVA` and `SYSTEMUI_OPTIMIZE_JAVA` for faster app launches and smoother system navigation.
* **Uclamp Tuning:** Set `uclamp.min` to **350** for better UI boosting, ensuring the CPU stays at a higher frequency during touch interactions.
* **Resource Optimization:** Reworked `PowerHint` with policy-based nodes and tuned `schedutil` for more responsive CPU frequency scaling.
* **Memory Management:** Boosted **zRAM to 70%** of total RAM with **70 swappiness** and updated LMK for improved multitasking.

---

### **🛡️ Security, Stability & SEPolicy**
* **Wakeup Management:** Labeled `sysfs_wakeup` nodes and defined contexts for `/sys/class/wakeup` to allow the system to manage wakeup sources properly.
* **Suspend Fixes:** Granted `system_suspend` read permissions over `sysfs_wakeup` files to resolve battery-related denials and fix suspend issues.
* **Play Integrity:** ROM remains fully signed and passes all **3 Play Integrity checks** (Device Certified).
* **Build Stability:** Cleaned up duplicate declarations in `file.te`, `system_app.te`, and `device.mk` to resolve build failures and resource errors.

---

### **🏗️ Build System & Cleanups**
* **Resource Overlays:** Cleaned up duplicate 120Hz resource entries in `FrameworksResOverlay`.
* **Standardization:** Converted `rootdir` to **Blueprint** and renamed Lineage overlays for a cleaner build tree.
* **Legacy Removal:** Purged legacy MediaTek gauge, power properties, and tracing tools.

---

### **🔊 Connectivity & Audio**
* **NFC:** Upgraded to the modern **AIDL NXP NFC HAL** stack.
* **Audio Overhaul:** Integrated **Dolby Sony audio** for a premium sound experience.
* **Dolby Sony audio** for a premium sound experience.

* 
