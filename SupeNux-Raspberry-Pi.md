## Welcome
Welcome to the page to get your SupeNux Raspberry Pi .img file which has SupeNux, initialized by [Buildroot](https://buildroot.org) on Ubuntu. NOTE: When using this .img file, DO NOT forget to follow the SupeNux license. Click [here](https://github.com/gautamritvik/SupeNux/blob/main/LICENSE) for the SupeNux license.

## Requirements
- Physical SD card with 200 MB or more
- Raspberry Pi with SD card port (Raspberry Pi Keyboard will **NOT** work as it is a ***accessory*** for the Raspberry Pi, not a computing module.)
- Computer
- Computer's local terminal

Note: When you open the link below, it will say "No preview available", but when you see the option, click the button "Download" to get the .img file onto your computer. If you get redirected to another link saying:

"**Google Drive has detected issues with your download**
This file is too large for Google to scan for viruses.
This file is executable and may harm your computer.",

then click the button "Donwload anyway" to download the .img file.

## Download the file
Download the SupeNux Raspberry Pi .img file here ---> [sdcard.img](https://drive.google.com/file/d/1QG-6paf5dZjqHqqXwQn9VCwDCkgv88fk/view?usp=drive_link)


Now that you've installed the .img file above, now follow the steps below to get the file onto a physical SD card.
## Steps to flash the .img file onto a physical SD card
1. Insert the physical SD card you want to flash the .img file onto. Typically, older computers have built-in ports for SD cards, but if you're computer is newer, it may not have a SD card port, and you may need to get some type of adapter or something else to get your computer to read the SD card.
2. Now, follow the steps below based on your OS.
   - If you're on Linux/MacOS, follow the steps below:
     - Step 1: Identify your SD card after it's inserted into your computer with: `lsblk`
     - Step 2: Unmount the SD card to unmount any partitions it may have with: `sudo umount /dev/sdcard` (Replace "`/dev/sdcard`" with the identified path to your SD card from the command `lsblk`.)
     - Step 3: Write the .img file to the identified SD card path with: `sudo dd if=/path/to/image.img of=/dev/sdcard bs=4M status=progress` (Replace "`path/to/image.img`" with the path where the sdcard.img file from here is stored on your computer, and replace "`/dev/sdcard`" with the identified path to your SD card from the command `lsblk`.)
     - Step 4: Sync all the data to make sure that the data is written with: `sync` (Even though you think that the data is already successfully flashed onto the inserted physical SD card, it is still **HIGHLY** recommended so there are no problems. If problems ever occur though, just run `sudo fsck /dev/sdcard`, and don't forget to replace "`/dev/sdcard`" with the identified path to your SD card from the command `lsblk`.)
     - Step 5: Now that the .img file is successfully flashed onto the inserted physical SD card, you can safely eject it with: `sudo eject /dev/sdcard`, and remove the SD card from your computer (Replace "`/dev/sdcard`" with the identified path to your SD card from the command `lsblk`.)
   - If you're on Windows, follow the steps below:
     - Step 1: Download the Win32 Disk Imager if you haven't already by clicking [here](https://win32diskimager.b-cdn.net/win32diskimager-1.0.0-install.exe).
     - Step 2: Open the program.
     - Step 3: When open, select the .img file getting flashed onto the inserted physical SD card and select the inserted physical SD card you want your .img file to get flashed onto in the Win32 Disk Imager window.
     - Step 4: Start the writing process by clicking "Write".
     - Step 5: After the writing process is done, safely eject the SD card and remove the SD card from your computer.
3. Now that the .img file from here is successfully flashed onto the physical SD card, follow the steps below.
   - Step 1: Take the actual SD card out of the MicroSD adapter
   - Step 2: Flip your Raspberry Pi over onto it's top **gently**.
   - Step 3: Put the SD card into the SD card port.
   - Step 4: Flip the Raspberry Pi back to it's original position **gently**.
   - Step 5: Plug in the Raspberry Pi power.
   - Step 6: Plug in a keyboard.
   - Step 7: Plug in one side of a HDMI cable into the HDMI port on the Raspberry Pi and plug in the other side of the HDMI cable into the HDMI port on a monitor.
   - Step 8: Turn on the monitor.
   - Step 9: Do the following steps shown on the monitor the Raspberry Pi shows (It will most likely show a set of prompts to **create** an account, but if it doesn't, try to use "root" as the username and press Enter on your keyboard for the password.)
   - Step 10: Once you see "#" with your text cursor next to it, you've successfully logged in! You are currently using the bash terminal.
