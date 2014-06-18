 SUMMARY:

 The purpose of this script is to provide a method for WhatsApp users to extract their cipher key on NON-ROOTED
 Android devices. The cipher key is required to decrypt WhatsApp CRYPT6 and CRYPT7 backup files. This script
 works by hooking into the USB backup feature on Android 4.0 or higher. It will NOT work with earlier Android
 versions or on devices where this feature has been deliberately disabled by the manufacturer. The cipher key
 can be used with WhatCrypt (www.whatcrypt.com), both on the website (online decryption / exportation) and with
 the Android App (offline decryption / recryption). Other apps and websites may also support WhatsApp cipher keys.
 It should be noted that WhatsApp cipher keys can roll (update) periodically. If this happens then you will need
 to repeat the instructions contained within this file in order to extract the latest cipher key. This script will
 also extract the latest UNENCRYPTED WhatsApp Message Database (msgstore.db) and Contacts Database (wa.db).

 In addition to the above. A copy of the cipher key will also be pushed to the WhatsApp Database directory on the
 device itself and contained within a file called ".nomedia". The reason for this is to allow Android Developers
 a unified method in which they can offer their app users WhatsApp Decryption for those willing to run this script.


 PREREQUISITES:

 1.) O/S: Windows Vista, Windows 7 or Windows 8, or Linux
 2.) Java (will start installation procedure if not already present on your system)
 3.) ADB (Android Debug Bridge) Drivers - If not installed: http://forum.xda-developers.com/showthread.php?t=2588979
 4.) USB Debugging must be enabled on the target device. Settings -> Developer Options -> (Debugging) USB debugging
     If you cannot find Developer Options then please go to: Settings -> About phone/device and tap the Build number
     multiple times until you're finally declared a developer.


 INSTRUCTIONS (WINDOWS):

 1.) Extract "WhatsApp-Key-DB-Extractor.zip" on your computer maintaining the directory structure.
 2.) Browse to the extracted folder and click on "WhatsAppKeyExtract.bat".
 3.) Connect your device via USB*, unlock your screen and wait for "Full backup" to appear.
 4.) Leave the password field blank and tap on "Back up my data".
 5.) The "extracted" folder will now contain your "whatsapp.key", "msgstore.db" and "wa.db".

 * = If you have never used USB Debugging before, you may also need to verify the fingerprint.

 INSTRUCTIONS (LINUX):
 
 1.) Download the script `./whatspp-key-extractor`
 2.) Connect your device via USB*, unlock your screen and ensure that the device is connected by running "adb devices"
 3.) Run ./whatsapp-key-extractor and wait for "Full backup" to appear.
 4.) Leave the password field blank and tap on "Back up my data".
 5.) The key will be copied back onto your machine in such a way that WhatsApp TriCrypt will work
 
 Author: Abinash Bishoyi
 Intial Work: TripCode
 THANKS: Nikolay Elenkov for ade.jar and Snoop05 for ADB Installer.
