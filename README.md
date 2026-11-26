# SignalSpeak — ESP32-CAM Traffic Light Voice Assistant

- `www/index.html` — the whole web app (ESP32-CAM, phone camera, photo upload, voice alerts)
- `esp32-cam/esp32-cam.ino` — firmware for AI Thinker ESP32-CAM (stream on port 81 `/stream`, CORS enabled)
- `.github/workflows/build-apk.yml` — builds the Android APK on GitHub

## Get the APK
1. Upload all of these files to your GitHub repo (keep the folder structure).
2. Open the repo -> Actions -> "Build Android APK" -> Run workflow (it also runs on every push to main).
3. When it turns green, open the run -> Artifacts -> download `SignalSpeak-apk`, unzip, install `app-debug.apk` on your phone (allow "install unknown apps").

## Use it
Flash `esp32-cam.ino` (put your Wi-Fi name/password), open Serial Monitor at 115200, copy the IP it prints, enter it in the app and press Connect Camera. Phone and ESP32-CAM must be on the same Wi-Fi.
