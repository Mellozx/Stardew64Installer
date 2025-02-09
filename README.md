# Stardew64Installer
This handy piece of software is capable of turning a Linux installation of Stardew Valley into a working 64bit Windows version!

## Installation Instructions
All you need is a folder with a Linux installation of Stardew Valley (obtained via DepotDownloader).

Please note that this isn't all that useful to the average user since this currently only supports vanilla SDV.

**NOTE:** Due to the fact that this program messes with files (moves, copies, and modifies), AntiViruses may flag or other-wise block this program from performing tasks. If this is the case, please whitelist this program.

CorFlags.exe may also fail to modify MONOMODDED_StardewValley.exe. If this is the case, please re-launch the program with administrator privileges.

**Usage instructions:**

0. Locate and/or obtain a copy of the Linux version of SDV.
1. Open *SDV.Installer.exe*
2. Confirm that you're "good to go!"
3. Enter the directory of your Linux copy.
4. Wait. (These's a hard-coded wait time once you reach the MonoMod patching step to allow time from MonoMod to write MONOMODDED_StardewValley.exe) (If it hangs there for over 15-30 seconds, try re-executing the program)
5. Launch *StardewValley.exe* in the depot-download folder, as it is now modified.

Credit to [@Dradonhunter11](https://github.com/Dradonhunter11) for figuring out how to make SDV 64bit actually work. This program simply automates a majority of that process.

## Program Info
Stardew64Installer is split into two parts: SDV.Installer and StardewValley.Patches.mm. These two projects work together to allow the patching of StardewValley.exe and the automated installation.

Behind the scenes, CorFlags.exe is utilized to modify MONOMODDED_StardewValley.exe and [MonoMod](https://github.com/MonoMod/MonoMod) is used to patch StardewValley.exe.

For the actual steps this program automates, see: [SMAPI Issue #767](https://github.com/Pathoschild/SMAPI/issues/767#issuecomment-799046253). (However, do note that CorFlags is used to modify MONOMODDED_StardewValley.exe, not Steamworks.NET.dll)

### SDV.Installer
SDV.Installer is a very simple command window program that asks the user for the directory of their Linux SDV installation and shows the user what's currently happening behind the scenes. Nothing fancy.

### StardewValley.Patches.mm
StardewValley.Patches.mm contains patches utilized by Stardew64Installer to allow the Linux version of SDV to work. This currently only patches StardewValley.KeyboardDispatcher..ctor.

## Contributing
Contributing is simple. I don't have a set style guide or any real guidelines to follow, just feel free to PR any changes you feel are fit to make and explain your reasoning as well. We'll discuss further once a PR is made (or you can contact me directly before-hand).

## SMAPI
SMAPI is currently unsupport, however; support should be coming to SMAPI itself within this week (as of March 17th, 2021). It will change its installer to support Windows XNA and Windows with a Linux install. (See: https://gyazo.com/836b01128839e8d493282836c132ce1a.png)

## TODO
- [ ] Automated Linux install through [DepotDownloader](https://github.com/SteamRE/DepotDownloader).
- [ ] Determine what DLLs are actually required for a proper installation.
- [ ] Remove the need to move \SDVLibs\ files into the main execution folder while keeping the source clean.
- [ ] SMAPI support.
