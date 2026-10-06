# Setting up a Field Radio

## Required Hardware

- Robot Radio
- [Vivid-Hosting PoE wall adapter](https://wcproducts.com/products/frc-radio) (must be Vivid-Hosting brand) **OR** 12V DC power supply connected to the Weidmuller on the robot radio.
- Ethernet cables
- Heatsink for the radio. The radio will overheat without one. You can buy a heatsink from [WestCoast Products](https://wcproducts.com/products/frc-radio) or make your own. A fan is recommended, but not required.

## Steps

1. Download the [AP firmware](https://frc-radio.vivid-hosting.net/access-points/fms-ap-firmware-releases) and copy the checksum
2. If you are using the PoE wall adapter, connect an Ethernet cable from the PoE port on the wall adapter to RIO port on the radio. **Do not use the LAN port on the adapter.**
3. Connect another Ethernet cable from the DS port on the radio to a laptop.
4. Navigate to [](http://192.168.69.1) in Chrome.

   - If you cannot access the page, you may need to set a static IP on the laptop. Press Windows+R and type `ncpa.cpl` to open the network settings. Right-click on the Ethernet adapter and select "Properties". Select "Internet Protocol Version 4 (TCP/IPv4)" and click "Properties". Set the following settings:
     - IP Address: `192.168.69.2`
     - Subnet Mask: `255.255.255.0`
     - Gateway: `Leave Blank`
     - DNS: `192.168.69.1 or Leave Blank`

5. Upload the firmware and enter the checksum
6. Connect the RIO port on the field radio to port 1 on the field switch