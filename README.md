## OpenIPC for Smartwares CIP-37210   [![Telegram](https://openipc.org/images/telegram_button.svg)][telegram]
[Official vendor page](https://www.smartwares.eu/en-gb/smartwares-products/camera-systems/ip-cameras/smartwares-cip-37210-wi-fi-camera-indoor-cip--37210)

![cip-37210_0](https://user-images.githubusercontent.com/1933140/228334552-0f611eeb-6b24-4354-93e4-cfd9a63b9f36.jpg)

### Table of contents

1)  [Requirements](https://github.com/OpenIPC/device-cip-37210/blob/main/README.md#requirements)
2)  [Connecting USB-UART adapter](https://github.com/OpenIPC/device-cip-37210/blob/main/README.md#connecting-usb-uart-adapter)
3)  [Partitions](https://github.com/OpenIPC/device-cip-37210/blob/main/README.md#partitions)
4)  Backup factory firmware
5)  Flashing OpenIPC U-Boot
6)  Flashing OpenIPC kernel
7)  Flashing OpenIPC rootfs
8)  WiFi setup
9)  Settings
10)  Frequently asked questions
11) Rolling back to factory firmware from backup



### Requirements

1) WiFi IP Camera Smartwares CIP-37210 with SoC HiSilicon 3518EV200 version (not with SoC Ingenic T21). 
   At the moment there are known of the existence of three modifications of the camera with this name.

![05-req1](https://user-images.githubusercontent.com/1933140/228339564-a0bc325c-505c-4a7a-9940-fa5fa8cb78bf.png)

2) Phillips screwdriver

![screwdriver](https://user-images.githubusercontent.com/1933140/228342881-c68d8a80-a12d-49b6-bbca-eed6fcd0fd44.png)

3) USB-UART adapter and wires.

   Don't forget to select 3.3 volts jumper.

   We recommend this adapter:

![232](https://user-images.githubusercontent.com/1933140/228343595-83e54ffb-c27d-4c92-b165-d7f48b949a6d.png)


4) Working microSD card

![microsd](https://user-images.githubusercontent.com/1933140/228342958-e6d1cef9-28b7-4c08-b65a-cd5200992448.png)

6) Installed and prepared [OpenIPC BURN utility](https://github.com/OpenIPC/burn)

https://www.youtube.com/playlist?list=PLh0sgk8j8CfsMPq9OraSt5dobTIe8NXmw

### Connecting USB-UART adapter

Сonnect the USB-UART adapter to the camera according to the circuit diagram:

![07-USB-UART](https://user-images.githubusercontent.com/1933140/228344385-f16179a3-aabb-4d56-9070-aac4da2129b6.png)

### Partitions
CIP-37210 16mb SPI flash partitions table for OpenIPC
|  | Decimal size mega bytes | Decimal size kilo bytes | Decimal size  bytes | Hexadecimal size bytes | Hexadecimal start address | Hexadecimal end address |
| --- | --- | --- | --- | --- | --- | --- |
| U-Boot | 0,25 MB | 256 KB | 262144 bytes | 0x40000 | 0x0 | 0x3FFFF |
| U-boot environment | 0,0625 MB | 64 KB | 65536 bytes | 0x10000 | 0x40000 | 0x4FFFF |
| Kernel (uImage) | 2 MB | 2048 KB | 2097152 bytes | 0x200000 | 0x50000 | 0x24FFFF |
| Root file system | 5 MB | 5120 KB | 5242880 bytes | 0x500000 | 0x250000 | 0x74FFFF |
| Rootfs data (overlay) | 8,6875 MB | 8896 KB | 9109504 bytes | 0x8B0000 | 0x750000 | 0xFFFFFF |
| TOTAL | 16 MB | 16384 KB | 16777216 bytes | 0x1000000 |  |  |

U-Boot (short for Universal Bootloader) is an open-source boot loader software that is commonly used in embedded systems and devices.
It is responsible for initializing the hardware and starting the operating system on the device.

U-Boot environment (often referred to as "env") is a set of variables that are stored in non-volatile memory and used by U-Boot at boot time. These variables contain configuration information, such as the boot device, kernel parameters, and network settings.

The Linux kernel (uImage) is a compressed image of the Linux kernel that contains the necessary components to start the operating system.
 It includes the kernel code, device drivers, and other essential components. The uImage format includes a header that provides information about the kernel image, such as its size, load address, and entry point. It is used by U-Boot to load the kernel image into memory and start execution. The use of a compressed uImage helps to reduce the size of the kernel image, making it more suitable for embedded systems with limited storage capacity.

The root filesystem is the top-level directory of the filesystem. It must contain all of the files required to boot the Linux system before other filesystems are mounted. It must include all of the required executables and libraries required to boot the remaining filesystems.

Overlay is used to create a read-only root file system that can be overlaid with a read-write file system. This allows the system to boot from a read-only file system, which is more secure and reliable, while still allowing users to make changes and store data in a separate overlay file system.

### Backup factory firmware

More information about the [project][project] is available in our [website][website] and on the [wiki][wiki].

<p align="center">
<a href="https://opencollective.com/openipc/contribute/backer-14335/checkout" target="_blank"><img src="https://opencollective.com/webpack/donate/button@2x.png?color=blue" width="250" alt="Open Collective donate button"></a>
</p>

[firmware]: https://github.com/openipc/firmware/
[mit]: https://opensource.org/license/mit/
[opencollective]: https://opencollective.com/openipc
[paypal]: https://www.paypal.com/donate/?hosted_button_id=C6F7UJLA58MBS
[project]: https://github.com/openipc/
[telegram]: https://t.me/OpenIPC
[website]: https://openipc.org/
[wiki]: https://github.com/OpenIPC/wiki
