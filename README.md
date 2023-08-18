# QE2Tweaks

A collection of "tweaks" (small mods) for Quake 2 Enhanced multiplayer servers.

## New Server Variables

All tweaks implemented as server game variables, and are off (0) by default and
need to be set on (1) before starting a map.

### Faster Blasters

server game variable: `g_faster_blasters`

Makes blaster shots travel faster: 5000 instead of 1500 (blaster) and 1000 (hyperblaster)

Also adjusts `sv_maxvelocity` from default of 2000 to 5000.

### Spawn With Chainfist

server game variable: `g_spawn_with_chainfist`

Everybody needs a good melee weapon. Give players a chainfist when they spawn!

### Spawn With Shotgun

server game variable: `g_spawn_with_shotgun`

Give newly-spawned players a fighting chance. Give them a shotgun when they spawn!

### Rockets Only

server game variable: `g_rockets_only`

All rockets, all the time.

## Visual Studio 2022 Build Notes

- Sources originally from https://github.com/id-Software/quake2-rerelease-dll
- No preprocessor defines have been added to what was already in game.soln
- Installed jsoncpp via Project->NuGet instead of vcpkg as suggested by id
    - Needed package jsoncpp-vc140-static-32_64
      (jsoncpp in NuGet is a 2014 sourceforge project!)
- Switched language standard for Debug and Release from C++2017 to C++2020
    - Originally I'd left it at C++2017 and installed fmt from NuGet but build
      spit out a bunch of errors related to formatting; went away with C++2020

## TO DO List

(Pull requests are welcomed!)

- Centerprint "you fragged x" messages
- Centerprint "fragged by x with y health z armor"
- Centerprint list of enabled tweaks on server in welcome message
- Game timer in HUD!
