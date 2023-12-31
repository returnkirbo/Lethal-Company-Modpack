# Lethal Company Modpack

This Windows powershell script allows you to install BepInEx (by default) and any [Thunderstore](https://thunderstore.io/c/lethal-company) mods/modpacks for Lethal Company you specify with the given format with ease of distribution among your friends.

Initially, this was made to ease the additional installation of additional mods for [Lethalize](https://github.com/KrystilizeNevaDies/Lethalize) for my friends as an alternative towards a mod manager, but feel free to use it if you'd like.

"hey man just pop this script into powershell"

## Installing Singular Mod(s)

In order to install a mod, you must modify the script to your liking. Below is the given format.
```
powershell -nop -ExecutionPolicy Bypass -c "Invoke-Command -ScriptBlock ([scriptblock]::Create([System.Text.Encoding]::UTF8.GetString((New-Object Net.WebClient).DownloadData('https://raw.githubusercontent.com/returnkirbo/Lethal-Company-Modpack/06b38be795f6ecb960c73025e1eba4249a044190/Install-Modpack.ps1')))) -ArgumentList @( `
'-authorName/modName','versionNumber', `
'-authorName/modName','versionNumber')"
```

Below is an example of what a script may look. You may also use this if you'd like as it's used within my friendgroup as our modpack.

```
powershell -nop -ExecutionPolicy Bypass -c "Invoke-Command -ScriptBlock ([scriptblock]::Create([System.Text.Encoding]::UTF8.GetString((New-Object Net.WebClient).DownloadData('https://raw.githubusercontent.com/returnkirbo/Lethal-Company-Modpack/06b38be795f6ecb960c73025e1eba4249a044190/Install-Modpack.ps1')))) -ArgumentList @( `
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

## Installing Thunderstore Modpacks + Optional Mod(s)

Below is the given format for installing a modpack. All BepInEx configs that come from modpacks are saved as long they aren't overwritten.
```
powershell -nop -ExecutionPolicy Bypass -c "Invoke-Command -ScriptBlock ([scriptblock]::Create([System.Text.Encoding]::UTF8.GetString((New-Object Net.WebClient).DownloadData('https://raw.githubusercontent.com/returnkirbo/Lethal-Company-Modpack/06b38be795f6ecb960c73025e1eba4249a044190/Install-Modpack.ps1')))) -ArgumentList @( `
'-modpack','authorName/modPackName','versionNumber')"
```

To add mods ontop of a modpack, just add a new line of arguments similar to installing a singular mod. Declaring a modpack should be the **first** arguments given.
```
powershell -nop -ExecutionPolicy Bypass -c "Invoke-Command -ScriptBlock ([scriptblock]::Create([System.Text.Encoding]::UTF8.GetString((New-Object Net.WebClient).DownloadData('https://raw.githubusercontent.com/returnkirbo/Lethal-Company-Modpack/06b38be795f6ecb960c73025e1eba4249a044190/Install-Modpack.ps1')))) -ArgumentList @( `
'-modpack','authorName/modName','versionNumber', `
'-authorName/modName','versionNumber')"
```

Afterwards, execute the script in Windows's powershell. 

As of right now, only one modpack can be downloaded so if you wish to add more mods, just add a new line with the correct format.

## Powershell Syntax

Ensure that you have the correct syntax otherwise the script may not execute correctly.
<br>``'`` specifies each invididual argument | ex. ``'-notnotnotswipez/MoreCompany','1.7.2'``
<br>``,`` refers to next line, required after a ``'`` | ex. ``'-notnotnotswipez/MoreCompany','1.7.2',``
<br>`` ` `` refers to new line | ex. ``'-notnotnotswipez/MoreCompany','1.7.2', ` ``

*if you only need one set of arguments, you only need to provide ``)"`` as the closing and not ``,`` or `` ` ``*

If you receive a 404 Not Found error it most likely means that one of the arguments set does not correctly match the given mod either due to misspelling, nonexistent version, or the mod not exist at all.
                  
## Footnotes

Want a mod added? Issues? Questions? File an issue and I'll get to you soon.

This is a modified version of [Lethalize](https://github.com/KrystilizeNevaDies/Lethalize) with the option to add any mod you'd like. Full thanks to KrystilizeNevaDies!
