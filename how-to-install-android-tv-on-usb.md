# How to Install Android TV on a USB Drive

A clean, step-by-step guide to make a portable Android TV on a USB stick.

You can plug this USB into almost any Windows computer and turn it into a smart TV.

---

## What You’ll Need

- USB stick **8 GB or larger** (16 GB or 32 GB USB 3.0 is better)
- Windows computer
- About 20–30 minutes

---

## 1. Download the Required Files

### Android TV ISO
Download the Android TV ISO from a Google Drive link (search for “Android TV USB ISO” or use a trusted source that provides the image file).

> The Google Drive link can sometimes show “too many users” error. Wait a few hours and try again if that happens.

### Rufus
Download here: [https://rufus.ie](https://rufus.ie)

### Optional Tools
- [7-Zip](https://www.7-zip.org/)
- [WinRAR](https://www.win-rar.com/)

---

## 2. Write Android TV to the USB Stick

1. Plug in your USB stick.
2. Open Rufus.
3. Under **Device**, select your USB stick (double-check!).
4. Click **SELECT** and choose the Android TV ISO file you downloaded.
5. Set **File system** to **FAT32**.
6. Leave other settings at default.
7. Click **START** and wait until it finishes.
8. Close Rufus and safely eject the USB.

Your Android TV USB is now almost ready.

---

## 3. Extract the Extra Storage File (Very Important)

1. Plug the USB back into the computer.
2. Open the USB drive in File Explorer.
3. Look for a file named **data4GB**, **data4GB.zip**, or **data4GB.rar**.
4. Right-click it → **Extract here** (using 7-Zip or WinRAR).
5. You should now see a file called **data.img** on the USB.
6. Do **not** move this file – leave it in the same place.
7. Safely eject the USB.

This `data.img` file gives Android TV extra storage for apps and settings. Skipping this step will leave you with very little space.

---

## 4. Boot from the USB

### Method 1 – Easiest (Recommended)
1. Keep the USB plugged in.
2. Hold the **Shift** key.
3. Click **Start → Power → Restart**.
4. On the blue screen choose **Use a device**.
5. Select your USB drive.

### Method 2 – From Settings
1. Open **Settings**.
2. Go to **System → Recovery**.
3. Under **Advanced startup** click **Restart now**.
4. Choose **Troubleshoot → Advanced options → UEFI Firmware Settings → Restart**.
5. In the firmware menu, look for Boot or Boot Override and select the USB.

### Method 3 – Boot Menu during startup
1. Restart the computer.
2. Immediately start tapping the Boot Menu key repeatedly.

**Common keys:**

| Brand / Situation | Key |
|-------------------|-----|
| Most laptops      | `Esc`, `F12`, `F9` |
| ASUS              | `Esc` or `F8` |
| Dell              | `F12` |
| HP                | `Esc` or `F9` |
| Lenovo            | `F12` or `Fn + F12` |

Select the USB drive and press Enter.

### Method 4 – Desktop Shortcut to UEFI/BIOS (Very Useful)
This is the fastest way to open the BIOS/UEFI settings on your ASUS Windows 11 laptop.

1. Right-click an empty area on the desktop.
2. Select **New → Shortcut**.
3. Paste this command:

```
shutdown /r /fw /t 0
```

4. Name it **Restart to UEFI/BIOS** and finish.
5. Double-click it (save your work first – it restarts immediately).

---

## 5. First Time Setup

1. Choose your language.
2. Connect to the internet:
   - Use Wi-Fi if available.
   - If Wi-Fi does not work, plug in an Ethernet cable (it may appear as **VirtualWiFi**).
3. When you see the Android TV selection screen, select it and press **Esc** on the keyboard if needed.
4. Finish the setup and sign in with Google account (optional).

You now have Android TV running from USB.

---

## Tips

- Use a **USB 3.0** stick for better speed.
- Connect the laptop to your TV with an **HDMI cable** to use it as a living-room Android TV.
- Your normal Windows system stays completely untouched.
- To go back to Windows just remove the USB and restart.

---

## Troubleshooting

| Problem              | Solution                                      |
|----------------------|-----------------------------------------------|
| USB not showing      | Try another USB port                          |
| Won’t boot           | Disable Secure Boot in BIOS                   |
| Limited storage      | Make sure you extracted `data4GB` correctly   |
| Google Drive error   | Wait and try the link again later             |
| Wi-Fi not working    | Use Ethernet cable instead                    |

---

## Useful Links

- [Rufus](https://rufus.ie)
- [7-Zip](https://www.7-zip.org/)
- [WinRAR](https://www.win-rar.com/)

---

**Tip:** Use a USB 3.0 stick or external SSD for better speed.

---

Made with ❤️ by [1048ae](https://github.com/1048ae67-sudo)
