Dell OptiPlex 3070 with i5-9600k on macOS Monterey 12.0
============================================



- Bootloader version: Opencore 0.7.1
- macOS version: macOS Monterey 12.1


![Oops!There was supposed to be an image here](https://i.imgur.com/jKUO4oY.png)

#### Hardware Specification
| Component | Specs |
|------------|----------------------------------------|
| **CPU**     | `Intel® Core™ i5-9100T` |   
| **RAM**     | `8gb DDR4 2400MHZ`|   
| **HDD**     | `SKHynix NVMe SSD 256GB`|
| **iGPU**    | `Intel® UHD Graphics 630`|
| **Audio**   | `RRealtek ALC3234`|
| **OS**      | `macOS Monterey 12.0 (21A5284e)`|
| **Boot**    | `OpenCore 0.7.1`|
| **WiFi/BT**    | `BCM943602CS /w adapter`|

#### Working: 

- Audio
- GPU 
- All USB Ports
- LAN
- Airdrop & Airplay
- Sleep
- Internal sound and hdmi
- DisplayPort monitor & HDMI monitor + wake/sleep

Not working: 
- WiFi has issues when enabled / make mouse sluggish

#### BIOS Settings

General → Advanced Boot Options: uncheck
System Configuration → SATA Operation: AHCI
Secure Boot → Secure Boot Enable: Disabled
Intel® Software Guard Extensions™ → Intel® SGX™ Enable: Disabled
Power Management → Block Sleep: check
Virtualization Support → VT for Direct I/O: uncheck

##### BIOS Settings via GRUB (Optional)
## BIOS Settings via GRUB (Optional) for dell OPTIPLEX 3070MFF

- Set Pre-Allocated DVMT to 64M: setup_var 0x8DC 0x02 
default was 0x01
- Disable CFG lock: setup_var 0x5BE 0x00 </br>
default was 0x01
