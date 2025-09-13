<img width="800" height="450" alt="ae2" src="https://github.com/user-attachments/assets/f87c188f-bb6e-4427-bbf6-068756d7010c" />

**About Airfield Event**

Adds an airfield event to your server! A cargo plane lands on the airfield and drops airdrops, boxes. Strong NPCs, Bradley and a patrol helicopter will protect the crates

You can also set up custom loot using the "SimpleLootTable" plugin


Features:

Easy to set up. Excellent customization options in the config

**Commands(admin only):**

afestart -  force the event to start

afestop - cause the event to end

afefast -  quick landing of a cargo plane, for testing settings

afe_addcustom -  adds a custom landing place for a cargo plane. You must stand on level ground and look in the direction where the cargo plane will move(do not forget to set in the config file "Use a custom place to land a cargo plane": true)

**Hooks:**

 void AirfieldEventStarted() // called when the event starts

{

}

void AirfieldEventEnded() // called when the event has ended

{

}

**AirfieldEvent config:**

```json
{
  "PVE mode (crates can only be looted by the player who first dealt damage to the NPC)": false,
  "Time after which the owner of the event will be deleted if he left the dome or left the server (for PVE mode)": 300,
  "Give event ownership to the owner's teammates if he is no longer the owner. Only if teammates are within the event radius (for PVE mode)": true,
  "Radius for event(for PVE mode)": 380,
  "Create a dome for PVE mode": false,
  "Dome transparency (the higher the value, the darker the dome, recommended 4)": 4,
  "Dome offset": {
    "x": 0.0,
    "y": 0.0,
    "z": 30.0
  },
  "Message when a player enters the event dome(only for PVE mode if there is a dome)": "You have entered the Airfield Event",
  "Message when the event owner leaves the event dome (only for PVE mode if there is a dome)": "Return to the event dome, otherwise after 300 seconds you will no longer be the owner of this event",
  "Do not allow other players into the event(only for PVE mode if there is a dome)": false,
  "Message when a player is ejected from the event dome(only for PVE mode if there is a dome)": "You cannot be here, you are not the owner of this event",
  "Allow admin to be in event dome (only for PVE mode if there is a dome)": true,
  "Triggering an event by timer (disable if you want to trigger the event only manually)": true,
  "Minimum time to event start(in seconds)": 3600,
  "Maximum time to event start(in seconds)": 7200,
  "Event duration(In seconds. Time is calculated from the moment the cargo is dropped by the plane at the airfield)": 3600,
  "End the event early if all crates were completely looted and all NPCs were killed(including Bradley and Heli)": true,
  "Minimum number of online players to trigger an event": 1,
  "Minimum drops amount(minimum number of cargo spawns after plane landing, should not be less than 1)": 2,
  "Maximum drops amount(maximum number of cargo spawns after plane landing, should not be less than 1, maximum 10)": 4,
  "Minimum crates amount(spawn every cargo drop)": 1,
  "Maximum crates amount(spawn every cargo drop)": 1,
  "Crate simple loot table name(plugin SimpleLootTable is required)": "",
  "Minimum number of items in a crate(plugin SimpleLootTable is required)": 0,
  "Maximum number of items in a crate(plugin SimpleLootTable is required)": 0,
  "Remove crates after being looted by a player(in seconds)": 300,
  "Extend event duration if NPCs, Heli or Bradley is attacked (if less time left, extend to set time (in seconds))": 600,
  "Crates timer(in seconds)": 900,
  "Minimum airdrops amount(spawn every cargo drop)": 1,
  "Maximum airdrops amount(spawn every cargo drop)": 1,
  "Airdrop simple loot table name(plugin SimpleLootTable is required)": "",
  "Minimum number of items in an airdrop(plugin SimpleLootTable is required)": 0,
  "Maximum number of items in an airdrop(plugin SimpleLootTable is required)": 0,
  "Minimum NPCs amount(spawn every cargo drop)": 1,
  "Maximum NPCs amount(spawn every cargo drop)": 2,
  "NPCs type(NPCs prefab, experimental setting, it is not known how the NPCs will behave) 0 - tunneldweller; 1 - underwaterdweller; 2 - excavator; 3 - full_any; 4 - lr300; 5 - mp5; 6 - pistol; 7 - shotgun; 8 - heavy; 9 - junkpile_pistol; 10 - oilrig; 11 - patrol; 12 - peacekeeper; 13 - roam; 14 - roamtethered; 15 - bandit_guard; 16 - cargo; 17 - cargo_turret_any; 18 - cargo_turret_lr300; 19 - ch47_gunner": 8,
  "NPCs health(0 - default)": 0,
  "NPCs damage multiplier": 1.0,
  "NPCs accuracy(the lower the value, the more accurate, 0 - maximum accuracy)": 2.0,
  "NPCs attack range": 75.0,
  "Radius of chasing the player(NPCs will chase the player as soon as he comes closer than the specified radius, must be no greater than the attack range)": 60.0,
  "Minimum distance to NPC damage": 75.0,
  "Message if the player attacks far away NPCs": "NPC is too far away, he doesn't take damage",
  "Forcibly immobilize an NPC": false,
  "Method of distribution of kits for NPCs(1 - sequentially, 2 - repeating, 3 - randomly)": 1,
  "List of kits for NPC(requires Kits plugin)": [
    "kit1",
    "kit2",
    "kit3"
  ],
  "Default displayName for NPC(for SimpleKillFeed/DeathNotes plugin)": "Airfield NPC",
  "List of displayNames for each NPC(for SimpleKillFeed/DeathNotes plugin)": [
    "Airfield NPC1",
    "Airfield NPC2",
    "Airfield NPC3"
  ],
  "Chance of an NPC throwing a grenade(0-100%) Only if the NPC loses sight of the player, if the player is in a vehicle, if the player is trying to search crates": 50,
  "NPC grenade damage scale": 1.0,
  "Will the NPC take damage from a collision with a car": true,
  "Event message(if empty, no message will be displayed)": "Airfield event started",
  "Event end message(if empty, no message will be displayed)": "Airfield event ended",
  "Landing message(displayed when the cargo plane has landed)": "Cargoplane landed at Airfield",
  "Patrol helicopter spawn chance (0 - 100%)": 50,
  "Call the helicopter only after activating the hackable crate": false,
  "How long the helicopter will patrol the airfield (in minutes)": 5,
  "Helicopter damage multiplier": 1.0,
  "Helicopter health": 10000.0,
  "Helicopter main rotor health": 900.0,
  "Helicopter tail rotor health": 500.0,
  "The patrol helicopter will not patrol the airfield if it has found a target": true,
  "Spawns a helicopter right on the airfield(if false, then the helicopter will arrive from afar in a few seconds)": false,
  "Helicopter patrol range": 150,
  "Event marker on the map(will spawn a marker immediately after the start of the event)": false,
  "If true, spawn the marker only after the plane lands": true,
  "Event marker name": "Airfield event",
  "Display on the marker how much time is left until the end of the event": true,
  "Event marker lifetime(in seconds)": 3600,
  "Event marker transparency(0-1)": 0.75,
  "Event marker radius": 0.5,
  "Event marker color.R(0-1)": 1.0,
  "Event marker color.G(0-1)": 0.0,
  "Event marker color.B(0-1)": 0.0,
  "Use a custom place to land a cargo plane": false,
  "Custom place position": {
    "x": 0.0,
    "y": 0.0,
    "z": 0.0
  },
  "Custom place rotation": {
    "x": 0.0,
    "y": 0.0,
    "z": 0.0
  },
  "Use custom navmesh (enable if using custom airfield and getting NPC navmesh error)": false,
  "BradleyAPC spawn chance (0 - 100%) If you are not using a custom map, correct operation of BradleyAPC is not guaranteed. Use the default airfield or a landing spot that is similar to the default airfield": 50,
  "BradleyAPC bullet damage": 7.0,
  "BradleyAPC health": 1000.0,
  "Use Notify plugin for messages": false,
  "Type notify for 'Message when a player enters the event dome'(only for Notify plugin)": 0,
  "Type notify for 'Message when the event owner leaves the event dome'(only for Notify plugin)": 0,
  "Type notify for 'Message when a player is ejected from the event dome'(only for Notify plugin)": 0,
  "Type notify for 'Message if the player attacks far away NPCs'(only for Notify plugin)": 0,
  "Type notify for 'Event message'(only for Notify plugin)": 0,
  "Type notify for 'Event end message'(only for Notify plugin)": 0,
  "Type notify for 'Landing message'(only for Notify plugin)": 0,
  "SteamID for chat message icon": 0
}
```

![ae3](https://github.com/user-attachments/assets/b96c1a14-c5f4-4ec8-91f3-c7902e13413a)
![ae4](https://github.com/user-attachments/assets/950ef42d-99e8-404d-accf-f19c1925b974)
![ae7](https://github.com/user-attachments/assets/8736eebe-3005-462a-822a-4a2aced10078)
