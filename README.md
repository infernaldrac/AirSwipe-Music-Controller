# 🎵 Gesture-Controlled Local Music Player

Control your **local music playback using hand gestures** — powered by **OpenCV**, **MediaPipe**, and **pygame**.  
Built with love and code by(https://github.com/infernaldrac) 💻🎧

---

## 🚀 Features
- ✊ **Fist → Toggle Play/Pause**  
- 👉 **Swipe Right → Next Track**  
- 👈 **Swipe Left → Previous Track**  
- ✌️ **Two Fingers Up → Volume Control** (vertical hand position maps to volume)  
- 🎥 Visual overlays:  
  - Hand landmarks  
  - Current gesture label  
  - Cooldown indicator  
  - Mini volume bar  
- ⚙️ Gesture smoothing + cooldown to prevent accidental re-triggers  
- 🎶 Local music playback using `pygame` (place songs in `local_music/`)

---

## ⚙️ Quick Setup

1. **Create a virtual environment and install dependencies:**
   ```powershell
   python -m venv venv; .\venv\Scripts\Activate.ps1
   pip install -r requirements.txt
   ```

2. **Add your music:**
   - Create a folder named `local_music` in the project root.  
   - Add `.mp3`, `.wav`, or `.ogg` files there.

3. **(Optional) System Volume Control — Windows Only**
   - `pycaw` (included in `requirements.txt`) lets you control the **Windows master volume** directly.  
   - Run the script with:
     ```powershell
     python gesture_spotify_player.py --system-volume
     ```
   - If not specified, volume gestures only affect the internal `pygame` playback volume.

4. **Run the player:**
   ```powershell
   python gesture_spotify_player.py
   ```

---

## 💡 Notes & Tips
- 🖐️ Run locally for **real-time webcam access** and **low-latency control** (Colab isn’t ideal for live gesture input).  
- 🎯 If gestures trigger too easily, adjust thresholds in `gesture_spotify_player.py` (gesture buffer sizes, swipe distances, cooldowns).  
- 🔊 For full system-wide volume on Windows, ensure `pycaw` is installed and use the `--system-volume` flag.

---

## 🧠 Colab Note
A notebook version — `gestures_spotify_colab.ipynb` — is included for quick demos.  
> ⚠️ Webcam performance in Colab is limited (higher latency).  
> For the best experience, use **local execution**.

---

## 👤 Author & Credits
**Project by:** (https://github.com/infernaldrac)

Show support by giving the project a ⭐.

---

## 📄 License
**MIT License** — open to use, modify, and share with proper credit.
