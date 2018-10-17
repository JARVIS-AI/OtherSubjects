# Xiaomi MI5

Xiaomi the chineense mobile manufacturing that sells world wide.

This is my phone Xiaomi Mi5 3GB

Let's start some tricks !

### Unlock Bootloader

For unlocking Mi5

Get permission from site and wait for it

Download tool from site **miflash unlocker**

In Mi5 enable **usb debugging**

Write :

```

adb reboot bootloader

```

After enter **Fastboot**

Connect device to PC

Run app while you have net connection

Login

Success permission

**Unlock it**

**Reboot it**

Done



### Locking Bootloader



For locking again

Enter **Fastboot**

Write :

```

fastboot devices

```

```

fastboot oem device-info

```

```

fastboot oem lock

```

Reboot

Done



## Information

**Why did Mi lock the bootloader for Mi devices?** Mi is an international brand now, but it's only in few countries  currently, and is still in the stage of expanding its international  market. So it's difficult for users from countries where Mi is not  officially sold to buy Mi phones. Many users have taken the risk of  buying from an unofficial reseller. But they sometimes get fake Mi  phones, or Mi phones with unofficial ROM loaded with bloatware. You guys must have seen some users asking in the forum whether their Mi phones  are genuine, or that they have weird ROM version installed on their new  phones. This is really bad for user experience, and it might even cause  property loss if some malware are installed. This situation also exists  in China market.  Another problem Mi users have often encountered is that, after their Mi phones  are lost or stolen, the person who got the device could easily flash a  new ROM into it, and makes it almost impossible for our users to get  their phones back. In the recent MIUI developer version update, we've  added a feature that needs users to enter their Mi account info to use  the phone after doing a full wipe. But if an ill-intentioned person  knows how to use fastboot method to flash ROMs, this will not stop  him/her from gaining control of the phone.    Based on the above two reasons, we've  decided to lock the bootloader. We've also made changes to Mi Cloud's  'Find Device' function, and adjusted system update's verifying logic. By these combined methods, user data can be better protected, and user  experience can also be improved.

**What Mi devices are locked?** Mi 4c, Redmi Note 3, Mi Note Pro, Redmi 3, Mi 4S, Mi 5 and Mi devices launched in the year 2016 onwards

**How to check whether the bootloader is locked/unlocked?** The status of bootloader can be checked in the following process.-The unlocker tool will show the message of "Unlocked".  - An "Unlocked" word will be shown when booting.  - Advanced users can check the bootloader status via cmd

**Flashing full ROM in unlocked bootloader will lock the bootloader again?** No, the bootloader will remain unlocked unless you choose clean all and lock option during fastboot.

**What do you need to know about unlocking?**First and foremost you can only unlock your own device. This means the  unlocking tool you downloaded must be logged in with the same Mi account on your device. One Mi account could only unlock one device within 30  days

**Isn't locking bootloader against Mi's 'geek' spirit?**Locking bootloader is aimed to provide a better user experience, which we've  been trying to do the whole time. In the meantime, we've provided an  unlocking tool for senior users who know their ways around flashing and  tweaking their devices.     The unlocking procedure will need Internet access to get the unlocking  password. Also, the Mi Account logged in on the Mi phone and the  unlocking tool needs to be the same. Otherwise, the unlocking request  will be denied. This will ensure that ill-intentioned people will not  get access to your personal data.

**What will change after locking bootloader?** - Locking bootloader will not affect normal OTA updates  - ROOT will be disabled if the user has enabled it before. Enabling ROOT will need to unlock bootloader  - Recovery mode is changed. Updating via Recovery will need to use Mi PC Suite  - Devices with locked bootloader cannot update using Miflash. Users need to unlock bootloader if they want to flash Fastboot ROMs.

The risks stated above do not fully cover changes which may be brought about by Mi Unlock. We will keep improving Mi Unlock in order to prevent the cases when  unauthorized vendors unlock Mi devices to install third-party apps which worsen MIUI user experience and cannot to be deleted. Locked devices  also provide you with high-quality security features, such as Find  device, and other added-value services. We're sorry for any  inconveniences our policies may cause. Please think twice before unlocking if you are not familiar with ROM flashing.

Final note, if you don't know that much about Android, flashing, custom  ROMs etc. It's not recommended for you to unlock the bootloader. It  might cause serious damage to your device or personal data.



### Flashing Guide



#### Method 1: Local Update

> Note !!!!
>
> Note: You can upgrade your phone by Local Update method without unlocking your phone. The method suits for the situations listed below for sure:  Update to Global Stable ROM from Global Stable ROM, Update to Global  Beta ROM from Global Beta ROM, Update to Global Beta ROM from Global  Stable ROM and vice versa. If you encounter the issue that the reboot  page keep loading for a long time after flashing, you can choose to wipe all data via entering Recovery Mode. You can turn off your device and  then hold both Volume+ button and Power button at the same time to enter Recovery Mode.



