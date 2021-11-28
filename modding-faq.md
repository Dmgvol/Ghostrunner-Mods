# Modding FAQ

### How to install mods?
__For regular mods(ending with `_P` in their name);__
- Place your `.pak` files into `..\Ghostrunner\Ghostrunner\Content\Paks`.
- Latest GR version? then duplicate `Ghostrunner-WindowsNoEditor.sig` and rename it to match your mod name `<modname>.sig`. 

__For LogicMods(that require the modloader);__
- Same steps as with regular mods but inside `\Paks\LogicMods\`. 

### How to use modloader?
- Make sure you have the latest version downloaded; <https://github.com/RussellJerome/UnrealModLoader/releases>
- Navigate to `Ghostrunner\Content\Paks\` and create a new folder named `LogicMods`.
- Place your mods inside LogicMods folder along with their matching `.sig` files.
- Run the modloader and launch GR, it should display "successfully loaded <modname>" for each of your mods.

### Mods stopped working with latest patch?
Since the latest GR update, game files are now encrypted which require all mods to have a copy and renamed `.sig` file to match each mod; 
- Navigate to Paks folder, duplicate `Ghostrunner-WindowsNoEditor.sig` and rename it to match your mod name `<modname>.sig`. 
- If the mod is a LogicMod then move the matching `.sig` file into `/LogicMods`.

### Modloader is crashing the game?
- Navigate to UnrealModLoader directory, then Profiles, and open `Ghostrunner-Win64-Shipping.profile` with a text editor.
- Remove everything besides the 3 first lines;
```cs
[GameInfo]
UsesFNamePool=1
IsUsingFChunkedFixedUObjectArray=1
```

### Modloader crashing with DX11 error?
Make sure you launch the game in dx11 since modloader supports only dx11 by design, but there are plans to add support dx12 in the future.


---
### Still having issues?
Feel free to join the [GRSR Discord](https://discord.gg/eZRz3Q5) and ask!