# BlockKindleOTA
Block Kindle OTA firmware updates with this tool.

An alternative to [renametoabin], [ShutTheBackDoor] and [BinaryRenamer].

## How to use
1. Read the important instructions below.
2. `git clone` or download the project and copy the project folder to the `/extensions` directory in the Kindle root directory.
3. Open `KUAL` and select `Tools` -> `Block OTA` -> `Block`. The device will restart after a moment.

## Important Note
This plugin refers to the method in this post: https://www.mobileread.com/forums/showthread.php?t=327879, which is to prevent the upgrade service from starting by removing (renaming) the binary files related to the upgrade function. This method only works for jailbroken devices. This method attempts to ensure that no new upgrade files are downloaded after blocking, but upgrades can still be made by downloading upgrade files before blocking or manually placing upgrade files after blocking. In addition, in order to ensure that the upgrade service that has been started is completely shut down, the plugin will restart the device once, and at this time **if there is already downloaded firmware, it will enter the upgrade process**. Although the plugin will try to delete the downloaded upgrade files, the situation varies. For safety reasons, please **make sure that the "Update My Kindle" button in the Kindle settings is gray (i.e. unclickable) before clicking "Block OTA"**

You can connect to a computer and check whether there is an upgrade file of one or two hundred megabytes in the Kindle root directory (named, for example, `updatexxxxxxxx.bin). If it exists, deleting it will make the upgrade button gray. In addition, in order to minimize the risk, there are the following suggestions:

> - Install the Jailbreak Hotfix after the device is successfully jailbroken (strongly recommended). This can prevent jailbreaking from failing in extreme cases
> - Don't stay connected to WiFi for very long before blocking firmware upgrades. This reduces the possibility that an upgrade file is downloaded before the blocking is completed
> - Connect to WiFi for a period of time after blocking firmware upgrades and pay attention to the status of the "Update My Kindle" button (it should stay gray) to verify that the blocking is effective. During this period, you need to prevent the device from restarting unexpectedly.

[renametoabin]: https://www.mobileread.com/forums/showpost.php?p=4076733&postcount=25 
[ShutTheBackDoor]: https://www.mobileread.com/forums/showthread.php?t=205666
[BinaryRenamer]: https://www.mobileread.com/forums/showthread.php?p=4380046
