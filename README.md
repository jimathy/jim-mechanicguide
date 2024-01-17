# Mechanic Guide
Read this before opening a ticket. please GOD, read it.

## Multi-Framework Support
My actual "live" support of this is very limited
With the use of my free script `jim_bridge` the script is now able to be used fully on:
- qb-core
- qbx-core
- ox_core
- ex_extended - (with the use of `ox_lib`, `ox_target` and `ox_inventory`)

The ones we can personally help with are qb-core and qbx-core, the others are just compatability as of now
Most likely `es_extended` will have many options that I don't know about, so don't expect anything special from it

------------------
## Performance Items

- These all work very similarly
- Stand next to the vehicle and use these items.
	- If the upgrade can not be put on the car, you will get a notification telling you so.
	- If it can, you will begin adding it to the vehicle.
- If you have an upgraded part already in the vehicle, adding a different level item will remove the previous upgrade from the car and place it in your inventory.
- The mechanic's `toolbox` item is used to remove these upgrades and set them back to stock.
- The items classed as performance items include:
```
- car_armor - "Vehicle Armor"
- brakes1 - "Tier 1 Brakes"
- brakes2 - "Tier 2 Brakes"
- brakes3 - "Tier 3 Brakes"

- engine1 - "Tier 1 Engine"
- engine2 - "Tier 2 Engine"
- engine3 - "Tier 3 Engine"
- engine4 - "Tier 4 Engine"
- engine5 - "Tier 5 Engine"

- suspension1 - "Tier 1 Suspension"
- suspension2 - "Tier 2 Suspension"
- suspension3 - "Tier 3 Suspension"
- suspension4 - "Tier 4 Suspension"
- suspension5 - "Tier 5 Suspension"

- transmission1 - "Tier 1 Transmission"
- transmission2 - "Tier 2 Transmission"
- transmission3 - "Tier 3 Transmission"
- transmission4 - "Tier 4 Transmission"

- drifttires - "Drift Tires"
- bprooftires - "Bulletproof Tires"

- turbo - "Supercharger Turbo"
- headlights - "Xenon Headlights"
```
------------------
## Cosmetic Items

- These all work very similarly
- Stand next to or get in the vehicle and use these items, if options are available for the car this will bring up a menu that shows a list of possible cosmetics
- To reset back to default, use another of the same item, as you are putting the "stock" on
- The items classed as costmetic items include:
```
- bumper - "Vehicle Bumper"
- exhaust - "Vehicle Exhaust"
- externals - "Exterior Cosmetics"
- hood - "Vehicle Hood"
- horn - "Custom Vehicle Horn"
- internals - "Internal Cosmetics"
- livery - "Livery Roll"
- paintcan - "Vehicle Spray Can"
- customplate - "Customized Plates"
- rims - "Custom Wheel Rims"
- roof - "Vehicle Roof"
- rollcage - "Roll Cage"
- seat - "Seat Cosmetics"
- skirts - "Vehicle Skirts"
- spoiler - "Vehicle Spoiler"
- tires - "Drift Smoke Tires"
- tint_supplies - "Tint Supplies"
```

------------------
## Extra Damage Items

- These items are for the extra damages included in jim-mechanic
- The upgrades improve durability for each part and lower the chance of the damage effects kicking in
- Oil Pump
	- "Your engine is overheating" - Slowly damages your engine's health
- Drive Shaft
	- "The steering feels wrong.." - Affects steering temporarily
- Spark Plugs
	- "The engine has stalled" - The car will stop temporarily
- Car Battery
	- "Theres something affecting your lights.." - Makes the lights in your car flicker on and off
- Fuel Tank
	- "You hear something dripping.." - Lowers fuel level faster

These can be repaired by a mechanic with mechanic tools item

------------------
## Mechanic Items

- This is the list of rest of the items that come with this script
```
- toolbox - "Toolbox" - This is the scripts main way to control the performance modifications in a car.
- mechanic_tools - "Mechanic tools" - This is the script's main repair tools
- nos - "NOS Bottle" - My scripts Nitrous Canister
- noscan - "Empty NOS Bottle" - Empty Nitrous Canister
- ducttape - "Duct Tape" - A configurable repair item
- mechboard - "Mechanic Sheet" - Given as a list of changes when completing a preview of the vehicle
- underglow_controller - "Neon Controller"-  Controls underglow style and colour + xenon headlight colours
- sparetire - For repairing wheels while in the toolbox menu
- sparkplugs - For repairs
- carbattery - For repairs
- axleparts - For repairs
- newoil - For repairs
```

------------------
## Toolbox / Check_tunes.lua

