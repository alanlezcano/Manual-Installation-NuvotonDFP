# Manual Installation of `Nuvoton.NuMicro_DFP` Pack in Keil uVision
Manual integration of the Nuvoton NuMicro DFP (1.3.7) into Keil uVision for the NuMaker-PFM-M251SD board. Includes step-by-step setup instructions, pack files, and troubleshooting guide.

## Problem Summary

The Keil Pack Installer was unable to download and install the `Nuvoton.NuMicro_DFP.1.3.26.pack` automatically. It was stuck due to issues such as:

* "File in use" errors in `.Download` folders
* Keil not recognizing manually copied `.pack` files
* The Pack Installer not showing `NuMicro M251` or similar devices
* Folders being locked by `cpackget`

---
## Preparation for DFP download
We downloaded the MDK-ARM (MDK542A.EXE) from the [official website](https://www.keil.com/demo/eval/arm.htm)
The DFP will be downloaded in the files created by this installation process.
## Solution: Manual Pack Installation

### 1. **Download the `.pack` File**

We used version `1.3.7` from the [Packs Available in GitHub](https://github.com/OpenNuvoton/cmsis-packs/tree/master/Nuvoton_DFP)


```
Nuvoton.NuMicro_DFP.1.3.7.pack was used for improved stability, as newer versions are known to contain unresolved bugs.
```

---

### 2. **Create the Required Folder Structure**

Go to:

```
C:\Users\<YourUsername>\AppData\Local\Arm\Packs\Nuvoton\NuMicro_DFP\1.3.7
```

> Replace `<YourUsername>` with your actual Windows user name.

If these folders don't exist, create them manually.

---

### 3. **Rename the pack to a .zip file and Extract it**

Rename the file to a '.zip' format. Use 7-Zip or WinRAR to **extract** `Nuvoton.NuMicro_DFP.1.3.7.zip` into the `1.3.7` folder.

After extraction, the folder should contain:

```
- Device/
- Flash/
- SVD/
- Nuvoton.NuMicro_DFP.pdsc
- Nuvoton.NuMicro_DFP.1.3.7.zip
```

---

### 4. **Open Keil uVision**

Go to **New Project** and select the device.
In our case, the `NuMicro M251` series appeared successfully.

---

## Status: Working

The `Nuvoton.NuMicro_DFP` pack was successfully added and is usable within Keil uVision, allowing project creation and device selection.

---

## Tools Used

* Keil uVision5
* GitHub (Open-CMSIS-Pack repository)
* 7-Zip (for extraction)

---

## Troubleshooting Notes

* **Pack file locked**: Close any open Pack Installer windows before deleting `.pack` files or `.idx`.
* **Missing folders**: Some folders must be created manually.
* **Wrong extension**: If `.pack` opens weirdly, rename the extension to `.zip` temporarily to extract.

---
