# How to Install Google TV on a USB Drive

Simple step-by-step guide to make a portable Google TV on a USB stick.

You can plug this USB into almost any Windows computer and turn it into a smart TV.

---

## What You Need

- USB stick **16 GB or larger** (32 GB or 64 GB is better)
- Windows computer
- About 30–45 minutes

---

## 1. Download the Files

### Google TV Files
Download from any of these links:

- [Google Drive](https://drive.google.com/file/d/1yWCAlPuiiCordbkPEx9Uv7jplWPE3djh/view?usp=sharing)
- [Mega](https://mega.nz/file/PVp3RJKD#Lrx54cvoPsl195aAm6rdCq3sqZqgjQKKd_1kjFoAfLY)
- [MediaFire](https://www.mediafire.com/file/8t9wn2flf2imsj8/Google_TV_13_%252B_Data.zip/file)

After download:
1. Right-click the file → **Extract All**
2. You will see:
   - `GoogleTV13.iso`
   - **Storages** folder

### Rufus
Download here: [https://rufus.ie](https://rufus.ie)

### Optional Tools (for extracting files)
- [7-Zip](https://www.7-zip.org/)
- [WinRAR](https://www.win-rar.com/)

---

## 2. Make the USB Bootable

1. Plug in your USB stick
2. Open Rufus
3. Select your USB stick under **Device**
4. Click **SELECT** and choose `GoogleTV13.iso`
5. Drag the **Persistent partition size** slider all the way to the right
6. Partition scheme:
   - Choose **GPT** (for most modern PCs)
   - Choose **MBR** (only for very old PCs)
7. Click **START** and wait until it finishes

---

## 3. Unlock Full Storage

1. Open **Disk Management** (right-click Start → Disk Management)
2. Find your USB drive
3. Right-click the large partition → **Delete Volume**
4. Right-click the empty space → **New Simple Volume**
5. Format it as **exFAT** and finish the wizard

### Move system.sfs
1. Open the small boot partition on the USB
2. Cut the file named `system.sfs`
3. Paste it into the new exFAT partition

### Add Data File
1. Open the **Storages** folder
2. Choose the right size:

| Your USB Size | Use This File |
|---------------|---------------|
| 16 GB         | 8 GB          |
| 32 GB         | 16 GB         |
| 64 GB         | 32 GB         |

3. Copy that file into the exFAT partition

Done. Your Google TV USB is ready.

---

## 4. Boot from the USB (Windows 11)

### Method 1 – Easiest (Recommended)
1. Keep the USB plugged in
2. Hold the **Shift** key
3. Click **Start → Power → Restart**
4. On the blue screen choose **Use a device**
5. Select your USB drive

### Method 2 – From Settings
1. Open **Settings**
2. Go to **System → Recovery**
3. Under **Advanced startup** click **Restart now**
4. Choose **Troubleshoot → Advanced options → UEFI Firmware Settings → Restart**
5. In the firmware menu, look for Boot or Boot Override and select the USB

### Method 3 – Boot Menu during startup
1. Restart the computer
2. Immediately start tapping the Boot Menu key repeatedly (common keys: Esc, F12, F9, F10)
3. When the menu appears, select your USB drive and press Enter

---

## 5. First Time Setup

1. Choose language
2. Connect to Wi-Fi
3. Sign in with Google account (optional)
4. Finish the setup

You now have Google TV running from USB.

---

## Troubleshooting

| Problem              | Solution                                      |
|----------------------|-----------------------------------------------|
| USB not showing      | Try another USB port                          |
| Won’t boot           | Disable Secure Boot in BIOS                   |
| Black screen         | Try another option in the boot menu           |
| Limited storage      | Make sure you moved `system.sfs` correctly    |

---

## Useful Links

- [Google TV Files (Google Drive)](https://drive.google.com/file/d/1yWCAlPuiiCordbkPEx9Uv7jplWPE3djh/view?usp=sharing)
- [Google TV Files (Mega)](https://mega.nz/file/PVp3RJKD#Lrx54cvoPsl195aAm6rdCq3sqZqgjQKKd_1kjFoAfLY)
- [Google TV Files (MediaFire)](https://www.mediafire.com/file/8t9wn2flf2imsj8/Google_TV_13_%252B_Data.zip/file)
- [Rufus](https://rufus.ie)
- [7-Zip](https://www.7-zip.org/)
- [WinRAR](https://www.win-rar.com/)

---

**Tip:** Use a USB 3.0 stick or external SSD for better speed.

---

Made with ❤️ by [1048ae](https://github.com/1048ae67-sudo)
