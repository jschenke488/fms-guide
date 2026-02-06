# Setting up a Field Radio

## Required Hardware

- Robot Radio
- [Vivid-Hosting PoE wall adapter](https://wcproducts.com/products/frc-radio) (must be Vivid-Hosting brand) **OR** 12V DC power supply connected to the Weidmuller on the robot radio.
- Ethernet cables
- Heatsink for the radio. The radio will overheat without one. You can buy a heatsink from [WestCoast Products](https://wcproducts.com/products/frc-radio) or make your own. A fan is recommended, but not required.

## Steps

1. If you are using the PoE wall adapter, connect an Ethernet cable from the PoE port on the wall adapter to RIO port on the radio. **Do not use the LAN port on the adapter.**
2. Connect another Ethernet cable from the DS port on the radio to a laptop.
3. Navigate to [](http://192.168.69.1) in Chrome.

   - If you cannot access the page, you may need to set a static IP on the laptop:
     - IP Address: `192.168.69.2`
     - Subnet Mask: `255.255.255.0`
     - Gateway: `Leave Blank`
     - DNS: `192.168.69.1 or Leave Blank`

4. Select "Access Point Mode"
5. Set the following settings:
   - 2.4 GHz Wi-Fi: `Disabled`
   - Team Number: `1730`
   - WPA Key: `Ask a mentor`
   - Wi-Fi Channel: `13`

**Do not set an SSID suffix!**

6. Click "Configure".