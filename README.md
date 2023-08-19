# QE2Tweaks

A collection of "tweaks" (small mods) for Quake 2 Enhanced multiplayer servers.

## Installing

1. Download the latest `game_x64.dll` from https://github.com/ceeeKay/Q2ETweaks/releases
2. Put `game_x64.dll` into a mod-specific subdirectory (e.g. `q2etweaks`) in your
   `%USERPROFILE%\Saved Games\Nightdive Studios\Quake II` directory.
3. If you want to host online games, you may instead need to put `game_x64.dll` into
   `...\SteamLibrary\steamapps\common\Quake 2\rerelease` instead.
   BACK UP YOUR ORIGINAL game_x64.dll FILE!!! (e.g. rename to game_x64.dll.orig)
   You can use Steam's "check files" if you have an accident, though.

## Loading

1. Launch Quake II Remaster, open the console (`~`)
2. If you used a mod-specific directory, type `game q2etweaks` (or whatever you called it).
2. Set your Q2ETweaks server game variables as you like (see below).
3. Start a game via Multiplayer menu, `map` command, etc.
4. You can change Q2ETweaks server game variables at any time, but some don't take effect util map restart.

## New Server Game Variables

All tweaks implemented as server game variables, and are off (0) by default and
need to be set on (1) before starting a map.

### Faster Blasters

server game variable: `g_faster_blasters`

Makes blaster shots travel faster: 5000 instead of 1500 (blaster) and 1000 (hyperblaster).

Also adjusts `sv_maxvelocity` from default of 2000 to 5000.

### No Self Damage

server game variable: `g_no_self_damage`

Doesn't allow you to hurt yourself.

### Start With Chainfist

server game variable: `g_start_with_chainfist`

Everybody needs a good melee weapon. Give players a chainfist when they spawn!

### Start With Shotgun

server game variable: `g_start_with_shotgun`

Give newly-spawned players a fighting chance. Give them a shotgun and 10 shells when they spawn!

### Only Weapon

server game variable: `g_only_weapon`

Disables weapon and ammo spawns and gives this player the specified weapon with infinite ammo.

valid values: One weapon name in quotes, e.g. `"Chaingun"` or `"Rocket Launcher"` or `""` to disable mode.

    - `"Grapple"`
    - `"Blaster"`
    - `"Chainfist"`
    - `"Shotgun"`
    - `"Super Shotgun"`
    - `"Machinegun"`
    - `"ETF Rifle"`
    - `"Chaingun"`
    - `"Grenades"`
    - `"Grenade Launcher"`
    - `"Prox Launcher"`
    - `"Rocket Launcher"`
    - `"HyperBlaster"`
    - `"Ionripper"`
    - `"Plasma Beam"`
    - `"Railgun"`
    - `"Phalanx"`
    - `"BFG10K"`
    - `"Disruptor"`

## Developers

Pull requests are welcomed!

### Visual Studio 2022 Build Notes

- Sources originally from https://github.com/id-Software/quake2-rerelease-dll
- No preprocessor defines have been added to what was already in game.soln
- Installed jsoncpp via Project->NuGet instead of vcpkg as suggested by id
    - Needed package jsoncpp-vc140-static-32_64
      (jsoncpp in NuGet is a 2014 sourceforge project!)
- Switched language standard for Debug and Release from C++2017 to C++2020
    - Originally I'd left it at C++2017 and installed fmt from NuGet but build
      spit out a bunch of errors related to formatting; went away with C++2020