- This is all about the item "toolbox" this item
- The toolbox is only usable by mechanics, if `Config.System.ItemRequiresJob` is enabled
- This item can only be used **OUTSIDE** of a vehicle.
- This displays information about the vehicle's currently installed peformance modifications
	- It will attempt to grab information from `vehicles.lua` to display vehicle names and the value, it does this by searching for a matching "model hash".
	- It will list the names and levels of each installed modification, and even if they can be installed on the vehicle at all.
	- If there is an installed item you can select it in the shown menu, then you will be the given a confirmation option to remove it. Doing so will set it back to stock and place the specific upgrade in your inventory.
- At the bottom of this menu is a quick shortcut to what is displayed by the `/checkmods` command, which displays a simple list of all possible cosmetic mods that can applied to the current vehicle

------------------
## Mechanic_Tools / repair.lua

- This menu is activated by the item "mechanic_tools"
- Note: It tires to get all the information BEFORE the progressbars so if you don't get any animations or menu, theres an error.
- It will start with an animated check of the engine and body for damage and then get a list what it found.
- How this menu functions is defined by the config options
	- `FreeRepair = true` will allow you to repair the car with no requirements
	- `StashRepair = true` will place a stash location for the mechanics to place their materials so they can be pulled from there and used when repairing

------------------
## Nitrous / nos.lua

- Nitrous relies on three columns in the database `player_vehicles`
	- `hasnitro` - Wether the vehicle has Nitrous in or not
	- `noslevel` - The amount of nos that is in the vehicle (max 100)
	- `noscolour` - The RGB colours of the NOS Purge
- A vehicle's NOS is saved between server restarts for player owned vehicles
- To add NOS to a vehicle you will first need `Turbo` to be installed on the vehicle.
	- Then you will need a NOS cannister (`nos`) and to use it outside of the vehicle. This will start a skill check to install it.
- The NOS consists of two modes, these can be switched with `Left Ctrl`
	- Boost Mode
	- Purge Mode
- When in Boost Mode you can control the power with `Page Down` or `Page Up` and is activated with `Left Shift`
	- Level 1 - Standard NOS Boost
	- Level 2 - Increased acceleration + Boost
	- Level 3 - Greater acceleration + Boost
	- Boosting for too long will damage the engine and the greater the boost level the more damage that will be done
- When in Purge Mode, you will be able to activate purge spray's from your vehicle
	- `Page Down` or `Page Up` in this mode controls the the of spray (purely cosmetic)
	- Purging after boosting speeds up the cooldown and allows you to boost again sooner
- When the NOS is used up in a vehicle, the driver will receive an empty nos can, which can be refilled/crafted to make it full again.
- If you put in a new can before you run out of NOS in the vehicle you will also recieve an empty can.
- NOS can be installed on almost any vehicle
	- If it allows you to install `Turbo` you can install NOS
- The `manualPurgeLoc` table at the bottom of the file is the Manually placed Purge locations on vehicles
	- Currently I added Super cars beacuse their default placement was all over the place
	- Feel free to edit/add any and share these with others.
```
{ xOffset, yOffset, zOffset, xRotation, yRotation, zRotation },
```
------------------
## manualrepair.lua / Non-Mechanic repair benches

- This file creates repair benches that can **ONLY** be used when there isn't any mechanics on duty.
- The benches are added to set locations at the top of this file
- They are activated by targetting with `qb-target` while in a car
- How the config.lua options are set will determine how the menu functions
	- `Config.ManualRepairs.ManualRepairCost` - This is the **SET** amount a vehicle repair will cost
	- `Config.ManualRepairs.ManualRepairBased` - when `true` this overrides the above and grabs the value of the vehicle from vehicles.lua
	- `Config.ManualRepairs.ManualRepairPercent` - The percentage of the vehicle value to be used. Default is `5`
	- `Config.ManualRepairs.repairEngine` - `true` repair engine + body, `false` repair body only
	- `Config.ManualRepairs.repairExtras` - `true` will attempt to repair extra damages
	- `Config.ManualRepairs.dutyMessage` - The excuse for why people can't repair while mechanics are on duty.
	- `Config.ManualRepairs.repairAnimate` - Animates the repair, better than a progress bar
	- `Config.ManualRepairs.repairSpeed` - How fast each repair step takes

------------------
## police.lua / Emergency Repair Benches

- This file creates repair/customisation benches for police
	- These are intended to be for Police/EMS players, but other job roles can be added easily
- It adds a bench to the set locations where they can repair and change a cosmetics and performance.
- This is activated by using your target script.
- What can be accessed is handled in the config under `Emergency`

------------------
## preview.lua - `/preview`

