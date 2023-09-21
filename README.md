How to re-purpose a useless iSmartAlarm Spot+ (iSC5P) camera ?
Intro
If you are on this page you probably did the same mistake as I did and bought yourself iSmartAlarm equipment. I have been looking at ways to re-use the iSmartAlarm hardware but unfortunately it isn't so easy.
You can read my blog post here:
xxxx


Prepare your micro SD card
Flashing the device seems to be one where a lot of people fail, they do not see a blue light flashing or they just get a permanent orange light… .
1. Download and install Win32 Disk Imager (Win32 Disk Imager download | SourceForge.net) or any other tool that can burn an image file to a micro SD.
2. Download the image from fang-hacks (https://github.com/samtap/fang-hacks/releases/download/0.2.0/fanghacks_v0.2.0.zip)
3. Burn , with Win32 Disk Imager, the image to the micro SD.
Note: Please try different SD cards if it fails, I was lucky with a 1 and 2 GB drive. I was unsuccessful with a 16 GB drive.
Preparing the firmware and putting on the SD Card.
1. Download the firmware - upd_isa.camera.isc5.bin.extracted (https://mega.nz/#!GBghwbpY!btf0jxHPFTPtifqNJNMHXEiRd3H5DkUtOJYOq8QpgfQ)
2. Extract the file and place it in the root of your sd card
3. Rename the file 0.elf to FIRMWARE_660R.bin
4. Disconnect the sd card from your computer

Flash your iSmartAlarm Spot+'s firmware.
1. Disconnect the camera from the power source
2. Insert the sd card (with the firmware in the root folder) into the camera
3. Plug the camera into the power source while holding down the setup button
Note: Make sure you press the setup button before you connect the power and keep it pressed in

4. Wait for 15 seconds until the light starts blinking blue and orange and after that blue
Note: I had the above on one device, but on another device I had that it was permanently orange. After about 15–20 seconds I released the setup button and it was blinking orange, I then continued with step 6.
5. Release the setup button
6. Wait for a few minutes (get a drink, or some food) - just wait
7. The camera should auto reboot after flashing - just be patient and wait
8. After all of this you can press the setup button again and you will hear the device say something (can be in Chinese, don't worry 😊). Also, the device repeats the same text.
Note: If you do not hear a text, something is not correct and I would recommend to start over.
9. Unplug the camera from the power supply

Connecting the camera to your Wireless Network
1. Unplug the sd card from the device and back into your computer.
2. Copy all the files from this zip (https://github.com/davidjb/fang-wlan-setup/archive/refs/heads/master.zip) onto the root of the sd.
3. Open .wifipasswd and .wifissid and enter the details of your wireless network. SSID in the .wifissid file and password in .wifipasswd.
Note: For more information on step 3, please go to GitHub - davidjb/fang-wlan-setup: WLAN setup of XiaoFang cameras without app usage
4. Boot the camera without the sd card plugged in. Wait for a good minute, making sure it is fully booted.
5. Plug in your sd card into the device and wait at least 10–30 seconds (longest I had to wait was about 25 second). You should hear "kling klang" coming out of the camera.
6. Disconnect the camera from the power socket, wait a good 5–10 seconds, and plug it back in
Note: In this step we did not unplug the sd card, so it is still plugged in
7. After about a minute you should see a blue light flashing. This means the device is connected to your wireless network!

Access your camera via a browser
1. Using your preferred network management tools you will need to verify what IP address your camera has. You can use any tool you like. I did it by just looking at all joined devices on my network.
2. If you have the IP address , you should see if you can ping it. If you can not ping it , there is something wrong. Verify the light is blinking (blue)? Else repeat and start over.
3. If you can ping the device, try to go to http://ip-address/cgi-bin/status.
Note: If you get a 404 error with a flashing blue led, remove the sdcard and re insert it after a few seconds. Shortly after re inserting, the camera will go make some noise. Retry the link now.

