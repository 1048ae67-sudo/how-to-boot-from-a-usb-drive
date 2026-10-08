# How to Boot Kali Linux from a USB Drive

A clean, step-by-step guide to create a **Kali Linux** live USB and boot it on Windows (including ASUS laptops).

**Official site:** [kali.org](https://www.kali.org)  
**Recommended image:** Kali Linux Live (AMD64)

---

## What You’ll Need

- USB stick **8 GB or larger** (16 GB+ recommended; everything on it will be erased)
- Windows computer
- About 30–60 minutes

---

## 1. Download the Required Files

### Kali Linux Live Image
Download the official Live ISO from the official page only:

**[Official Kali Linux Downloads](https://www.kali.org/get-kali/)**  
Choose the **Live** image for AMD64 (64-bit).

Always verify the SHA256 checksum after downloading.

### Rufus (Recommended Tool)
Download the portable version from the official site:

**[Download Rufus](https://rufus.ie/)**

---

## 2. Write Kali Linux to the USB Stick

1. Plug in your USB stick.
2. Run Rufus (as Administrator if needed).
3. In Rufus:
   - **Device** → Select your USB stick (double-check the size!)
   - Click **SELECT** and choose the Kali Linux `.iso` file
   - Leave Partition scheme and Target system at the defaults (usually GPT / UEFI)
   - Click **START**
4. If prompted about **ISOHybrid image**, select **DD Image** mode (recommended by Kali for best compatibility).
5. Wait until the process finishes, then close Rufus.

Your Kali Linux USB is now ready.

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
2. Plug in the Kali USB.
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

## 5. First Launch of Kali Linux

1. You will see the Kali Linux boot menu.
2. Select **Live system** (or the default option) and press Enter.
3. Wait for the desktop to load.
4. Default username: `kali`  
   Default password: `kali`

You’re in!

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| USB not detected | Try a different USB port (preferably USB 2.0) |
| Won’t boot | Disable Secure Boot / Fast Boot in BIOS |
| Black screen or hangs | Try the “Failsafe” or “Forensic mode” options in the boot menu |
| Still stuck | Check that you used the Live ISO and DD mode in Rufus |

---

## Useful Links

- [Official Kali Downloads](https://www.kali.org/get-kali/)
- [Making a Kali Bootable USB Drive (Windows)](https://www.kali.org/docs/usb/live-usb-install-with-windows/)
- [Kali Linux Documentation](https://www.kali.org/docs/)
- [Rufus Website](https://rufus.ie/)

---

**Tip:** After you are comfortable, you can add **persistence** so files and settings are saved between sessions. See the official Kali documentation for the recommended method.

---

Made with ❤️ by [1048ae](https://github.com/1048ae67-sudo)
