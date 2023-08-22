# QE2Tweaks

A collection of "tweaks" (small mods) for Quake 2 Enhanced multiplayer servers.

## New Server Variables

All tweaks implemented as server variables, and are off (0) by default and
need to be set on (1) before starting a map.

### Centerprint Frags

server variable: `sv_centerprint_frags`

Centerprint "You fragged..." and "Fragged by..." messages on killer and victim's screens.

### Game timer

server variable: `sv_game_timer`

Print a game timer in the corner of players' HUDs.

### Speedometer

server variable: `sv_speedometer`

Print a speedometer in players' HUDs.

### Target ID

server variable: `sv_target_id`

Print target ID (player name) in players' HUDs. Players can toggle enable/disable with 'id' command.

### Faster Blasters

server game variable: `g_faster_blasters`

Makes blaster shots travel faster: 5000 instead of 1500 (blaster) and 1000 (hyperblaster).

Also adjusts `sv_maxvelocity` from default of 2000 to 5000.

### Faster Rockets

server game variable: `g_faster_rockets`

Makes rockets travel faster: 1000 instead of 650.

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

## Installing

1. Download the latest `game_x64.dll` from https://github.com/ceeeKay/Q2ETweaks/releases
2. If you want to host online games for cross-play, you need to put `game_x64.dll` into
   `...\SteamLibrary\steamapps\common\Quake 2\rerelease`.

**Back up your original game_x64.dll file!** (e.g. rename to game_x64.dll.orig).

You can use Steam's "Verify integrity of game files" if you have an accident.

## Loading

1. Launch Quake II Remaster, open the console (`~`)
2. Set your Q2ETweaks server game variables as you like (see below).
3. Start a game via Multiplayer menu or appropriate console commands.
4. You can change Q2ETweaks server game variables at any time, but some don't take effect util map restart.

## Contributing

Pull Requests and filed Issues are welcomed!

Come discuss in the Quake Remastered community discord at https://quakeqe.com

### Visual Studio 2022 Build Notes

Project file is from my fork of https://github.com/id-Software/quake2-rerelease-dll
at https://github.com/ceeeKay/quake2-rerelease-dll adjusted to use C++2020 and NuGet.

VS 2022 should build out of the box without further project configuration.
