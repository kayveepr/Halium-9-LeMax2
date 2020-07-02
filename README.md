# H9
WIP for H9

This is a work in progress at infancy Halium 9 porting to LeEco X2. This is not a standalone porting but depends on 
LineageOS 16.0 repos and Erfanoabdi's ubports GSI installer.

Please refer to https://github.com/ubports/porting-notes/wiki/Halium-9 for more information.

At present(May 2020) X2 boots up with the uploaded boot img file with LOS, Baikal or CBG MIUI11-Global P vendors.Please be 
aware that bugs are aplenty and unstable as each reboot results in different device profile. One may find what worked once
does not work on reboot.
Create a directory "local_manifests" under <parent_dir>/.repo and copy local_manifests.xml for LineageOS 16.0 repo sync. Else
do manually.
"apparmor" as default security. GPS tested working well with webapps requesting for permission to use.
