# USBHostMSD

The USBHostMSD interface is used to access a USB mass storage device.

<span class="warnings">**Warning:** Library in beta</br>This library is in beta. If you have any problems using the USBHost library, please send a bug report to [support@mbed.org](support@mbed.org). </span>

The USB Host connector should be attached to:

* **p31 (D+), p32 (D-) and GND** for the **LPC1768**.
* Add **two 15k resistors tied to GND on D+ and D-**.

## Hello World

[![View code](https://www.mbed.com/embed/?url=https://developer.mbed.org/users/samux/code/USBHostMSD_HelloWorld/)](https://developer.mbed.org/users/samux/code/USBHostMSD_HelloWorld/file/tip/main.cpp) 

## API

[![View code](https://www.mbed.com/embed/?url=https://developer.mbed.org/users/mbed_official/code/USBHost/)](https://developer.mbed.org/users/mbed_official/code/USBHost/file/tip/main.cpp) 

## Troobleshooting
If your mbed board is automatically reset when you plug a USB device, you should consider using an external power supply.

