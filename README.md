# homeAssistant-container
Home assistant container setup using zigbee passthrough

lsusb
Bus 001 Device 006: ID 1a86:55d4 QinHeng Electronics SONOFF Zigbee 3.0 USB Dongle Plus V2

l /dev/serial/by-id/
lrwxrwxrwx 1 root root 13 Nov  9 12:16 usb-ITEAD_SONOFF_Zigbee_3.0_USB_Dongle_Plus_V2_20230803101958-if00 -> ../../ttyACM0
lrwxrwxrwx 1 root root 13 Sep 26 11:36 usb-Prolific_Technology_Inc._USB-Serial_Controller_D-if00-port0 -> ../../ttyUSB1
lrwxrwxrwx 1 root root 13 Sep 26 11:34 usb-Prolific_Technology_Inc._USB-Serial_Controller_DXABb11BS14-if00-port0 -> ../../ttyUSB0

see compose file - devices

add the following

  volumes:
      - /dev/ttyACM0:/dev/ttyACM0
    devices:
      - /dev/ttyACM0:/dev/ttyACM0


Lumi weather (no display) range test - 1 press; connect -hold 5s


