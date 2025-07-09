# RPi-Zero-2-W-MJPEG-Streaming
<p align="center">
  <a href="https://drive.google.com/file/d/1SxrGfRK0qoJIxdzjj4nxNYeZHwk9vhIf/view?usp=drive_link" target="_blank">
    <img src="https://github.com/user-attachments/assets/bc06ccbf-f706-4a6c-9505-558e665a4825" width="600"/>
  </a>
</p>

One of the primary module from our capstone project "IoT-Based Smart Traffic Monitoring System with Data Analytics"

This project enables real-time video streaming from a Raspberry Pi Zero 2 W using a CSI camera module. 
It captures frames using the `picamera2` library, compresses them as JPEG images using `Pillow`, and streams them over HTTP using `aiohttp` in a lightweight MJPEG format.

> This project provides a practical alternative for low-latency video streaming suitable for local AI processing and web interfaces.

---

🧩 Components
<p align="center">
  <img src="https://github.com/user-attachments/assets/c65a0670-3c8a-4574-bce9-4773cea8a364" width="600"/>
</p>

- Raspberry Pi Zero 2 W booted with 32-bit Lite OS
- CSI Camera Rev 1.3 | 5 mp
- Laptop

---

🚀 Features

- 📷 Live video capture using CSI camera
- 🧠 Low-latency JPEG encoding (no OpenCV required)
- 🌐 MJPEG streaming over HTTP (viewable in Firefox, OpenCV, or `<img>` tag)
- 🧩 Easy to integrate with AI pipelines (OpenCV-ready)
- 🧵 Lightweight: no `av`, `opencv-python`, or `ffmpeg` required

---

🧰 Dependencies

Installed using `apt` (no pip builds required):

```bash
sudo apt update
sudo apt install -y \
  python3-picamera2 \
  python3-pil \
  python3-aiohttp \
  libcamera-apps
```

---

## 🖥️ How to Run

1. Connect your CSI camera to the Pi and enable camera support.

2. From your Local Clone this repo:
```bash
git clone https://github.com/BenjiBenji20/RPi-Zero-2-W-MJPEG-Streaming.git
cd RPi-Zero-2-W-MJPEG-Streaming
```
Note: Install the dependencies in requirement.txt, required for object detection

3. In your Pi, run the streaming server:
```bash
python3 stream.py
```

4. Open the stream from another device:
```bash
http://<raspberry-pi-ip>:8080/video
```
Note: You can view the livestream using Web chrome by running view-livestream.html or run object detection using yolo by running local/yolo-livestream.py

## 📦 Sample Use Cases
Local AI inference (via OpenCV)

Home Surveillance Camera 

Educational demo for low-level streaming
