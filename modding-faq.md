# Modding FAQ

## First time using/downloading a _LogicMod_? follow these steps: 
- Download the mod file(`.pak`) and the latest [UnrealModLoader](<https://github.com/dmgvol/UnrealModLoader/releases/latest>). (the UnrealModLoader.V2.2.1a.zip ) 
- Unpack the UnrealModLoader rar (doesn't matter where).
- Navigate to Ghostrunner installation folder, folder Paks:</br>
`\Ghostrunner\Ghostrunner\Content\Paks\` and create a new directory named `LogicMods`.
- Place the downloaded `.pak` file into that `LogicMods` folder.
- Navigate back to `Paks`, duplicate `Ghostrunner-WindowsNoEditor.sig`, rename that file to match the mod's name and move it to `LogicMods`. </br>
For example: if the mod is `WaveMod.pak` then it should be: `WaveMod.sig`.
- Launch `UnrealEngineModLauncher.exe` and then Ghostrunner.
- It should display "successfully loaded [modname]" for each of your mods, inside the modloader console window.
- Enjoy!
  
___
</br></br></br>

### - How to install mods?
__For regular mods(ending with `_P` in their name);__
- Place your `.pak` files into `..\Ghostrunner\Ghostrunner\Content\Paks`.
- Latest GR version? then duplicate `Ghostrunner-WindowsNoEditor.sig` and rename it to match your mod name `<modname>.sig`. 
- Launch the game.

__For LogicMods(that require the modloader);__
- Same steps as with regular mods but inside `\Paks\LogicMods\`. 
- Once done, launch `UnrealEngineModLauncher.exe` and then Ghostrunner.

### How to use modloader?
- Make sure you have the latest version downloaded from [**here**](https://github.com/dmgvol/UnrealModLoader/releases/latest)
- Navigate to `Ghostrunner\Content\Paks\` and create a new folder named `LogicMods`.
- Place your mods inside LogicMods folder along with their matching `.sig` files.
- Run the modloader and launch GR, it should display "successfully loaded <modname>" for each of your mods.

### - Mods stopped working with latest patch
Since the latest GR update, game files are now encrypted which require all mods to have a copy and renamed `.sig` file to match each mod; 
- Navigate to Paks folder, duplicate `Ghostrunner-WindowsNoEditor.sig` and rename it to match your mod name `<modname>.sig`. 
- If the mod is a LogicMod then move the matching `.sig` file into `/LogicMods`.

### - Modloader is crashing the game
Try launching the modloader without any mods in `LogicMods` and if that issue persists then: 
- Navigate to UnrealModLoader directory, then Profiles, and open `Ghostrunner-Win64-Shipping.profile` with a text editor.
- Remove everything besides the 3 first lines;
```cs
[GameInfo]
UsesFNamePool=1
IsUsingFChunkedFixedUObjectArray=1
```
If it still crashes the game, ask on Discord.

### - Modloader crashing with DX11 error
Make sure you launch the game in dx11 since modloader supports only dx11 by design, but there are plans to add support dx12 in the future.

### - Modloader is stuck on "Waiting for game window"
It may be due to a permission issue, try running the modloader as administrator.

### Can I make the modloader launch automatically?
- The newest version of the modloader  comes with an auto-injector in its tools folder (instructions are in the README but I'll explain here)
- Open the ModLoaderInfo.ini and edit the path to where your modloader .dll is stored
- Copy all the files(README isn't needed) to where the game binary is stored (in `Ghostrunner\Ghostrunner\Binaries\Win64`)
- Run the binary and the modloader should auto-inject into the process

---
### Still having issues?
Feel free to join the [GRSR Discord](https://discord.gg/eZRz3Q5) and ask! </br>
(or the Official GR server)