- The preview system is shown by typing `/preview`
	- Shows a menu with all possible cosmetic changes for the current vehicle
	- There is a `hardCam` config option to lock the camera, which is moveable with the camera button at the top of each cosmetic menu
	- When complete, press "Stop Previewing" or exit the vehicle and the preview will be classed as finished
	- This system locks the vehicle in place
	- As per exploit protection, is attempts to change the vehicle plate so people can't save their changes
		- This is controlled by `Config.Overrides.disablePreviewPlate`
		- Some people need to remove this as some persistant vehicle scripts cause vehicles to duplicate.
- When exiting the vehicle, depending on the set config options you will recieve a list of the changes made
	- `Config.Discord.DiscordPreview` will attempt to print the list to a specified discord channel
	- `Config.Previews.PreviewPhone = true` will attempt to use the set phone system to send the player a phone email with the list
	- `Config.Previews.PreviewPhone = false` will spawn a item `mechboard` which when used will show the list of changes on screen
- Note: Spawning the `mechboard` item, trying to use it and then asking me why it's telling you not to spawn it shows you haven't read this-

#### To create a discord webhook follow the following steps:
- Click the gear icon (Edit Channel) of the channel you want to post to.
- Click Webhooks in the left menu.
- Click the Create Webhook button.
- Enter a Name of your choice.
- Click the Copy button of the Webhook URL.
- Click the Save button.
- Paste the Webhook URL in the script you want to use it.

## Car Lifts
The script features built in synced carlift for your vehicles to be placed on
- These aren't required for edits, but change the animation for RP
- These are toggleable in the config if you wish to use another carlift script
- All locations come preset with carlifts in some form
	- Some have replacement carlifts
	- Some have new carlifts
	- Some make use of the carlifts already in a MLO

For example:
```lua
carLift = {
	{ coords = vec4(-201.85, -1319.65, 31.3, 19.36), useMLOLift = true },
	{ coords = vec4(-221.27, -1318.71, 31.3, 352.67), useMLOLift = true },
},
```
These locations make use of CarLifts already in place at Gabz Alta Street MLO, this is shown with the extra `use = true` or `useMLOLift = true`

-----------------
## Configuration

There is little snippets of information on each line for these, but this is a more detailed list of information

### Config.Lan
- This script has a built in locale system
- You will need to then set the langauge with Config.Lan. By default it's set to english `"en"`

-----------------
## System

### Debug
- This enables a debug mode, this will enable the debug boxes around locations to show you where they are set and where they are moving to.
- This also enables Debug Messages in the F8 Menu and server console to help me and you with debugging issues

### Menu
- This controls which menu will be used
	- "qb" for `qb-menu/qbx-menu` or `jixel-menu`
	- "ox" for `ox_lib`
	- "gta" for `warmenu`

### Notify
- This controls which notification system is to be called
	- "qb" - `qb-core/qbx-core`
	- "ox" - `ox_lib`
	- "esx"	- `es_extended`
	- "gta" - `Built in GTA notifications`
	- "okok" - `okok-notify`

### ProgressBar
- This Controls what progressbar will be shown when using the script
	- "qb" - `qb-core/qbx-core` Default
	- "ox" - `ox_lib` default
	- "gta" - `gta` default
	- "esx" - `esx_progressbar` default

### distkph
- This is only used when the odometer is used, toolbox menu and the onscreen milage display.
	- `true` = distance in Kilometers
	- `false` = distance in Miles

-----------------
## General

