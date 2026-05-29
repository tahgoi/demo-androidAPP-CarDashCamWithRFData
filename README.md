# CarDashCam with RF Data 🛰️📹

**Android Telemetry Pilot** is a high-performance Android application designed for real-time cellular telemetry monitoring, synchronized video recording, and low-latency network offloading. It serves as a mobile sensor hub for field testing and remote monitoring scenarios.

![Project Status](https://img.shields.io/badge/Status-Beta-orange)
![Platform](https://img.shields.io/badge/Platform-Android-green)
![API Level](https://img.shields.io/badge/API-29%2B-blue)


App is currently on Play Store undergoing testing, if intersted to download and participate onbeta testing, just send your email to android.xappslab@gmail.com - we'll send you a link to download from Play Store.

---

## 🚀 Key Features

- **Real-Time Telemetry HUD**: Monitor critical network metrics (5G NR/LTE), GPS coordinates, speed, and heading via a professional glassmorphic interface.
- **Integrated OpenStreetMap (OSM)**: Live map tracking using OpenStreetMap for offline-capable, high-detail navigation data.
- **On-Screen Display (OSD) Burn-in**: Automatically overlay telemetry data directly onto video frames before encoding, ensuring your data is permanently baked into the footage.
- **High-Performance Video Engine**: Records H.264/AVC video synchronized with telemetry logs.
- **Low-Latency Streaming**: Real-time JPEG-over-TCP offloading to companion receivers (e.g., MSI Claw, PC) for remote monitoring.
- **Local Persistence**: Integrated Room Database for logging every telemetry tick, searchable by linked video filename.
- **Modern UI/UX**: Dark-themed, neon-accented HUD designed for high visibility in field environments.

---

## 🛠️ Technical Stack

- **Language**: Kotlin 1.9.22
- **Camera Pipeline**: [CameraX](https://developer.android.com/training/camerax) (ImageAnalysis & Preview)
- **Database**: [Room](https://developer.android.com/training/data-storage/room)
- **Map Engine**: [osmdroid](https://github.com/osmdroid/osmdroid) for OpenStreetMap integration.
- **Location**: Google Play Services (Fused Location Provider)
- **Networking**: Raw Sockets (TCP) with custom frame headers
- **Architecture**: MVVM with Kotlin Coroutines and StateFlow
- **Encoder**: MediaCodec (Hardware-accelerated H.264)

---

## 📲 Installation & Demo

You can download the latest demo APK from the [Releases](https://github.com/tahgoi/android-telemetry-pilot/releases) section.

### Prerequisites
- Android 10 (API 29) or higher.
- Active SIM card for cellular telemetry.
- GPS enabled for location tracking.

### Permissions Required
- **Camera**: For viewfinder and video recording.
- **Location (Fine)**: For GPS tracking and cellular signal details (Android requirement).
- **Phone State**: For reading network technology (LTE/5G) and signal metrics.
- **Storage/Media**: For saving recordings and snapshots.

---

## 🖥️ Usage

1.  **Grant Permissions**: Accept all permission prompts on the first launch.
2.  **Mode Toggle**: Use the camera icon to switch between **Photo** (Snapshot) and **Video** (Recording) modes.
3.  **OSD Toggle**: Use the overlay icon to enable/disable the data burn-in on the video stream.
4.  **Network Stream**: Configure the **Target IP/Port** in Settings to stream live frames to a receiver.
5.  **Settings**: Access the gear icon to adjust logging preferences, receiver IP, and UI themes.

---

## 🛠️ Development Setup

1.  Clone the repository:
    ```bash
    git clone https://github.com/tahgoi/android-telemetry-pilot.git
    ```
2.  Open in **Android Studio (Ladybug or newer)**.
3.  Sync Gradle and build the project.
4.  Run on a physical device (Emulators do not support cellular telemetry).

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
*Developed for advanced telemetry field research.*

---

## 📸 Screenshots & Demo

### Video Demo

<video src="./screenshots/screenrecording_dashcam_lte_osd_drive.mp4" controls width="100%"></video>

### Screenshots

<p align="center">
  <img src="./screenshots/dashcam_mounted_lte_osd_video_mode.jpg" width="30%" title="Dashcam mounted on dash — LTE OSD video mode" />
  <img src="./screenshots/dashcam_landscape_lte_osd_highway_100kmh_minimap.jpg" width="30%" title="Landscape OSD burn-in — highway 100 km/h with minimap" />
  <img src="./screenshots/video_mode_portrait_lte_osd_indoor.jpg" width="30%" title="Portrait video mode — LTE OSD indoor" />
</p>
<p align="center">
  <img src="./screenshots/map_view_osm_5gnr_panel.jpg" width="30%" title="Map view (OSM) with 5G NR panel" />
  <img src="./screenshots/5gnr_monitor_lte_anchor_nr_secondary_cell.jpg" width="30%" title="5G NR Monitor — LTE anchor + NR secondary cell" />
  <img src="./screenshots/file_manager_telemetry_csv_mp4_recordings.jpg" width="30%" title="File manager — telemetry CSV and MP4 recordings" />
</p>
<p align="center">
  <img src="./screenshots/settings_sim_routing_offload_dark_theme.jpg" width="30%" title="Settings — SIM routing, wireless offload, dark theme" />
  <img src="./screenshots/settings_telemetry_logging_sim_video_1080p.png" width="30%" title="Settings — telemetry logging, SIM, video 1080p" />
  <img src="./screenshots/settings_video_30fps_1080p_logs_export.png" width="30%" title="Settings — video 30fps/1080p, logs export" />
</p>
<p align="center">
  <img src="./screenshots/about_technical_architecture.png" width="30%" title="About — technical architecture" />
</p>
