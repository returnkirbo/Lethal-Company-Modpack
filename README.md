# Lethal Company Modpack

This Windows powershell script installs BepInEx dependency by default and installs any other mods (Thunderstore) you specify with the given format.

Initially, this was made to ease the additional installation of additional mods for [Lethalize](https://github.com/KrystilizeNevaDies/Lethalize) for my friends as an alternative towards a mod manager, but feel free to use it if you'd like.

## Installing/Modifying

In order to install, you must modify the script to your liking. Below is the given format.
```
powershell -nop -ExecutionPolicy Bypass -c "Invoke-Command -ScriptBlock ([scriptblock]::Create([System.Text.Encoding]::UTF8.GetString((New-Object Net.WebClient).DownloadData('https://github.com/returnkirbo/Lethal-Company-Modpack/releases/download/release/Install-Modpack.ps1')))) -ArgumentList @( `
    '-authorName/modName','versionNumber', `
    '-authorName/modName','versionNumber')"
```
Ensure that you have the correct syntax otherwise the script may not execute correctly.
<br>``'`` specifies each invididual argument | ex. ``'-notnotnotswipez/MoreCompany','1.7.2'``
<br>``,`` refers to next line, required after | ex. ``'-notnotnotswipez/MoreCompany','1.7.2',``
<br>`` ` `` refers to new line | ex. ``'-notnotnotswipez/MoreCompany','1.7.2', ` ``
<br>``)"`` closes the list | ex. ``'-Renegades/FlashlightToggle','1.4.1')"``

If you receive a 404 Not Found error it most likely means that one of the arguments set does not correctly match the given mod either due to misspelling, nonexistent version, or the mod not exist at all.

Below is an example of what a script may look. You may also use this if you'd like as it's used within my friendgroup as our modpack.

```
powershell -nop -ExecutionPolicy Bypass -c "Invoke-Command -ScriptBlock ([scriptblock]::Create([System.Text.Encoding]::UTF8.GetString((New-Object Net.WebClient).DownloadData('https://github.com/returnkirbo/Lethal-Company-Modpack/releases/download/release/Install-Modpack.ps1')))) -ArgumentList @( `
    '-notnotnotswipez/MoreCompany','1.7.2', `
    '-RugbugRedfern/Skinwalkers','2.0.1', `
    '-RickArg/Helmet_Cameras','2.1.5', `
    '-x753/More_Suits','1.4.1', `
    '-Sligili/More_Emotes','1.2.1', `
    '-KoderTeh/Boombox_Controller','1.1.0', `
    '-tinyhoot/ShipLobby','1.0.2', `
    '-sunnobunno/YippeeMod','1.2.2', `
    '-AllToasters/SpectateEnemies','1.5.0', `
    '-Ryokune/CompatibilityChecker','1.1.1', `
    '-Suskitech/AlwaysHearActiveWalkies','1.4.2', `
    '-Renegades/WalkieUse','1.3.1', `
    '-Renegades/FlashlightToggle','1.4.1')"
```

Afterwards, execute the script in Windows's powershell. 
<br>*In the scenario where you come across a mod where it's not installed at the correct path, open an issue and I'll add a check for it.*
                  
## Mods used within my modpack + Credits

Lethal Company -> 45

[BepInExPack](https://thunderstore.io/c/lethal-company/p/BepInEx/BepInExPack/) -> always latest
<br>[MoreCompany](https://thunderstore.io/c/lethal-company/p/notnotnotswipez/MoreCompany/) -> 1.7.2
<br>[SkinWalkers](https://thunderstore.io/c/lethal-company/p/RugbugRedfern/Skinwalkers/) -> 2.0.1
<br>[HelmetCameras](https://thunderstore.io/c/lethal-company/p/RickArg/Helmet_Cameras/) -> 2.1.5
<br>[MoreSuits](https://thunderstore.io/c/lethal-company/p/x753/More_Suits/) -> 1.4.1
<br>[MoreEmotes](https://thunderstore.io/c/lethal-company/p/Sligili/More_Emotes/) -> 1.2.1
<br>[Boombox_Controller](https://thunderstore.io/c/lethal-company/p/KoderTeh/Boombox_Controller/) -> 1.1.0
<br>[ShipLobby](https://thunderstore.io/c/lethal-company/p/tinyhoot/ShipLobby/) -> 1.0.2
<br>[YippeeMod](https://thunderstore.io/c/lethal-company/p/sunnobunno/YippeeMod/) -> 1.2.3
<br>[SpectateEnemies](https://thunderstore.io/c/lethal-company/p/AllToasters/SpectateEnemies/) -> 1.5.0
<br>[CompatibilityChecker](https://thunderstore.io/c/lethal-company/p/Ryokune/CompatibilityChecker/) -> 1.1.1
<br>[AlwaysHearActiveWalkies](https://thunderstore.io/c/lethal-company/p/Suskitech/AlwaysHearActiveWalkies/) -> 1.4.2
<br>[WalkieUse](https://thunderstore.io/c/lethal-company/p/Renegades/WalkieUse/) -> 1.3.1
<br>[FlashlightToggle](https://thunderstore.io/c/lethal-company/p/Renegades/FlashlightToggle/) -> 1.4.1

Want a mod added? Issues? Questions? File an issue and I'll get to you soon.

This is a modified version of [Lethalize](https://github.com/KrystilizeNevaDies/Lethalize) with the option to add any mod you'd like. Full thanks to KrystilizeNevaDies!
