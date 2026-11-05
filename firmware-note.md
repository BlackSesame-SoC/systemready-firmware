# C1200 Firmware Flash

This guide describes how to flash C1200 firmware and install a Linux distribution on the C1200 CDCU.

## Flash the Firmware

1. Obtain the software version and flashing tools from the BlackSesame version URL. Contact the BlackSesame team to obtain them.

   Example:

   ![BlackSesame version download page](pic/00.jpg)

2. Open the flashing tool.

   ![BST flashing tool](pic/01.jpeg)

3. Configure the flashing tool:

   - Select the version archive.
   - Select C1296.
   - Select CDCU1.0.
   - Select the ADAS_DB template.
   - Select Type-C.
   - Select chD.
   - Check uboot, and replace it with the U-Boot build that supports UEFI.

4. Start flashing.

## Install the Distribution

1. Write the distribution ISO to an SD card using dd, then insert the SD card into the C1200 CDCU.
2. Power on
3. U-Boot scans the ESP partition and launches the corresponding installer. If automatic scanning does not occur, manually configure bootcmd to execute bootflow scan -lb.
4. Install the distribution.
5. Reboot the target.
