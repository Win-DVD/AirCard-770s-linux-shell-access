# AirCard-770s-linux-shell-access
This guide is for the Sierra Wireless / Netgear Aircard 770s aka ATT Unite. It will provide linux shell access for running your own software.

Do AT!OPENLOCK? to get a challenge code.  
Use https://sierra-keygen.uu.sg/ or any other Sierra challenge response gen to unlock it with the generated challenge response.  
Device generation must be set to MDM9X15. And we are unlocking the AT!OPENLOCK command with it.

### Example:

`AT!OPENLOCK? D6BFBEC30D47BDD1` unlocks with `AT!OPENLOCK="86120F62B9EC8C9F"`

Now you can do this command:

`AT!CUSTOM="ADBENABLE", 1`

This will enable ADB.  
Once you do this, Simply reboot. Can use the power button or `AT!GRESET`

If on Windows, you should see a new AirCard 770s device likely with no driver. Hardware ID being `USB\Vid_1199&Pid_9053&MI_01`  
You can use the official Google ADB driver with this (https://dl.google.com/android/repository/usb_driver_r13-windows.zip).  
Though Windows will likely say it may not work due to non matching HWID, install it anyway.

If you don't already, you will need some kind of ADB application.  
You can use the one from Android Studio OR alternatively use https://xdaforums.com/t/tool-minimal-adb-and-fastboot-2-9-18.2317790/ for space savings.

Once you are at the ADB program of choice, you are basically done.  
Just run `adb shell` and you are golden. full shell access. It's that easy. You can now run the programs your heart desires.
You can also start a telnet and ftp server if you wish.

Here is a picture of one running doom.
<img width="2040" height="1459" alt="aircarddoom" src="https://github.com/user-attachments/assets/d2d7c239-6920-46c6-9ee2-a822af50e7c0" />
