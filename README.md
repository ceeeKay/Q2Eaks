# Q2Eaks

A collection of "tweaks" (small mods) for the Quake II Remaster/Rerelease (aka Quake 2 Enhanced) multiplayer servers.

(pronounced "Q Tweaks")

## New Server Variables

All tweaks implemented as server variables, and are off (0) by default and
need to be set on (1) before starting a map.

### Eyecam

server variable: `sv_eyecam`

Allow eyecam (first person view) when in spectator mode. Use "attack" to cyle between free/chase/eye cam modes and "jump" to cycle between players when in chase/eye cam modes.

Note: To enter spectator mode in deathmatch mode, (CTF/TDM has its own menu option and the `observe` command), use the console command `spectator_0 1`. To re-join the game, use `spectator_0 0`. If you have split-screen players, use `spectator_1` through `spectator_7` in the same manner.

Warning: When spectating split-screen local players, `sv_eyecam` will still draw the chased player's model. This is a client engine limitation that can't be changed with a mod. Spectating network players or bots are not affected by this.

### Game timer

server variable: `sv_game_timer`

Print a game timer in the corner of players' HUDs.

### Print Frags

server variable: `sv_print_frags`

Print "You fragged..." and "Fragged by..." messages on killer's and victim's HUDs.

### Speedometer

server variable: `sv_speedometer`

Print a speedometer in players' HUDs.

### Target ID

server variable: `sv_target_id`

Print target ID (player name) in players' HUDs. Players can toggle enable/disable with 'id' command.

### Faster Projectiles

server game variable: `g_faster_projectiles`

Enables faster blaster shots, flechettes, and rockets in one cvar.

### Faster Blasters

server game variable: `g_faster_blasters`

Makes blaster shots travel faster: 5000 instead of 1500.
Makes hyperblaster shots travel faster: 2750 instead of 1000.

Also adjusts `sv_maxvelocity` from default of 2000 to 5000.

### Faster Flechettes

server game variable: `g_faster_flechettes`

Makes flechettes fired by the ETF rifle travel faster: 2750 instead of 1150.

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

### No BFG 10k

server game variable: `g_no_bfg`

Don't spawn the BFG 10k, even if `g_dm_random_items` is set.
### No Chainfist

server game variable: `g_no_chainfist`

Don't spawn the Chainfist, even if `g_dm_random_items` is set.
### No Chaingun

server game variable: `g_no_chaingun`

Don't spawn the Chaingun, even if `g_dm_random_items` is set.
### No Disruptor

server game variable: `g_no_disruptor`

Don't spawn the Disruptor, even if `g_dm_random_items` is set.
### No ETF Rifle

server game variable: `g_no_etf_rifle`

Don't spawn the ETF Rifle, even if `g_dm_random_items` is set.
### No Grenade Launcher

server game variable: `g_no_glauncher`

Don't spawn the Grenade Launcher, even if `g_dm_random_items` is set.
### No Hyperblaster

server game variable: `g_no_hyperblaster`

Don't spawn the Hyperblaster, even if `g_dm_random_items` is set.
### No Ionripper

server game variable: `g_no_ionripper`

Don't spawn the Ionripper, even if `g_dm_random_items` is set.
### No Machinegun

server game variable: `g_no_machinegun`

Don't spawn the Machinegun, even if `g_dm_random_items` is set.
### No Phalanx

server game variable: `g_no_phalanx`

Don't spawn the Phalanx, even if `g_dm_random_items` is set.
### No Plasmabeam

server game variable: `g_no_plasmabeam`

Don't spawn the Plasmabeam, even if `g_dm_random_items` is set.
### No Proximity Launcher

server game variable: `g_no_proxlauncher`

Don't spawn the Proximity Launcher, even if `g_dm_random_items` is set.
### No Railgun

server game variable: `g_no_railgun`

Don't spawn the Railgun, even if `g_dm_random_items` is set.
### No Rocket Launcher

server game variable: `g_no_rlauncher`

Don't spawn the Rocket Launcher, even if `g_dm_random_items` is set.
### No Shotgun

server game variable: `g_no_shotgun`

Don't spawn the Shotgun, even if `g_dm_random_items` is set.
### No Super Shotgun

server game variable: `g_no_sshotgun`

Don't spawn the Super Shotgun, even if `g_dm_random_items` is set.

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

1. Download the latest `game_x64.dll` from https://github.com/ceeeKay/Q2Eaks/releases
2. If you want to host online games for cross-play, you need to put `game_x64.dll` into
   `...\SteamLibrary\steamapps\common\Quake 2\rerelease`.

**Back up your original game_x64.dll file!** (e.g. rename to game_x64.dll.orig).

You can use Steam's "Verify integrity of game files" if you have an accident.

## Loading

1. Launch Quake II Remaster, open the console (`~`)
2. Set your Q2Eaks server game variables as you like (see below).
3. Start a game via Multiplayer menu or appropriate console commands.
4. You can change Q2Eaks server game variables at any time, but some don't take effect util map restart.

## Contributing

Pull Requests and filed Issues are welcomed!

Come discuss in the Quake Remastered community discord at https://quakeqe.com

### Visual Studio 2022 Build Notes

Project file is from my fork of https://github.com/id-Software/quake2-rerelease-dll
at https://github.com/ceeeKay/quake2-rerelease-dll adjusted to use C++2020 and NuGet.

VS 2022 should build out of the box without further project configuration.
