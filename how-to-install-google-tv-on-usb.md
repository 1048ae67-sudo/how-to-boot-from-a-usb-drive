# How to Install Google TV on a USB Drive

A clean, step-by-step guide to create a **portable Google TV** on a USB stick and boot it on any Windows PC or laptop (including ASUS).

This turns any computer into a smart TV with the full Google TV interface, Play Store, YouTube, Netflix, and more — all from a USB drive.

**Based on:** Techy Druid method  
**Official written guide:** [techydruid.com/google-tv-usb](https://techydruid.com/google-tv-usb/)

---

## What You’ll Need

- USB stick **16 GB or larger** (32 GB or 64 GB recommended for better app storage)
- USB 3.0 drive or external SSD preferred for better speed
- Windows computer
- About 30–45 minutes

---

## 1. Download the Required Files

### Google TV 13 Package (ISO + Storage files)
Download from one of these links (same files):

- **Google Drive:** [Download here](https://drive.google.com/file/d/1yWCAlPuiiCordbkPEx9Uv7jplWPE3djh/view?usp=sharing)
- Alternative (Mega): [Download here](https://mega.nz/file/PVp3RJKD#Lrx54cvoPsl195aAm6rdCq3sqZqgjQKKd_1kjFoAfLY)
- Alternative (MediaFire): [Download here](https://www.mediafire.com/file/8t9wn2flf2imsj8/Google_TV_13_%252B_Data.zip/file)

After downloading:
1. Right-click the archive → **Extract All** (or use 7-Zip / WinRAR)
2. Inside you will find:
   - `GoogleTV13.iso` (the main system image)
   - **Storages** folder (contains data files: 4GB / 8GB / 16GB / 32GB / 64GB)

### Rufus (Recommended Tool)
Download from the official site:

**[Download Rufus](https://rufus.ie/)**

---

## 2. Create the Bootable USB with Rufus

1. Plug in your USB stick.
2. Open Rufus.
3. In Rufus:
   - **Device** → Select your USB stick (double-check the size!)
   - Click **SELECT** and choose the `GoogleTV13.iso` file
   - **Persistent partition size** → Drag the slider **all the way to the right** (maximum)
   - **Partition scheme**:
     - Choose **GPT** if your PC is modern (Windows 10/11, UEFI)
     - Choose **MBR** if it is an older BIOS-only system
   - File system stays **FAT32**
4. Click **START**.
5. Confirm that all data on the USB will be erased.
6. Wait until Rufus finishes (usually 5–10 minutes).

---

## 3. Unlock Full Storage (Very Important)

By default the system is limited. Follow these steps carefully:

1. Open **Disk Management** (right-click Start → Disk Management).
2. Find your USB drive.
3. You will see a small boot partition and a larger persistence partition.
4. Right-click the **persistence / large partition** → **Delete Volume**.
5. Right-click the now **Unallocated** space → **New Simple Volume**.
6. Follow the wizard:
   - Use the maximum available size
   - Format as **exFAT**
   - Give it a name if you want (example: SYSTEM)
7. Finish the wizard.

### Move the System File

1. Open the **Boot partition** of the USB (the small one).
2. Find the file named **`system.sfs`**.
3. **Cut** this file (Ctrl + X).
4. Paste it into the new **exFAT partition** you just created.

### Add the Data Storage File

1. Go to the **Storages** folder you extracted earlier.
2. Choose the correct data file according to your USB size:

| USB Size | Recommended Data File |
|----------|-----------------------|
| 16 GB    | 8 GB                  |
| 32 GB    | 16 GB                 |
| 64 GB    | 32 GB                 |

**Important rule:** Never choose a data file equal to the full size of your USB. Always leave some free space.

3. Copy the chosen data file into the **exFAT partition** of the USB.

Your Google TV USB is now ready.

---

## 4. Boot from the USB

### Easiest Method (Windows 11)

1. Keep the USB plugged in.
2. Click **Start**.
3. Hold the **Shift** key.
4. While holding Shift, click **Power → Restart**.
5. On the blue screen choose **Use a device** → select your USB.

### Alternative: Boot Menu

1. Shut down the computer completely.
2. Plug in the Google TV USB.
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

## 5. First Launch of Google TV

1. The system will start loading.
2. Choose your language.
3. Connect to Wi-Fi (or use Ethernet if Wi-Fi does not work).
4. Sign in with your Google account (optional but recommended for Play Store).
5. Complete the setup.

You now have a fully working portable Google TV!

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| USB not detected | Try a different USB port (preferably USB 3.0) or enable “List USB Hard Drives” in Rufus |
| Won’t boot | Disable Secure Boot and Fast Boot in BIOS |
| Black screen | Try a different kernel option from the boot menu |
| Limited storage | Make sure you moved `system.sfs` and added the correct data file |
| Apps not installing | Check that you used the correct data.img size for your USB |

---

## Useful Links

- [Full written guide by Techy Druid](https://techydruid.com/google-tv-usb/)
- [Original YouTube video](https://youtu.be/0DeYfTwZAgo)
- [Rufus official site](https://rufus.ie/)

---

**Tip:** For the best experience, use a fast USB 3.0 drive or an external SSD. The system will feel much smoother.

---

Made with ❤️ by [1048ae](https://github.com/1048ae67-sudo)
