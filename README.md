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
