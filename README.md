<img width="800" height="450" alt="ae2" src="https://github.com/user-attachments/assets/f87c188f-bb6e-4427-bbf6-068756d7010c" />

About Airfield Event

Adds an airfield event to your server! A cargo plane lands on the airfield and drops airdrops, boxes. Strong NPCs, Bradley and a patrol helicopter will protect the crates

You can also set up custom loot using the "SimpleLootTable" plugin


Features:

Easy to set up. Excellent customization options in the config

Commands(admin only):

afestart -  force the event to start

afestop - cause the event to end

afefast -  quick landing of a cargo plane, for testing settings

afe_addcustom -  adds a custom landing place for a cargo plane. You must stand on level ground and look in the direction where the cargo plane will move(do not forget to set in the config file "Use a custom place to land a cargo plane": true)

Hooks:

 

void AirfieldEventStarted() // called when the event starts

{

}

void AirfieldEventEnded() // called when the event has ended

{

} 
![ae3](https://github.com/user-attachments/assets/b96c1a14-c5f4-4ec8-91f3-c7902e13413a)
