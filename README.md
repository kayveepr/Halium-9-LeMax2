# Halium 9 on Le Max 2 aka X2
WIP for H9

This is a work in progress at infancy Halium 9 porting to LeEco X2. This is not a standalone porting but depends on 
LineageOS 16.0 repos and Erfanoabdi's ubports GSI installer.

Please refer to https://github.com/ubports/porting-notes/wiki/Halium-9 for more information.

At present(Jun 2020) X2 boots up with the uploaded boot img file with LineageOS, Baikal or CBG MIUI11-Global for X2 all P vendors.Please be aware that bugs are aplenty.

With LineageOS P vendor - only one SIM on slot 1 detected. Both data and calls work on SIM with 2G/3G fallback. With exclusive 4G SIM only data works. No ringtone only vibrate. GPS works. Screen rotation works other way around. Power button sleep and light sensor do not work.

With BaikalOS and CBG MIUI vendors both SIMs are detected. No in call audio. Screen rotation works OK. Rest as above except power button sleep and light sensor work with CBG MIUI for X2 P vendor.

Create a directory "local_manifests" under <parent_dir>/.repo and copy local_manifests.xml for LineageOS 16.0 repo sync. Else do manually.

"apparmor" as default security. GPS tested working well with webapps requesting for permission to use.
