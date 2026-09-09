# Installing SimpleOS on Anbernic RG DS

SimpleOS does **not** replace the kernel and does **not** flash U-Boot.
It is an overlay on **official Anbernic Linux**. DraStic and Nintendo BIOS
files are not in this package: SimpleOS uses the copies already on the
firmware.

<p align="center">
  <img src="images/installing.png" alt="SimpleOS installing on the lid screen" width="480">
</p>
<p align="center">
  <img src="images/installing2.png" alt="SimpleOS installing on the touch screen" width="480">
</p>

## What you need

1. Official [**Anbernic Linux**](https://win.anbernic.com/download/640.html) for RG DS: .
2. The release zip `releases/SimpleOS-RGDS-YYYYMMDD.zip` from this repository.

## Install

1. Flash the SD card with Anbernic's Linux firmware
2. On a PC, open the **user partition** (next to `Roms/`, `anbernic/`, …).
3. Extract the **contents** of the zip into the **root** of that partition:

   ```
   simpleos/
   simpleos/install/
   .simpleos_update/
   Roms/APPS/Install SimpleOS.sh
   README.txt
   ```

   If Windows asks to merge `Roms/`, confirm. Do not leave everything inside a
   nested folder named `SimpleOS-RGDS-…`.
4. Eject the card, insert it in the RG DS, power on.
5. In the Anbernic menu: **APPS → Install SimpleOS**.
   SimpleOS splash screens appear on both displays. Do not power off.
6. When it finishes, the device reboots into SimpleOS
7. If the top screen doesn't come app: press **start → reboot**

Games go in `simpleos/games` and/or the stock NDS folder (`Roms/NDS`).

## Update

Replace `simpleos/` (or copy `system.zip` into `simpleos/`) and run
**Install SimpleOS** again. 

## Return to Anbernic Stock OS

Create the empty file `simpleos/userdata/boot_stock` and reboot.
Original logos are kept as `*.anbernic` next to the files SimpleOS replaced.

