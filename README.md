# Android Telemetry Pilot 🛰️📹

**Android Telemetry Pilot** is a high-performance Android application designed for real-time cellular telemetry monitoring, synchronized video recording, and low-latency network offloading. It serves as a mobile sensor hub for field testing and remote monitoring scenarios.

![Project Status](https://img.shields.io/badge/Status-Beta-orange)
![Platform](https://img.shields.io/badge/Platform-Android-green)
![API Level](https://img.shields.io/badge/API-29%2B-blue)

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