### JimShops
- Set this to true if you are using my free qb-shops alternative, [jim-shops](https://github.com/jimathy/jim-shops)
- Set to false to use default inventory style shops

### showClockInTill
- Toggle this to enable showing toggling duty option at cash registers

### showBossMenuTill
- Toggle this to enable showing the BossMenu option at cash registers

-----------------
## Main

### craftCam
- This enables alot the use of custom cameras all around the script
	- Its in the crafting location as this is what it was based on
- It adds custom cameras for extra immersion when crafting or editing vehicles

### MultiCraft
- This enables multicrafting
- Using this allows you to make multiples of crafting recipes faster

### MultiCraftAmounts
- This how many multiples will be offered when crafting

### showItemBox
- This was added for people with customised inventories
- qb-inventory by default(for some reason) doesn't include the itembox event when triggered (use, add, remove)
- you need to add them your self after, but some put them in to be automated
- Basically this toggles showing these boxes or not, to stop doubling them up

-----------------
## Main

### isVehicleOwned
- This checks the database for if the vehicle is player owned or not.
- If you only want customisations to be made to player owned vehicles, enable this.

### ItemRequiresJob
- This locks the mechanics performance items and cosmetic items behind a job role.
- The jobs are set lower in the config.lua file at `Config.JobRoles`

### JobLocationRequired
- This makes it so items become location locked. You will only be able to work if you are in a polyzone for a job's location (items will only work in a set mechanic shop)
- If this is disabled items can be used anywhere.

### LocationBlips
- This enables your locations blips even if you disable location requirements

### CostmeticJob
- This enables or disables a job requirement on cosmetic items.
- This ignores `Config.System.ItemRequiresJob`

### JobRoles
- This is the list of jobs that can use items in the script if `ItemRequiresJob` is enabled

## Overrides

### CosmeticItemRemoval
- This makes cosmetic items have unlimited uses
- Disabling this makes items remove from inventory after use.

### updateServerDelay
- This is to help stop overloading of server databases when many changes are happening between players
- It adds a specified cooldown in seconds between changes which resets every time a change is made
- It doesn't save the current vehicle's mods until the cooldown is done

### ChameleonPaints
- This adds makes the console exclusive chameleon paints appear when changing vehicle paints
- They are loaded in the script by default and to fully remove, you need to remove the loaded files in the data and stream folders

### DoorAnimations
- This enables or disables door opening and closing animations whne editing vehicles or viewing modifications

### disableNos
- Enabling this disables ALL Nirtous boosting related effects controlled by `jim-mechanic`
- Do this if you don't want NOS in your server/have another script controlling it

### showItemBox
- Enabling this shows the "item boxes" for using, adding and removing items
- Inventory scripts like ox_lib don't use this
- But some inventories do this automatically so this isn't needed and may show duplicate boxes

### disablePreviewPlate
- Enabling this `disables` the changing of the plates when previewing
- There is added in exploit protection as some users were managing to save their vehicles with previewed mods on
- Some persistant vehicle scripts counter act this and duplicate the vehicle.
- Disabling stops this, but also removes the exploit protection
- I am attempting to work with other devs to make this completely usable.

### disableToolboxProp
- This is a simple toggle to remove the toolbox when using the `toolbox` prop when using the `toolbox` item
- For some reason it wont load for some people so this stops the script from hanging when loading it

### saveOnExit
- This is a toggle to enable attempting to save the current vehicle the player is exiting to the database
- It doesn't save if your garage removes the vehicle "too fast" or instantly
- This isn't on by default as it SHOULD save the vehicle while driving but adds an extra chance for it

## Crafting

### craftCam
- This enables customs cameras ALL through the script, when modifying vehicles, when crafting
- This is a toggle because some users complained of motion sickness

### MultiCraft
- This enables the basic MultiCrafting features when crafting
- It allows users to make multiples of items when crafting

### MutliCraftAmounts
- This is the multiples of amounts you can craft when multicrafting

## Harness

### JobOnly
- This enables the harness item to only be put on the vehicles by the job roles specified in `Config.Main.JobRoles`
- Disabling this makes it so anyone can add a harness to a vehicle

### HarnessControl
- This enables harness and seatbelt controls inside jim-mechanic
- Only use this if you have followed the install instructions correctly

### seatbeltEasyLeave
- This enables the ability to leave a vehicle while the `seatbelt` is attached
- Disabling locks you in the vehicle until you unbuckle it

### harmessEasyLeave
- This enables the ability to leave a vehicle while the `harness` is attached
- Disabling locks you in the vehicle until you unbuckle it

### progOn
- This adds a progress bar for players when buckling their `harness`
- Disabling makes it instant

### progOff
- This adds a progress bar for players when un-buckling their `harness`
- Disabling makes it instant

### seatbeltNotify
- When enabled shows a notification when buckling and unbuckling the seatbelt and harness

### timeOn
- How long it takes for the harness to be attached
	- Default = `3000`
### timeOff
- How long it takes for the harness to be attached
	- Default = `2000`

### crashKill
- Enable this to make it more likely when a player is ejected when crashing to be gravely injured


## vehFailure

### damages
- This enables `jim-mechanic` control of vehicle extra damages in the script
- Enable this if you don't use `qb-vehiclefailure`

### repairKits
- This takes control of `advancedrepairkit` and `repairkit` if you don't use either `qb-mechanicjob` or `qb-vehiclefailure`
- On frameworks that didn't use thse items, they can be added manually after enabling this

### fixCommand
- This takes control of the `/fix` command after removing `qb-mechanicjob` and `qb-vehiclefailure`
- This fixes the vehicle's extra damages aswell if enabled
- Don't use this if you haven't removed the previous `/fix` command

### PreventRoll
- This was added to take over `qb-vehiclefailures` ability to prevent vehicles from being flipped over by pressing right or left while still in the drivers seat

## CarLifts

### Enable
- Simply enables the use of carlifts in the script

### Sound
- Enables the carlift sounds when lifting up or moving down
- Disabling makes them silent

### CarLiftModelReplace
- This is list of possible carlift models that can be replaced in MLO's

### CarLiftUse
- This is the list of usable carlife models in that a preadded to MLO's
- It contains the offsets for the targets where you can control the lift

## Repairs

### FreeRepair
- Enabling this makes all repairs by mechanic not require any materials to repair, so they repairs are free.

### StashRepair
- This enables grabbing materials for repairs from their current jobs mechanics stash, these stashes are accessible at set loications in the locations.lua.
- If disabled materials will be taken from the players inventory.

### ExtraDamages
- This enables the extra damages throughout the script
- (they are explained above)

### EffectLevels
- These are the percent of damage to each part that is needed before they have a chance of triggering

### Parts
- This is a list of items that are needed to repair the vehicles
- You can only set one item per repair but the `MAX` cost is set next to it
- If you have 1% of damages as an example, you will only need 1 item
- If you have 100% of damages, you will need the full amount

## Previews

### hardCam
- This enables custom set cameras for previewing
- Pressing the camera button in the menu will change the angle of it
- Stopping the preview will return it to normal

### PreviewPhone
- If this is enabled, it will attempt to send an email to your phone of the changed mods during a preview
	- The current supported phones as of writing this are:
		- "gks"
		- "qs"
		- "qb"
		- "roadphone"
- If this is disabled then the user will recieve a clipboard `mechboard` item with the list of changes

### PreviewJob
- This makes it so a job role set in `Config.Main.JobRoles` is required to use the /preview command

### PreviewLocation
- This makes it so you need to be a job location's polyzone to use the /preview command

### PhoneMail
- If PreviewPhone is true, change this to choose the correct phone system
	- "qb" = use qb-phone for emails
	- "gks" = use gks-phone for emails
	- "qs" = use qs-smartphone for emails
	- "roadphone" = use roadphone for emails

### PhoneItems
- This is list of phone items that are checked on the user
- If not found the script will default to giving the player a clipboard instead

## StoreCraft

### Crafting
- This simply enables crafting in the script for mechanics at targets set in locations.lua

### StashCraft
- This enables crafting from the set stash in each location for job roles

### Stores
- This enables the use of Stores to buy mechanic related items

## Odometer

### ShowOdo
- This enables the use of the odometer hud in the script
- Players can toggle this theirselves with `/showodo`

### OdoLocation
- This determines where the location of the Odometer will be for your players
- List of possible options:
```
	"left"
	"right"
	"top"
	"top-left"
	"top-right"
	"bottom"
	"bottom-left"
	"bottom-right"
```

### OdoShowIcons
- As of v2.9 there is now a "dashboard" feature that shows icons representing the damage
- Toggling this enables or completely disables these

### OdoAlwaysShowIcons
- Enable this to show the icons ALL THE TIME, even when parts are not damaged

### ShowToAll
- Enabling this allows all passengers in the car to see the cars odometer hud

### OdoIconsToShow
- Fine control over which icons will show
- Setting any of these to false will make the icon never be shown

## Emergency

### requireDutyCheck
- When enabled you won't be able to repair at an Emergency Repair bench if there are any people with the mechanics online
- When disabled, the repair option will always be there

### Jobs
- These are the jobs and their grades that can that the bench

### LockEmergency
- This makes it so you can only modify vehicles with the class "emergency" in their meta data

### Locations
- The locations where the benches will spawn, they are currently defaulted to GABZ MPRD and PillBox

### CosmeticsTable
- The list of items that will show in the emergency bench menu's

### PerformanceTable
- The list of perfromance settigns that show in the emergency bench menu's

## ManualRepairs

### ManualRepairCost
- This is the amount to charge people for a repair at the manual repair benches.
- The default is `5000` but I recommend setting this to a high amount for your server
- The intention of the mechanic script is to provide RP to the server, there is no RP in using a prop instead of talking to someone.

### ManualRepairCostBased
- Set this to true if you want the cost to ALWAYS be the amount set at "ManualRepairCost"
- Set this to false if you want it to "ManualRepairCost" to be the max and cost is calculated by damage

### ManualRepairBased
- This overrides the previous setting `ManualRepairCost`
- Setting this to true sets the price of the repair to be based on the cost of the vehicle in your vehicles.lua

### ManualRepairPercent
- This is only used if `ManualRepairBased` is enabled.
- This needs to be set to the percentage of the value of the vehicle you want to charge people per repair
- For example:
	- 5% of a $10,000 car would be $500 per repair
	- 10% of a $200,000 car would be $20,000 per repair

### repairEngine
- When enabled this will include engine repairs in the Repair Bench process
- If disabled it will only attempt to repair the body

### repairExtras
- Enabling this will include Extra Damages repair that come from `qb-mechanicjob`
- if `qb-mechanicjob` is not found but this is true, it will skip over these extras

### dutyMessage
- I left his here as people were giving me different reasons for why they wanted the repair benches in the script
- I'm leaving this up to them for how they want to phrase their notification.
- Default: `"There is a Mechanic on duty!"`

### repairAnimate
- When `true` this will add a small animatied sequence to the repair of the vehicle, instead of people just sitting and watching a progressbar

### repairSpeed
- The time between each task while using repairAnimate. `1500` Seems to be a reasonable time for each one

## antiLag

### antiLagDis
- This is the distance in units that players will hear the antilag noises

## maxAudio
- The max volume of the antilag audio clips (max setting is 1.0)

## NOS

### JobOnly
- Only allow job roles to change NOS

### NosRefillCharge
- This only is used at NOS Refill stations, if you have added them to your locations in locations.lua
- The amount in dollars required for a player to refill an Empty NOS can.
- Note: There is also the option of a mechanic crafting them for you.
- The default is `1000`

### NosBoostPower
- Fine controls over the accelleration power for each boost level
- Shown as a table for optimization
```lua
NosBoostPower = {
	20.0, -- Level 1
	35.0, -- Level 2
	50.0, -- Level 3
},
```
- These values seem a good default, but may need adjusting if you have customised vehicle meta files

### NitrousUseRate
- This is how fast the nitrous drains
- Default - `0.3`
- Boost Level 1 changes this number minus half of this number (0.4 - (0.4 / 2))
- Boost Level 3 changes this number plus half of this number (0.4 + (0.4 / 2))

### NitrousCoolDown
- This is how long a player has to wait before the boost works again
- Default - `7`
- 7 seconds seems to be enough time for it to cooldown, setting this too low allows some servers players to travel at insane speeds after spamming the button
- Set to `0` to disable this

### CooldownConfirm
- Simply, this will play a confirmation beep when cooldown is complete
- Made is toggleable in the config in case people didn't like it

### nosDamage
- This enables NOS causing damage to engine while boosting
- Boosting for too long will play sound alerts and damage the Engine.

### boostExplode
- If boosting too long at Boost Level 3 the NOS tank will explode.
- Will cause damage to the vehicle and cause a fire.
- This will remove remaining NOS from the vehicle and not give an empty tank

### EnableFlame
- `true` adds exhaut flame effects while boosting
### EnableTrails
- `true` adds taillight effects while boosting
### EnableScreen
- `true` True adds screen effects while boosting

### FlameDis
- This is the distance check on the visuals for flame effects from nos
- As of v3.3 this currently only applies to anti lag effects

### skillcheck
- When adding Nos to a vehicle there are three skillcheck script options available
	- "qb-skillbar"
	- "qb-lock"
	- "ps-ui"

### explosiveFail
- When `true` there is a `1 in 10` chance for when you fail the skillcheck for the tank to explode in the vehicle.
- Doesn't cause much damage, but fill push the player and vehicle back

### explosiveFailJob
- When `false` mecahnics WILL **NOT** cause explosions on failing the skill check
- When `true` mechanics **CAN** cause explosions on failing the skill check

### HandlingChange
- This helps change handling but is not recommended as some users reported this never resetting to defaults when boosting is finished.

## Discord

### DiscordPreview
- This enables or disables the Discord Reports for the `/preview` command
- When `true` this system will send the report to a specified discord channel using a webhook
- When `false` this system will be ignored/disabled

### DiscordDefault
- So people seem to be confused by this one.
- This is the default channel that will be used, no matter where you are.
- If you haven't set specific discord channels in a location, it **should** "default" to this link.

### DiscordColour
- You don't need to touch this, but this is the default colour of the post in the discord channel
- The default colour is `16753920` - this is a "decimal" colour number, which is a yellow colour.

### Duct tape:
- Many people forgot these are a thing while begging me to add repair benches..
- The Ducttape item is intended to be an alternative and customisable version of repairkits
- They are customisable and let even set the max amount of how much the parts get repaired

### Config.DuctTape.DuctSimpleMode
- This sets the duct tape item into simple mode, repairing to the amount every time
- `true` makes duct tape set every use to the amount set below at `MaxDuctEngine`
- `false` uses the `DuctAmountEngine` value to repair the by vehicle each use

### Config.DuctTape.MaxDuctEngine
- This is the MAX value the engine can be repaired by, leave this below 1000(100%) so people still need to use mechanic's
- If `DuctSimpleMode` is `true` will set it straight to this amount
- If `DuctSimpleMode` is `false` it will be the max amount it can be repaired to
- Default = `450.0` - (45% health)

### Config.DuctAmountEngine
- The amount to repair your engine by each ducttape item use
- This is only used if `DuctSimpleMode` is `false`
- Default = `100.0` - (10% Health)

### Config.DuctTape.DuctTapeBody
- Setting this to `true` allows the body to be repaired along side the engine
- This is also affected by `DuctSimpleMode` in the same ways

### Config.DuctTape.MaxDuctBody
- This is the MAX value the body can be repaired by, leave this below 1000(100%) so people still need to use mechanic's
- If `DuctSimpleMode` is `true` will set it straight to this amount
- If `DuctSimpleMode` is `false` it will be the max amount it can be repaired to
- Default = `450.0` - (45% health)

### Config.DuctAmountBody
- The amount to repair your engine by each ducttape item use
- This is only used if `DuctSimpleMode` is `false`
- Default = `100.0` - (10% Health)

### Config.RemoveDuctTape
- Simply, if this is `true` it will remove 1 ducttape item after use
- If `false` it will be constantly reusable

------------------
## Locations.lua

- This is one of the most important files in the script
	- It holds all the locations for going on duty, where people can apply mods etc.
- I have tried to include as many default mechanic shops as possible (All Gabz MLO's supported)
- These are easy to edit, change or remove, make a new polyzone using the commands
	1. `/pzcreate poly`
	2. `/pzadd`
	3. `/pzfinish`
- The main building's polyzones are made use of when `Config.System.JobLocationRequired = true` enabling this makes it so mechanic items can only used these zones.
- If you have `Config.System.RequiresJob = false` then anyone can use the items in this location, setting this config option to `true` makes it so mechanic workers are the only ones who can use them.

### Explanation of the locations and how to make one
```lua
Config.Locations[#Config.Locations+1] = {
	Enabled = true,
	job = "mechanic",
	zones = {
		vec2(-263.99075317382, -1349.6701660156),
		vec2(-263.5015258789, -1298.9702148438),
		vec2(-229.94024658204, -1299.089477539),
		vec2(-229.81985473632, -1291.589477539),
		vec2(-216.73846435546, -1288.9470214844),
		vec2(-193.63221740722, -1294.155883789),
		vec2(-174.24346923828, -1293.1431884766),
		vec2(-151.77659606934, -1300.6693115234),
		vec2(-151.88639831542, -1311.1921386718),
		vec2(-177.41833496094, -1311.566772461),
		vec2(-177.5919342041, -1351.1942138672)
	},
	autoClock = { enter = true, exit = true, },
	stash = {
		{ coords = vec4(-226.48, -1316.17, 31.27, 0.0), w = 3.6, d = 0.8, },
	},
	store = {
		{ coords = vec4(-228.64, -1314.19, 31.3, 90.0), w = 3.60, d = 0.8 },
	},
	crafting = {
		{ coords = vec4(-214.82, -1339.74, 31.46, 90.0), w = 2.8, d = 1.5 },
	},
	clockin = {
		{ coords = vec4(-195.55, -1316.46, 31.2, 181.72), prop = false },
	},
	manualRepair = {
		{ coords = vec4(-200.28, -1311.62, 31.3, 0.0), prop = true, },
	},
	carLift = {
        { coords = vec4(-201.85, -1319.65, 31.3, 19.36), use = true },
        { coords = vec4(-221.27, -1318.71, 31.3, 352.67), use = true },
    },
	garage = {
		spawn = vec4(-182.74, -1317.61, 30.63, 357.23),
		out = vec4(-190.62, -1311.57, 31.3, 0.0),
		list = { "towtruck", "panto", "slamtruck", "cheburek", "utillitruck3" },
		prop = true
	},
	payments = {
		img = "https://static.wikia.nocookie.net/gtawiki/images/b/be/BennysOriginalMotorWorks-GTAO-Logo.png",
		{ coords = vec4(-192.21, -1316.34, 31.10, 285.83), prop = true },
	},
	Restrictions = {
		Vehicle = { "Compacts", "Sedans", "SUVs", "Coupes", "Muscle", "Sports Classics", "Sports", "Super", "Motorcycles", "Off-road", "Industrial", "Utility", "Vans", "Cycles", "Service", "Emergency", "Commercial", },
		Allow = { "tools", "cosmetics", "repairs", "nos", "perform" },
	},
	blip = {
		coords = vec3(-211.55, -1324.55, 30.9),
		label = "Bennys Original Motorworks",
		color = 1,
		sprite = 446,
		disp = 6,
		scale = 0.7,
		cat = nil,
	},
	discord = {
		link = "",
		color = 16711680,
	}
}
```
### Explanation of each part of the location snippet
- `Enabled`
	- Toggling this enables or disables the current location
- `job`
	- The job role that will work in this building
- `autoClockout`
	- Take employees off duty when leaving the polyzone if they were working in this location
- `zones`
	- This is a batch of `vec2` locations (usually corners of a building) to create a polyzone
- `stash`
	- Where the job stashes will be accessible
	- Only appears if `Config.StoreCraft.StashCraft` or `Config.Repairs.StashRepair` are `true`
- `store` - Where the job lock stores will be accessible
	- These stores are set in the `recipes.lua`
	- By default the items are priced at $0 (free)
- `crafting`
	- Where the crafting stations will be accessible
- `clockin`
	- Where the player can go on duty (Clockin locations are also available at payment locations)
- `nosrefill`
	- Where the non-mechanic nos refill station will be
- `carlift`
	- This is the carlifts that appear when you enter the location, useMLOLift enables the use of a CarLift models used in custom MLO's
- `garage` - The "job garage" system that spawns a fresh temporary car
	- `spawn` - The vec4 location and direction where the spawned vehicle will appear
	- `out` - The vec4 location and direction of the "parking meter" prop used to access the spawn menu
	- `list` - The list of vehicle spawn codes that will appear in the garage's menu
- `payments`
	- Location, heading, and job's logo used for access payment scripts (default: [jim-payments](https://github.com/jimathy/jim-payments))
- `Restrictions`
	- This section controls what CAN be edited in the location
	- Each location comes with all the presets available
- `blip`
	- Where the map maker of the building will appear
- `label`
	- The name of the job/building that will appear on the map
- `color`
	- The colour id of the map marker
- `sprite`
	- The sprite of the blip for the maps
- `disp`
	-
- `scale`
	- The size of the blip marker (defaults are usually 0.7)
- `cat`
	- Category, this isn't required unless you have them set on your server
- `discordlink`
	- The webhook of the channel where this locations `/preview` reports are sent
	- This can be set per location, all you need to do is grab a webhook from a discord channel and then paste it here
	- This can be used in any discord, for example a players job discord's channel
	- If the locations link isn't set or left as `""` it will use the link set at `Config.DiscordDefault` instead, if available
- `discordcolour`
	- This is the colour of the post for the discord channel, this is a "decimal" colour number

### Creating a new polyzone location:
- This is simple guide for making new locations
	- Creating a "Zone"
		- Start by standing new a corner of a new building
		- Type in your chat `/pzcreate zone` and this will bring up a box to name it, type whatever you want to help find it later
		- You can move the created point with your `arrow keys`
		- When this point is placed placed type `/pzadd` to create a new point
		- You can again move this location with your `arrow keys`
		- Repeat this until finished
		- Type `/pzfinish` to finsh creating the zone and save the information to a file
		- The file is located in your server folder next to your `server.cfg`
	- Creating a "Box"
		- Start by standing near the zone you wish to create
		- Type in your chat `/pzcreate box` and this will bring up a box to name it
		- It will then ask you the width and length of the box, a good default is 0.6 and 0.6
		- Holding `Shift` or `Alt` while using the scroll wheel will allow you to change these values
		- Pressing `Z` will swap to being able to move the box up and down and changing the box height
		- Holding `Ctrl` while doing any of this will make it move slower for precise handling
		- Type `/pzfinish` to finsh creating the box and save the information to a file
		- The file is located in your server folder next to your `server.cfg`

------------------
## recipes.lua

## Crafting
- Crafting can be enabled/disabled in `config.lua` with the setting `Config.Crafting`
- Crafting is accessed through locations created by `locations.lua`
- The menu's are shared between all jobs/locations but you can lock items to specific jobs and grades
- And example of a recipe snippet
```lua
--This example is purely an example
{ 	['cleaningkit'] = {		--The item that will be crafted
		['rubber'] = 1,
		["engine2"] = 1,	--An ingredient and the amount needed
		['plastic'] = 1,
	},
	["amount"] = 2,		-- The amount that of the crafted item you will recieve
	["job"] = {			-- Support for hiding items only to certain jobs (multiple possible)
		["mechanic"] = 4,	-- Job: "mechanic" and Grade "4" only and above can see this recipe
		["tuner"] = 4,	-- Job: "tuner" and Grade "4" only and above can see this recipe
	}
},
```
- Where the ingredients come from depends on the `config.lua` settings
	- `StashCraft = true` would demand the ingredients come from the current job roles stash
	- `StashCraft = false` would instead check the players inventory for the ingredient items

## Stores
- Stores can be enabled/disabled in `config.lua` with the setting `Config.Stores`
- There are built in job stores that allow quick access of items
	- By default the items are free, but you can change this easily
- Example of a store snippet entry:
```lua
{
	name = "mechanic_tools", -- Item's spawn code
	price = 0,	-- Cost of the item
	amount = 10,	-- How many are available to buy
	info = {},	-- Usually blank, none of my items use this
	type = "item", -- Usually left as "item"
	requiredJob = { 	-- Job lock for items (THIS ONLY WORKS WITH JIM-SHOPS)
		["mechanic"] = 1,	-- Mechanic grade 1 and higher can see/buy this item
		["tuner"] = 1, 	-- Tuner grade 1 and higher can see/buy this item
	}
},
```