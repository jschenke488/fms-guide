# Setting up a WPA Kiosk

To program robot radios to connect to the field radio, a WPA Kiosk is used. This is a computer connected to the field network that generates WPA keys and programs them into robot radios. Ideally, you should have a separate computer for the WPA kiosk.

## Hardware

The WPA Kiosk consists of:
- A laptop running Windows
- A USB-to-Ethernet adapter (even if the computer has one built-in)
- Ethernet cables
- [Vivid-Hosting PoE wall adapter](https://wcproducts.com/products/frc-radio) (must be Vivid-Hosting brand) **OR** 12V DC power supply connected to the Weidmuller on the robot radio.

## Software

1. On the laptop, you need to enable virtualization in the BIOS. Because this process varies by computer model, look on the internet for instructions on how to do this.
2. Install [WSL (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install) and [Docker Desktop](https://apps.microsoft.com/detail/xp8cbj40xlbwkx?hl=en-US&gl=US).
3. Download the WPA Kiosk installer from [Box](https://vividhosting.app.box.com/v/frc-radio-kiosk).
4. Plug the USB-to-Ethernet adapter into the laptop and connect to DS port on a robot radio. **You must have a robot radio connected to the WPA Kiosk while setting it up.**
5. Extract the contents of the ZIP file to a folder on the computer. Run the executable as an administrator.
6. Select the Ethernet adapter the dropdown menu. Click "Configure".
7. Run the self-test
8. Open Chrome and navigate to [http://localhost](http://localhost). You should see the WPA Kiosk interface.
9. Hover over the F in FRC to the right of the Vivid-Hosting logo until the text changes to "FTA". Click it to open the FTA configuration page.
10. Click "Set Keys" and upload a CSV file in the following format:
```
1730,password,1730
```
The first column is the team number, the second column is the WPA key (password), and the third column is the team number again.

11. Click "Upload". The password is `supercoolpassword`.
12. Once the upload is complete, return to the main WPA Kiosk page.
13. To use the WPA kiosk again, make sure you open Docker Desktop and have the same USB-to-Ethernet adapter plugged in.