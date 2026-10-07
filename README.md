# How to Boot from a USB Drive

A clean, step-by-step guide to create a **Tails** live USB and boot it on Windows (including ASUS laptops).

**Official site:** [tails.net](https://tails.net)  
**Current version used in this guide:** Tails 7.14

---

## What You’ll Need

- USB stick **8 GB or larger** (everything on it will be erased)
- Windows computer
- About 30–60 minutes

---

## 1. Download the Required Files

### Tails Image
Download the official `.img` file:

**[Download Tails 7.14 (AMD64)](https://download.tails.net/tails/stable/tails-amd64-7.14/tails-amd64-7.14.img)**  
(~1.8 GB)

### Rufus (Recommended Tool)
Download the portable version recommended by Tails:

**[Download Rufus Portable](https://tails.net/rufus/rufus-portable.exe)**

---

## 2. Write Tails to the USB Stick

1. Plug in your USB stick.
2. Run `rufus-portable.exe`.
3. In Rufus:
   - **Device** → Select your USB stick (double-check!)
   - Click **Select** and choose the `tails-amd64-7.14.img` file
   - Click **Start**
4. Wait until the process finishes, then close Rufus.

Your Tails USB is now ready.

---

## 3. Boot from the USB

### Easiest Method (Windows 11)

1. Keep the USB plugged in.
2. Click **Start**.
3. Hold the **Shift** key.
4. While holding Shift, click **Power → Restart**.
5. On the blue screen choose **Use a device** → select your USB.

### Alternative: Boot Menu

1. Shut down the computer completely.
2. Plug in the Tails USB.
3. Turn the computer on and repeatedly press the **Boot Menu** key.

**Common keys:**

| Brand / Situation | Key |
|-------------------|-----|
| Most laptops      | `Esc`, `F12`, `F9` |
| ASUS              | `Esc` or `F8` |
| Dell              | `F12` |
| HP                | `Esc` or `F9` |
| Lenovo            | `F12` or `Fn + F12` |

Select the USB drive and press Enter.

---

## 4. Enter BIOS / UEFI (if needed)

You may need to disable **Secure Boot** or **Fast Boot**.

### Fastest way – Restart to BIOS shortcut

1. Right-click desktop → **New → Shortcut**
2. Paste this command:

```
shutdown /r /fw /t 0
```

3. Name it **Restart to BIOS** and finish.
4. Double-click it (save your work first – it restarts immediately).

### Other ways

- **Settings path:** Settings → System → Recovery → Advanced startup → Restart now → Troubleshoot → Advanced options → UEFI Firmware Settings
- **Shift + Restart** method (same as above)
- Press `F2`, `Delete`, `Esc` or `F10` repeatedly while the computer is starting

---

## 5. First Launch of Tails

1. You will see the **Tails Boot Loader**.
2. Then the **Welcome Screen** appears.
3. Choose your language and keyboard layout.
4. Click **Start Tails**.

You’re in!

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| USB not detected | Try a different USB port (preferably USB 2.0) |
| Won’t boot | Disable Secure Boot / Fast Boot in BIOS |
| Wrong file used | Make sure you used the `.img` file, not `.iso` |
| Still stuck | Choose **Troubleshooting Mode** in the Tails Boot Loader |

---

## Useful Links

- [Official Tails Download](https://tails.net/install/download/)
- [Windows Installation Guide](https://tails.net/install/windows/)
- [How to Start Tails on PC](https://tails.net/doc/first_steps/start/pc/)
- [Rufus Website](https://rufus.ie/)

---

**Tip:** After you are comfortable, set up **Persistent Storage** inside Tails if you want to keep files and settings between sessions.

---

Made with ❤️ by [1048ae](https://github.com/1048ae67-sudo)
