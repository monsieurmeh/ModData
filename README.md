# ModData 1.6.2

TLD utility mod for saving/loading custom mod savegame and profile data

***
* Simple usage
* Detects the save name when loaded/created
* Only allows load/save while a save game is active
* Uses an internal cache to reduce disk read/writes
* Deletes associated .moddata file when the save is deleted
* Now includes persistent profile data storage as well, so you can store data that will persist between savegames like feat or custom achievement progress
* [Example File](./example/)
---
* default file (savegame) = \\Mods\\ModData\\**slotName**.moddata (.zip file)
* default file (profile) = \\Mods\\ModData\\profile.moddata (.zip file)
* default entry filename = **modName**
* suffix entry filename = **modName**_**Suffix**

## Usage

```cs
using ModData;
```
```cs
ModDataManager dataManager = new ModDataManager(string modName, [bool debug = false]);
```
```cs
bool dataManager.Save(string data) 
bool dataManager.Save(string data, string? suffix)
bool dataManager.SaveToProfile(string data, string? suffix = null)
```
```cs
string? dataManager.Load() 
string? dataManager.Load(string? suffix)
string? dataManager.LoadFromProfile(string? suffix = null)
```

## Installation

1. If you haven't done so already, install MelonLoader by downloading and running [MelonLoader.Installer.exe](https://github.com/HerpDerpinstine/MelonLoader/releases/latest/download/MelonLoader.Installer.exe)
2. Download the latest version of `ModData.dll` from the [releases page](https://github.com/dommrogers/ModData/releases)
3. Move `ModData.dll` into the Mods folder in your TLD install directory

## Thanks

Thank you to all the helpful devs in the [TLD Modding Discord](https://discord.gg/EhBWKRx) for their patience and help