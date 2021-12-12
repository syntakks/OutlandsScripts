# OutlandsScripts
These are razor scripts for Outlands Ultima Online

## Smithy
This set of scripts will help you quickly and efficiently level up your Blacksmith skill.  

By using multiple scripts you can increase the speed of crafting as you aren't constantly 'waiting for gump' when drilling down into the menu during each loop iteration. Instead we can lean on "Make last" as much as possible to speed up crafting and keep the client running smoothly.  

I set this up to be used in Horseshoe Bay forge as you can restock directly from your bank there. This makes it a very safe approach as you'll only ever have 100ish ingots on you at a time. (Note: There is some "ingot drift" ;) as you recycle items. If you are crafting for a VERY long time you may see your total ingot count in backpack be higher than desired. Let me know if it's an issue for you.)  

This will auto recycle all items during the restock phase.  

It also includes a world save check that will pause crafting until save is over. This helps prevent your script from getting into a bad state that could leave it (and your gains) hanging.

### Setup
Drag the entire folder into your razor scripts folder.  
This will require some setup...  

1. This assumes you have access to your bank. I use Horseshoe Bay Forge as you can reach the bank.
    - MAKE SURE YOUR BANK BOX IS OPEN BEFORE RUNNING.
3. It's expecting a counter named "ingots".
4. It's expecting a restock agent of slot 1 (restock 1) I set mine for 1 hammer and 100 iron ingots. I put my hammers in a pouch and the iron ingots can be on first level of bank box. (NOTE: You will likely need to remove any other hued ingots from your bank box as the restock agent will grab them by mistake.)
5. Your Recycle setting in the crafting menu is "Recycle Entire Backpack"
    - DANGER!!! MAKE SURE YOU DON'T HAVE ANYTHING IN YOUR BAG YOU'LL MISS!!! YOU SHOULD ONLY HAVE HAMMERS/ INGOTS/ AND WHATEVER YOU ARE CRAFTING AT THE TIME IN YOUR BACKPACK

### Adding a Counter for your ingots
- Razor -> Display/Counters -> Counters
    - Add
        - Target: (Target a stack of iron ingots)
        - Name: ingots
        - Format: ingots
        - Click "OK"
    - Find the newly created "ingots (ingots)" item in the list and make sure the box is checked to activate the variable.
    - SAVE YOUR PROFILE

### Entry Point
- Blacksmith.razor
