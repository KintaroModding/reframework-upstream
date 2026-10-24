# REFramework (nightly)

**This is a link, not a copy.** REFramework is made by **praydog**. This repository only lists it on openmods: it
holds no REFramework code and no REFramework files. Every download on this page comes straight from praydog's own
nightly repository on GitHub.

- Original project and source code: [praydog/REFramework](https://github.com/praydog/REFramework)
- Nightly builds, the downloads of this page: [praydog/REFramework-nightly](https://github.com/praydog/REFramework-nightly/releases)

This listing is unofficial. praydog did not make it and does not support it. If praydog wants this listing removed,
openmods takes it down: see "Report a problem" on the [openmods rules page](https://openmods.nexus/rules#report).

## What it does

REFramework is a mod framework, scripting platform and modding tool for RE Engine games. Many mods for these games
need it. Its README lists:

- A Lua scripting API and a plugin system (all games)
- VR: 6DOF VR for all games, with motion controls for Resident Evil 2, 3, 7 and Village
- First person (Resident Evil 2 and 3) and a manual flashlight (Resident Evil 2, 3 and Village)
- Free camera, scene timescale, FOV slider, vignette disabler, ultrawide and aspect ratio fixes, and a GUI hider (all
  games)
- Fixes for crashes and stutters in Resident Evil Village and Monster Hunter Rise
- Developer tools: a game object display and an object explorer

The downloads here are **nightly developer builds**: newer than the last stable release, but less tested. The stable
builds are on the [REFramework releases page](https://github.com/praydog/REFramework/releases).

## Downloads

The latest nightly release has three files:

| File | What it holds |
|---|---|
| `REFramework.zip` | REFramework itself: `dinput8.dll`, one file for all supported games |
| `VR.zip` | The VR files (OpenVR and OpenXR) and the VR scripts |
| `csharp-api.zip` | The C# API, only for plugins written in C# |

## How to install

These steps follow [REFramework's README](https://github.com/praydog/REFramework#installation).

Without VR:

1. Close the game.
2. Download `REFramework.zip` from the latest nightly release.
3. Extract only `dinput8.dll` into the game folder, next to the game's exe. Example game folder:
   `G:\SteamLibrary\steamapps\common\RESIDENT EVIL 2 BIOHAZARD RE2`
4. Start the game.

With VR:

1. Install SteamVR, unless you use OpenXR on a supported headset.
2. Put `dinput8.dll` from `REFramework.zip` into the game folder, as above.
3. Extract the whole `VR.zip` into the same game folder.
4. Help for VR problems: [VR Troubleshooting/FAQ](https://github.com/praydog/REFramework/wiki/VR-Troubleshooting)

On Linux with Proton, add this launch option to the game in Steam's properties: `WINEDLLOVERRIDES="dinput8.dll=n,b" %command%`

To update, replace the files with the ones from the newest nightly release. To remove REFramework, delete
`dinput8.dll` from the game folder; the `reframework` folder next to it holds scripts and plugins.

## How to use

- Press **Insert** in the game to open the REFramework menu.
- Lua scripts go into the `reframework\autorun\` folder in the game folder.
- The scripting documentation: [refdocs.praydog.com](https://refdocs.praydog.com)

## Compatibility

REFramework supports these games, as listed in its README: Resident Evil 2, Resident Evil 3, Resident Evil 4,
Resident Evil 7, Resident Evil Village, Resident Evil Requiem, Devil May Cry 5, Street Fighter 6, Monster Hunter Rise,
Monster Hunter Wilds, Monster Hunter Stories 3, Dragon's Dogma 2, Dead Rising Deluxe Remaster, Ghosts 'n Goblins
Resurrection, Apollo Justice: Ace Attorney Trilogy, Kunitsu-Gami: Path of the Goddess, Onimusha 2: Samurai's Destiny,
Onimusha: Way of the Sword and Mega Man Star Force Legacy Collection.

A game update can break REFramework until a new build is out. REFramework supports DirectX 11 and DirectX 12.

## Known issues

- Report bugs in REFramework to the [REFramework issues](https://github.com/praydog/REFramework/issues), not to
  openmods: only praydog's project can fix them.
- Problems with this listing itself, for example a wrong link or a wrong game: please tell openmods on its Discord
  server.

## How to build

Nothing to build here: this repository holds only `openmods.json` and `openmods.md`. praydog's GitHub Actions
workflow (`dev-release.yml`) builds the nightly releases from the REFramework source. The source code and its build
files are in [praydog/REFramework](https://github.com/praydog/REFramework).

## Credits

REFramework is made by [praydog](https://github.com/praydog) and
[its contributors](https://github.com/praydog/REFramework/graphs/contributors), under the MIT license. Its README
thanks SkacikPL, cursey, The Hitchhiker and alphaZomega for their help.

This listing: KintaroModding, for openmods. It links to REFramework only and claims no part of it.
