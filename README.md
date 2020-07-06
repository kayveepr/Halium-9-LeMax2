# Halium 9 on LeEco LeMax 2 aka X2
WIP for H9

This is a work in progress at infancy Halium 9 porting to LeEco X2. This is not a standalone porting but depends on 
LineageOS 16.0 repos and Erfanoabdi's ubports GSI installer.

Please refer to https://github.com/ubports/porting-notes/wiki/Halium-9 for more information.

At present(Jun 2020) X2 boots up with the uploaded boot img file with AEX, AOSiP, LineageOS, Baikal or CBG MIUI11-Global for X2 all P vendors.Please be aware that bugs are aplenty. Common issues are Camera, FP and magnetometer.

Issues: 

In all cases GPS works. Whereever both SIMs are detected data works from LTE SIM from slot 1. For calls use a SIm with 2G/3G fallback as VoLTE does not work.

With LineageOS P vendor - only one SIM on slot 1 detected. Both data and calls work on SIM with 2G/3G fallback. With exclusive 4G SIM only data works. No ringtone only vibrate. GPS works. Screen rotation works other way around. Power button sleep and light sensor do not work. Data works on single SIM.

With BaikalOS and CBG MIUI vendors both SIMs are detected. No in call audio. Screen rotation works OK. Rest as above except power button sleep and light sensor work with CBG MIUI for X2 P vendor.

AEX P - Both SIMs detected, in-call audio works, some sensors detected. 

Create a directory "local_manifests" under <parent_dir>/.repo and copy local_manifests.xml for LineageOS 16.0 repo sync. Else do manually.

"apparmor" as default security. GPS tested working well with webapps requesting for permission to use.

Installation Instructions:

Disclaimer: Sincerely hope the X2 device anyone tries Halium 9 on X2 as given here does not get bricked. Should that happen please bear in mind that anyone tries Halium 9 on X2 as given here does so at his/her own risk.

Requirements:

1. TWRP 3.3.1-0 for X2 downloadable from https://dl.twrp.me/x2/. 3.4.0-0 should work too.
2. Download AEX P ROM for X2 from https://downloads.aospextended.com/download/x2/pie/AospExtended-v6.6-x2-20190728-1658-OFFICIAL.zip. This is a no GApps one.
3. Download Halium 9 GSI from Erfanoabdi's - https://build.lolinet.com/file/halium/GSI/ubports_GSI_installer_v9.zip - as tested.
4. Backup your existing data/ROM, boot to TWRP - wipe data. One may optionally wipe all on reboot to recovery.
5. Install AEX P or any mentioned P ROMs. No need to reboot.
6. Insatll GSI zip.
7. Reboot to bootloader and install halium-boot.img via "fastboot flash boot halium-boot.img" command(without quotes) giving appropriate path to wherever the boot img file is,
8. Reboot.

Pleas note it is WIP and adb sideload is preferred for both P and GSI zip so that one can avoid transferring files to device after wipe. Theoratically halium-boot.img, ubports-GSI zip file and P Vendor img file are good enoigh to boot and try Halium 9 GSI on X2. Please note that "not" all P ROMs or vendor img files work on X2 and hence use only what has been mentioned here. This notwithstanding one may find logcat filled with errors for FP and Camera.

All credits go to Erfanoabdi(GSI), Marc(LineageOS source and other guidance), andr68rus(BaikalOS), CBG(MIUI P Global for X2), shivatejapeddi(AEX). moto999999(AOSiP).