1. Download the latest MIUI ROM file  [**Download here**](http://en.miui.com/download.html)

   > There is no need to do it again if you’ve already downloaded the latest ROM file.

2. Connect your device to the Windows PC/laptop via a  micro USB cable, and copy the ROM file downloaded in Step 1 into the  folder ‘downloaded_rom’ in the internal storage of your device.

3. Launch ‘Settings’ app on your device, select ‘About phone’, click  ‘System update’, then press ‘three dots’ icon at the top-right corner,  and select ‘choose update package’ to enter. Choose the ROM file you’ve  put in ‘downloaded_rom’ in Step 2.

4. After choosing the right ROM file, your device will begin upgrading.  Your device should automatically boot to the new version when the update is completed.



#### Method 2: Recovery Update 

> Note !!!!
>
> Please wipe all data in Recovery mode  if you want to update to a discontinuous ROM version, or downgrade to an older ROM version using MIUI full ROM pack. Due to the differences in  Recovery interface, this method is not applicable to some Redmi MTK  devices and devices with locked bootloader. 



1. Download the latest MIUI ROM file [**Download here**](http://en.miui.com/download.html)  Rename the downloaded ROM file to ‘update.zip’ on the computer. 
2. Connect your device to the Windows PC/laptop via a micro USB cable, and  copy the ROM file downloaded and renamed in Step 1 into the root  directory of the internal storage of your device. (Do not put it in any  folder) 
3. Enter the Recovery mode of your device. There are 2 methods to do it as follows:  Method 1: Launch ‘Settings’ app on your device, select ‘About phone’,  click ‘System update’, then click the ‘…’ icon at the top-right corner,  and select ‘Reboot to Recovery mode’ to enter.  Method 2: You can also turn off your device and then hold both Volume+  button and Power button at the same time to enter Recovery mode.
4. In Recovery mode, you can use Volume +/- to select up/down, and Power button to confirm.  After entering Recovery mode, choose the language you use, select  ‘Install update.zip to System One’ and confirm, and then your device  will begin updating automatically. Wait until the update is completed,  choose ‘Reboot to System One’, and then your device should boot to the  new version.



#### Method 2: Fastboot Update

> Note !!!!
>
> Note: A Windows PC/laptop will be needed for the following steps. Make  sure that your device is fully charged or has enough power for this  process. This guide will help you update your device to the latest MIUI  ROM version. All user data will be purged in this process. Please back  up your data and think twice before proceeding.



1. Download [**MIUI ROM Flashing Tool**](http://api.en.miui.com/url/MiFlashTool) (Size: 46 MB). Devices marked with ★ are locked. If your device is locked, please click  [ **here** ](http://en.miui.com/unlock/) to unlock it first.  Devices marked with ☆ are unlocked. If your device is unlocked, please just follow the following tutorial to complete the  ROM flashing.

2. Select the right MIUI ROM version for your phone from the listed below, and download the corresponding package file.
     [**★ Xiaomi Mi 6 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=sagit_global&b=F&r=global&n=)
     [**★ Xiaomi Mi 6 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=sagit_global&b=X&r=global&n=)
     [**★ Xiaomi Mi MIX Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=lithium_global&b=F&r=global&n=)
     [**★ Xiaomi Mi MIX Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=lithium_global&b=X&r=global&n=)
     [**★ Xiaomi Mi MIX 2 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=chiron_global&b=F&r=global&n=)
     [**★ Xiaomi Mi MIX 2 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=chiron_global&b=X&r=global&n=)
     [**★ Xiaomi Mi 8 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=dipper_global&b=F&r=global&n=)
     [**★ Xiaomi Mi 8 Latest Russia Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=dipper_ru_global&b=F&r=global&n=)
     [**★ Xiaomi Mi MIX 2S Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=polaris_global&b=F&r=global&n=)
     [**★ Xiaomi Mi MIX 2S Latest Russia Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=polaris_ru_global&b=F&r=global&n=)
     [**★ Xiaomi Mi MIX 2S Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=polaris_global&b=X&r=global&n=)
     [**★ Redmi S2 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=ysl_global&b=F&r=global&n=)
     [**★ Redmi S2 Latest Russia Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=ysl_ru_global&b=F&r=global&n=)
     [**★ Redmi S2 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=ysl_global&b=X&r=global&n=)
     [**★ Redmi Note 5 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=whyred_global&b=F&r=global&n=)
     [**★ Redmi Note 5 Latest Russia Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=whyred_ru_global&b=F&r=global&n=)
     [**★ Redmi Note 5 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=whyred_global&b=X&r=global&n=)
     [**★ Redmi Note 5 Pro Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=whyred_global&b=F&r=global&n=)
     [**★ Redmi Note 5 Pro Lastest India Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=whyred_global&b=X&r=global&n=)
     [**★ Xiaomi Mi 5 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=gemini_global&b=F&r=global&n=)
     [**★ Xiaomi Mi 5 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=gemini_global&b=X&r=global&n=)
     [**★ Xiaomi Mi Note 2 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=scorpio_global&b=F&r=global&n=)
     [**★ Xiaomi Mi Note 2 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=scorpio_global&b=X&r=global&n=)
     [**★ Redmi Note 4X Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=mido_global&b=F&r=global&n=)
     [**★ Redmi Note 4X Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=mido_global&b=X&r=global&n=)
     [**★ Xiaomi Mi 5s Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=capricorn_global&b=F&r=global&n=)
     [**★ Xiaomi Mi 5s Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=capricorn_global&b=X&r=global&n=)
     [**★ Xiaomi Mi 5s Plus Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=natrium_global&b=F&r=global&n=)
     [**★ Xiaomi Mi 5s Plus Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=natrium_global&b=X&r=global&n=)
     [**★ Redmi 4X Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=santoni_global&b=F&r=global&n=)
     [**★ Redmi 4X Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=santoni_global&b=X&r=global&n=)
     [**★ Redmi Note 5A Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=ugglite_global&b=F&r=global&n=)
     [**★ Redmi Note 5A Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=ugglite_global&b=X&r=global&n=)
     [**★ Redmi Note 5A Prime Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=ugg_global&b=F&r=global&n=)
     [**★ Redmi Note 5A Prime Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=ugg_global&b=X&r=global&n=)
     [**★ Redmi 5 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=rosy_global&b=F&r=global&n=)
     [**★ Redmi 5 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=rosy_global&b=X&r=global&n=)
     [**★ Redmi 5 Plus Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=vince_global&b=F&r=global&n=)
     [**★ Redmi 5 Plus Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=vince_global&b=X&r=global&n=)
     [**★ Mi Max Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=hydrogen_global&b=F&r=global&n=)
     [**★ Mi Max Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=hydrogen_global&b=X&r=global&n=)
     [**★ Mi Max Prime Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=helium_global&b=F&r=global&n=)
     [**★ Mi Max Prime Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=helium_global&b=X&r=global&n=)
     [**★ Mi Max 2 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=oxygen_global&b=F&r=global&n=)
     [**★ Mi Max 2 Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=oxygen_global&b=X&r=global&n=)
     [**★ Redmi 4A Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=rolex_global&b=F&r=global&n=)
     [**★ Redmi 4A Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=rolex_global&b=X&r=global&n=)
     [**★ Redmi 5A Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=riva_global&b=F&r=global&n=)
     [**★ Redmi 5A Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=riva_global&b=X&r=global&n=)
     [**★ Redmi 3S Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=land_global&b=F&r=global&n=)
     [**★ Redmi 3S Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=land_global&b=X&r=global&n=)
     [**★ Redmi Note 3 SD Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=kenzo_global&b=F&r=global&n=)
     [**★ Redmi Note 3 SD Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=kenzo_global&b=X&r=global&n=)
     [**★ Redmi Note 3 Special Edition Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=kate_global&b=F&r=global&n=)
     [**★ Redmi Note 3 Special Edition Lastest Global Developer Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=kate_global&b=X&r=global&n=)
     [**★ Mi Note 3 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=jason_global&b=F&r=global&n=)
     [**★ Redmi 4 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=prada_global&b=F&r=global&n=)
     [**★ Redmi 6A Latest Russial Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=cactus_ru_global&b=F&r=global&n=)
     [**★ Redmi 6A Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=cactus_global&b=F&r=global&n=)
     [**★ Redmi 6 Latest Russial Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=cereus_ru_global&b=F&r=global&n=)
     [**★ Redmi 6 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=cereus_global&b=F&r=global&n=)
     [**★ Redmi 6 Pro Latest Indian Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=sakura_india_global&b=F&r=global&n=)
     [**★ Redmi Note 2 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=hermes_global&b=F&r=global&n=)
     [**★ Redmi Note 4 MTK Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=nikel_global&b=F&r=global&n=)
     [**★ POCO F1 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=beryllium_global&b=F&r=global&n=)
     [**★ Xiaomi Mi 3 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=cancro_global&b=F&r=global&n=)
     [**★ Xiaomi Mi 4 Latest Global Stable Version Fastboot File Download**](http://update.miui.com/updates/v1/fullromdownload.php?d=cancro_global&b=F&r=global&n=)

   ​       Fastboot download links will be successively released to  the public in the near future. Thanks for your understanding and  patience. Please stay tuned!

   ​           **(Please check if the ROM file suffix is '.tgz'. If it is '.gz', please rename it to '.tgz')**

3. Turn off the device. Press the Volume– key and the Power button  at the same time to enter Fastboot mode. Then connect the device to the  Windows PC/laptop via a micro USB cable

4. Double click on the downloaded ROM file to decompress it. Open  the file folder for the decompressed ROM pack, and copy its path on the  computer.

   Decompress the MIUI ROM flashing tool downloaded  in Step 1, and double click on it to install (if there is security  warning, select ``Run``). After installation is completed, open  MiFlash.exe and paste into the address bar the ROM file folder path  copied in the last step. Click on the first button (circled out in yellow) to Refresh, and MiFlash should automatically recognize the device. Then click the second button (circled out in red) to flash the ROM file to the device.

   Wait until the progress bar inside MiFlash turns fully green,  which means the ROM has been successfully installed. Then your device  should automatically boot to the new version.

   If the flashing guide could not help you, please download Mi PC Suite here (After Mi PC Suite is installed, make sure that your phone is in fastboot mode, connect your phone to a computer, and select the correct ROM file to flash)

   

   

   

   