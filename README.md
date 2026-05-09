# Infinity-X-3.10-QPR2-for-Realme-8i-Narzo-50-spaced

## 📺 Display & UI (New & Improved!)
* **High Refresh Rate Native Support:** Set default and peak refresh rate to **120Hz** across the system.
* **Screen Recorder Pro:** Expanded options to include **90 FPS** and **120 FPS** for high-fidelity gameplay and UI captures.
* **SurfaceFlinger Tuning:**
    * Fine-tuned idle and touch timers for better responsiveness.
    * Configured frame rate multiple thresholds for **120Hz**.
    * Enabled **Client Composition Cache** to reduce GPU overhead.
    * Set `frame_rate_category_min` to **120** to force smoothness.
    * Enhanced smoothness by moving to **4 buffers** and adopting Motorola phase offsets.
* **Jank Reduction:** Optimized the link between SurfaceFlinger and the MTK display driver; disabled `latch_unsignaled` and cleaned up redundant idle timers to eliminate micro-stutters.
* **Visuals & Refinement:** Removed brightness thresholds for high refresh rates, cleared the refresh rate blacklist, added rounded corner support, and adjusted status bar padding.
* **Animations:** Switched to **linear interpolators** for consistent motion and simplified transitions.

## 🛠️ System & Performance
* **Resource Optimization:** Reworked `PowerHint` with policy-based nodes and tuned `schedutil` for more responsive CPU frequency scaling.
* **Java Optimizations:** Enabled `SYSTEM_OPTIMIZE_JAVA` and `SYSTEMUI_OPTIMIZE_JAVA` for faster app launches and smoother system navigation.
* **Uclamp Tuning:** Set `uclamp.min` to **350** for better UI boosting, ensuring the CPU stays at a higher frequency during touch interactions.
* **Memory Management:** Boosted **zRAM to 70%** of total RAM with **70 swappiness**, disabled writeback, and updated LMK for improved multitasking.
* **GPU Boost:** Patched **MediaTek GED** permissions to allow `gpu_boost_level 100` during high-load tasks, ensuring zero dropped frames.

## 🛡️ Security, Stability & OTA
* **Certification:** ROM is now **fully signed** and passes all **3 Play Integrity checks** (Device Certified).
* **Updates:** Integrated **OTA Update** support for seamless future releases.
* **SEPolicy & Wakeup:** Labeled `sysfs_wakeup` nodes and defined contexts for `/sys/class/wakeup`; granted `system_suspend` read permissions to fix battery/suspend related denials.
* **Security Fixes:** Disabled Factory Reset Protection (FRP) and authored custom vendor rules to resolve `sysfs_ged` permission denials.
* **Thermal Tuning:** Adjusted thresholds to prevent aggressive throttling during sustained high-performance encoding.

## 🔊 Connectivity & Audio
* **NFC:** Upgraded to the modern **AIDL NXP NFC HAL** stack.
* **Audio Overhaul:** Integrated **Dolby Sony audio** for a premium sound experience.
* **Streamlining:** Stripped unused codecs, disabled PCM dumping, and removed MTK encoder performance hints.

## 🏗️ Build System & Fixes
* **Standardization:** Converted `rootdir` to **Blueprint**, renamed Lineage overlays, and removed duplicate configs.
* **Bug Fixes:** Resolved duplicate 120Hz resource entries in `FrameworksResOverlay`, corrected permission errors for `opluserserve1`, and fixed "Permission Denied" issues for kernel performance nodes.
* **Cleanup:** Purged legacy MediaTek gauge, power properties, tracing tools, and compat namespaces.

---

## 🚀 HUGE THANKS TO @HELLINFIX FOR THE TREES AND ALL THE HELP 🫡
## 🤝 Thanks to @hxfuxyy for teaching me how to implement OTA updates
## 🎵 Thanks to @ViaanLarryROMS for the assistance in adding Sony Dolby
