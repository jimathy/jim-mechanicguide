# Mechanic Guide
Read this before opening a ticket.

---
## - Index -
1. [Performance Items](https://github.com/jimathy/jim-mechanicguide#performance-items)
2. [Cosmetic Items](https://github.com/jimathy/jim-mechanicguide#cosmetic-items)
3. [Mechanic Items](https://github.com/jimathy/jim-mechanicguide#mechanic-items)
4. [Toolbox](https://github.com/jimathy/jim-mechanicguide#toolbox--check_tuneslua)
5. [Mechanic_Tools](https://github.com/jimathy/jim-mechanicguide#mechanic_tools--repairlua)
6. [manualrepair.lua](https://github.com/jimathy/jim-mechanicguide#manualrepairlua--non-mechanic-repair-benches)
7. [police.lua](https://github.com/jimathy/jim-mechanicguide#policelua--emergency-repair-benches)
8. [/preview](https://github.com/jimathy/jim-mechanicguide#previewlua---preview)
9. [Config.lua](https://github.com/jimathy/jim-mechanicguide#configuration---configlua)
- Basics
	- [Config.Lan](https://github.com/jimathy/jim-mechanicguide#configlan)
	- [Config.Debug](https://github.com/jimathy/jim-mechanicguide#configdebug)
	- [Config.img](https://github.com/jimathy/jim-mechanicguide#configimg)
	- [Config.JimShops](https://github.com/jimathy/jim-mechanicguide#configjimshops)
	- [Config.JimMenu](https://github.com/jimathy/jim-mechanicguide#configjimmenu)
	- [Config.distkph](https://github.com/jimathy/jim-mechanicguide#configdistkph)
- Mechanic Controls
	- [Config.isVehicleOwned](https://github.com/jimathy/jim-mechanicguide#configisvehicleowned)
	- [Config.RequiresJob](https://github.com/jimathy/jim-mechanicguide#configrequiresjob)
	- [Config.LocationBlips](https://github.com/jimathy/jim-mechanicguide#configlocationblips)
	- [Config.LocationRequired](https://github.com/jimathy/jim-mechanicguide#configlocationrequired)
	- [Config.CostmeticJob](https://github.com/jimathy/jim-mechanicguide#configcostmeticjob)
	- [Config.FreeRepair](https://github.com/jimathy/jim-mechanicguide#configfreerepair)
	- [Config.StashRepair](https://github.com/jimathy/jim-mechanicguide#configstashrepair)
	- [Config.Stores](https://github.com/jimathy/jim-mechanicguide#configstores)
	- [Config.StashCraft](https://github.com/jimathy/jim-mechanicguide#configstashcraft)
	- [Config.Crafting](https://github.com/jimathy/jim-mechanicguide#configcrafting)
- Preview Modifiers
	- [Config.PreviewPhone](https://github.com/jimathy/jim-mechanicguide#configpreviewphone)
	- [Config.PreviewJob](https://github.com/jimathy/jim-mechanicguide#configpreviewjob)
	- [Config.PreviewLocation](https://github.com/jimathy/jim-mechanicguide#configpreviewlocation)
	- [Config.PhoneMail](https://github.com/jimathy/jim-mechanicguide#configphonemail)
- Cosmetic Removal
	- [Config.CosmeticRemoval](https://github.com/jimathy/jim-mechanicguide#configcosmeticremoval)
- Odometer Control
	- [Config.ShowOdo](https://github.com/jimathy/jim-mechanicguide#configshowodo)
	- [Config.OdoLocation](https://github.com/jimathy/jim-mechanicguide#configodolocation)
- Manual Repair Benches
	- [Config.ManualRepairCost](https://github.com/jimathy/jim-mechanicguide#configmanualrepaircost)
	- [Config.ManualRepairBased](https://github.com/jimathy/jim-mechanicguide#configmanualrepairbased)
	- [Config.ManualRepairPercent](https://github.com/jimathy/jim-mechanicguide#configmanualrepairpercent)
	- [Config.repairEngine](https://github.com/jimathy/jim-mechanicguide#configrepairengine)
	- [Config.repairExtras](https://github.com/jimathy/jim-mechanicguide#configrepairextras)
	- [Config.dutyMessage](https://github.com/jimathy/jim-mechanicguide#configdutymessage)
	- [Config.repairAnimate](https://github.com/jimathy/jim-mechanicguide#configrepairanimate)
	- [Config.repairSpeed](https://github.com/jimathy/jim-mechanicguide#configrepairspeed)
- NOS
	- [Config.NosRefillCharge](https://github.com/jimathy/jim-mechanicguide#confignosrefillcharge)
	- [Config.NosTopSpeed](https://github.com/jimathy/jim-mechanicguide#confignostopspeed)
	- [Config.NosBoostPower](https://github.com/jimathy/jim-mechanicguide#confignosboostpower)
	- [Config.NosBindings](https://github.com/jimathy/jim-mechanicguide#confignosbindngs)
	- [Config.NitrousUseRate](https://github.com/jimathy/jim-mechanicguide#confignitroususerate)
	- [Config.NitrousCoolDown](https://github.com/jimathy/jim-mechanicguide#confignosrefillcharge)
	- [Config.CooldownConfirm](https://github.com/jimathy/jim-mechanicguide#configcooldownconfirm)
	- [Config.nosDamage](https://github.com/jimathy/jim-mechanicguide#confignosdamage)
	- [Config.boostExplode](https://github.com/jimathy/jim-mechanicguide#configboostexplode)
	- [Config.EnableFlame](https://github.com/jimathy/jim-mechanicguide#configenableflame)
	- [Config.EnableTrails](https://github.com/jimathy/jim-mechanicguide#configenabletrails)
	- [Config.EnableScreen](https://github.com/jimathy/jim-mechanicguide#configenablescreen)
	- [Config.skillcheck](https://github.com/jimathy/jim-mechanicguide#configskillcheck)
	- [Config.explosiveFail](https://github.com/jimathy/jim-mechanicguide#configexplosivefail)
	- [Config.explosiveFailJob](https://github.com/jimathy/jim-mechanicguide#configexplosivefailjob)
- Discord Preview
	- [Config.DiscordPreview](https://github.com/jimathy/jim-mechanicguide#configdiscordpreview)
	- [Config.DiscordDefault](https://github.com/jimathy/jim-mechanicguide#configdiscorddefault)
	- [Config.DiscordColour](https://github.com/jimathy/jim-mechanicguide#configdiscordcolour)
- Repairs
	- [Repair requirements](https://github.com/jimathy/jim-mechanicguide#repairrequirements)
	- [Duct tape](https://github.com/jimathy/jim-mechanicguide#duct-tape)
		1. [Config.DuctSimpleMode](https://github.com/jimathy/jim-mechanicguide#configductsimplemode)
		2. [Config.MaxDuctEngine](https://github.com/jimathy/jim-mechanicguide#configmaxductengine)
		3. [Config.DuctAmountEngine](https://github.com/jimathy/jim-mechanicguide#configductamountengine)
		4. [Config.DuctTapeBody](https://github.com/jimathy/jim-mechanicguide#configducttapebody)
		5. [Config.MaxDuctBody](https://github.com/jimathy/jim-mechanicguide#configmaxductbody)
		6. [Config.DuctAmountBody](https://github.com/jimathy/jim-mechanicguide#configductamountbody)
		7. [Config.RemoveDuctTape](https://github.com/jimathy/jim-mechanicguide#configremoveducttape)
- Item Controls
	- [Config.Jobroles](https://github.com/jimathy/jim-mechanicguide#configjobroles)
	- [Config.nosBarColour](https://github.com/jimathy/jim-mechanicguide#confignosbarcolour)
	- [Config.nosBarFull](https://github.com/jimathy/jim-mechanicguide#confignosbarfull)
	- [Config.nosBarEmpty](https://github.com/jimathy/jim-mechanicguide#confignosbarempty)
11. [Locations.lua](https://github.com/jimathy/jim-mechanicguide#locationslua)
	1. [Snippet](https://github.com/jimathy/jim-mechanicguide#explanation-of-the-locations-and-how-to-make-one)
	2. [PolyZone Help](https://github.com/jimathy/jim-mechanicguide#creating-a-new-polyzone-location)
12. [recpies.lua](https://github.com/jimathy/jim-mechanicguide#recipeslua)
	1. [Crafting](https://github.com/jimathy/jim-mechanicguide#crafting)
	2. [Stores](https://github.com/jimathy/jim-mechanicguide#stores)
13. [Installation Notes](https://github.com/jimathy/jim-mechanicguide#installation-notes)
	1. [server.cfg](https://github.com/jimathy/jim-mechanicguide#add-the-script-to-the-server-resources)
	2. [Item List](https://github.com/jimathy/jim-mechanicguide#item-installation)
	3. [Dependancies](https://github.com/jimathy/jim-mechanicguide#dependancies)
	4. [Mechboard](https://github.com/jimathy/jim-mechanicguide#mechboard-item)
	5. [Update Core Events](https://github.com/jimathy/jim-mechanicguide#updating-core-events)
	6. [QB-MechanicJob](https://github.com/jimathy/jim-mechanicguide#qb-mechanicjob)
	7. [QB-MechanicJob Optimization](https://github.com/jimathy/jim-mechanicguide#qb-mechanicjob-optimization)
	8. [Blue Nos Flames](https://github.com/jimathy/jim-mechanicguide#blue-nos-flames--nopixel-style)

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
- brakes1 - "Performance Brakes"
- brakes2 - "GT Big Brakes"
- brakes3 - "Competition Brakes"
- engine1 - "Shonen Engine"
- engine2 - "V8 Engine"
- engine3 - "V10 Engine"
- engine4 - "V12 Engine"
- suspension1 - "Lowered Suspension"
- suspension2 - "Street Suspension"
- suspension3 - "Racing Suspension"
- suspension4 - "Rally Suspension"
- transmission1 - "Transmission Lvl 1"
- transmission2 - "Transmission Lvl 2"
- transmission3 - "Transmission Lvl 3"
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
```

------------------
## Toolbox / Check_tunes.lua

- This is all about the item "toolbox" this item
- The toolbox is only usable by mechanics, if `Config.RequiresJob` is enabled
- This item can only be used **OUTSIDE** of a vehicle.
- This displays information about the vehicle's currently installed peformance modifications
	- It will attempt to grab information from qb-core's `vehicles.lua` to display vehicle names and the value, it does this by searching for a matching "model hash".
	- It will list the names and levels of each installed modification, and even if they can be installed on the vehicle at all.
	- If there is an installed item you can select it in the shown menu, then you will be the given a confirmation option to remove it. Doing so will set it back to stock and place the specific upgrade in your inventory.
- At the bottom of this menu is a quick shortcut to what is displayed by the `/checkmods` command, which displays a simple list of all possible cosmetic mods that can applied to the current vehicle

------------------
## Mechanic_Tools / repair.lua

- This menu is activated by the item "mechanic_tools"
- Note: It tires to get all the information BEFORE the progressbars so if you don't get any animations, theres an error.
- It will start with an animated check of the engine and body for damage and then get a list what it found.
- How this menu fucntions is defined by the config options
	- `FreeRepair = true` will allow you to repair the car with no requirements
	- `StashRepair = true` will place a stash location for the mechanics to place their materials so they can be pulled from there and used when repairing
	- The locations for these mechanic stashes are set at the top of the file, the default is set to Gabz Tuners.
- When `qb-mechanicjob` is detected, it automatically attempts to load extra damages from this script
	- If you don't use it, only Engine and Body will be available to repair

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
	- `Config.ManualRepairCost` - This is the **SET** amount a vehicle repair will cost
	- `Config.ManualRepairBased` - when `true` this overrides the above and grabs the value of the vehicle from vehicles.lua
	- `Config.ManualRepairPercent` - The percentage of the vehicle value to be used. Default is `5`
	- `Config.repairEngine` - `true` repair engine + body, `false` repair body only
	- `Config.repairExtras` - `true` will attempt to repair extra damages from `qb-mechanicjob`
	- `Config.dutyMessage` - The excuse for why people can't repair while mechanics are on duty.
	- `Config.repairAnimate` - Animates the repair, better than a progress bar
	- `Config.repairSpeed` - How fast each repair step takes
- NOTE: People have reported this file causing issues with removing other qb-target locations in other files
	- I have no idea how or why.
	- Removing this file seems to fix it.

------------------
## police.lua / Emergency Repair Benches

- This file creates repair/customisation benches for police
	- These are intended to be for Police/EMS players, but other job roles can be added easily
- It adds a bench to the set locations where they can repair and change a handful of cosmetics/extras.
- This is activated by using third eye/qb-target
- Note: I have been asked several times to add more options to this
	- There are so many different custom police cars that use a random modification to change a small thing on the vehicle.
	- At that point if I added more/all options it would just be another version of `qb-customs`

------------------
## preview.lua - `/preview`

- The preview system is shown by typing `/preview`
	- This system locks the vehicle in place
	- Shows a menu with all possible cosmetic changes for the current vehicle
	- You can close the menu to move the camera around
	- Typing `/preview` opens it again allowing you to continue
	- When complete, exit the vehicle and the preview will be classed as finished
- When exiting the vehicle, depending on the set config options you will recieve a list of the changes made
	- `Config.DiscordPreview` will attempt to print the list to a specified discord channel
	- `Config.PreviewPhone = true` will attempt to use the set phone system to send the player a phone email with the list
	- `Config.PreviewPhone = false` will spawn a item `mechboard` which when used will show the list of changes on screen
- Note: Spawning the `mechboard` item, trying to use it and then asking me why it's telling you not to spawn it shows you haven't read this-

-----------------
## Configuration - config.lua

There is little snippets of information on each line for these, but this is a more detailed list of information

### Config.Lan
- This script has a built in locale system, it fairly updated versions, but the most recent versions of each language will be at: https://github.com/jimathy/mechanic-locales
- You will need to then set the langauge with Config.Lan. By default it's set to english `"en"`

### Config.Debug
- This enables a debug mode, this will enable the debug boxes around locations to show you where they are set and where they are moving to.
- This also enables Debug Messages in the F8 Menu and server console to help me and you with debugging issues

### Config.img
- Use this if if you are using an older/edited version of qb-menu
- This is for adding images of inventory items to qb-menu and qb-input.
- The default would be: `qb-inventory/html/images/`
- I personally use LJ's inventory system which makes it: `lj-inventory/html/images/`. I imagine other's are pretty similar.

### Config.JimShops
- Set this to true if you are using my free qb-shops alternative, [jim-shops](https://github.com/jimathy/jim-shops)
- Set to false to use default inventory style shops

### Config.JimMenu
- Set this to true if you have an updated qb-menu with inventory icon/fontawesome support
- This clear's `Config.img` so you don't get duplicate images

### Config.distkph
- This is only used when the odometer is used, toolbox menu and the onscreen milage display.
	- `true` = distance in Kilometers
	- `false` = distance in Miles

### Config.isVehicleOwned
- This checks the `player_vehicles` database for if the vehicle is player owned or not.
- If you only want customisations to be made to player owned vehicles, enable this.

### Config.RequiresJob
- This locks the mechanics performance items and cosmetic items behind a job role.
- The jobs are set lower in the config.lua file at `Config.JobRoles`

### Config.LocationBlips
- This enables your locations blips even if you disable location requirements

### Config.LocationRequired
- This makes it so items become location locked. You will only be able to work if you are in a polyzone for a job's location (items will only work in a set mechanic shop)
- If this is disabled items can be used anywhere.

### Config.CostmeticJob
- This enables or disables a job requirement on cosmetic items.
- This ignores `Config.RequiresJob`

### Config.FreeRepair
- Enabling this makes all repairs by mechanic not require any materials to repair, so they repairs are free.

### Config.StashRepair
- This enables grabbing materials for repairs from their current jobs mechanics stash, these stashes are accessible at set loications in the locations.lua.
- If disabled materials will be taken from the players inventory.

### Config.Stores
- This enables or completely disables the creation of shops for items.
- If you want your mechanics to be able to either buy or get the items for free quickly, enable this.

### Config.StashCraft
- This enables grabbing materials for crafting from their current jobs mechanics stash, these stashes are accessible at set loications in the locations.lua.
- If disabled materials will be taken from the players inventory.

### Config.Crafting
- This enables or completely disables the creation of crafting locations for items.
- If you want your mechanics to build and craft each item from ingredients, enable this.

### Config.PreviewPhone
- Enabling this will make the changed cosmetics from `/preview` be collected into an email and be sent to the person who did the preview
- Disabling this will make the list of changed costmetics and put it on a new "mechboard" item which is given to the person who did the preview

### Config.PreviewJob
- Enabling this locks the `/preview` command behind job roles
- The jobs are set lower in the config.lua file at `Config.JobRoles`

### Config.PreviewLocation
- Enable this if you want to lock the `/preview` command to only work in mechanic shops

### Config.PhoneMail
- This is used to determine your which phone script you use to send an email with preview details to your players
- This is only used if `Config.PreviewPhone` is true
- This currently as of writing this only supports `qb-phone` and `gks-phone`

### Config.CosmeticRemoval
- This simply, when enabled, will remove the cosmetic items (listed above) from your inventory when successfully added to the vehicle
- Disabling make them unlimited use

### Config.ShowOdo
- Enabling this will by default show the on-screen Odometer(Miles/Kilometers) when driving in an owned vehicle.
- Players can toggle on and off theirselves easily with the command `/showodo`

### Config.OdoLocation
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

### Config.ManualRepairCost
- This is the amount to charge people for a repair at the manual repair benches.
- The default is `5000` but I recommend setting this to a high amount for your server
- The intention of the mechanic script is to provide RP to the server, there is no RP in using a prop instead of talking to someone.

### Config.ManualRepairCostBased
- Set this to true if you want the cost to ALWAYS be the amount set at "ManualRepairCost"
- Set this to false if you want it to "ManualRepairCost" to be the max and cost is calculated by damage

### Config.ManualRepairBased
- This overrides the previous setting `ManualRepairCost`
- Setting this to true sets the price of the repair to be based on the cost of the vehicle in your vehicles.lua

### Config.ManualRepairPercent
- This is only used if `ManualRepairBased` is enabled.
- This needs to be set to the percentage of the value of the vehicle you want to charge people per repair
- For example:
	- 5% of a $10,000 car would be $500 per repair
	- 10% of a $200,000 car would be $20,000 per repair

### Config.repairEngine
- When enabled this will include engine repairs in the Repair Bench process
- If disabled it will only attempt to repair the body

### Config.repairExtras
- Enabling this will include Extra Damages repair that come from `qb-mechanicjob`
- if `qb-mechanicjob` is not found but this is true, it will skip over these extras

### Config.dutyMessage
- I left his here as people were giving me different reasons for why they wanted the repair benches in the script
- I'm leaving this up to them for how they want to phrase their notification.
- Default: `"There is a Mechanic on duty!"`

### Config.repairAnimate
- When `true` this will add a small animatied sequence to the repair of the vehicle, instead of people just sitting and watching a progressbar

### Config.repairSpeed
- The time between each task while using repairAnimate. `1500` Seems to be a reasonable time for each one

### Config.NosRefillCharge
- This only is used at NOS Refill stations, if you have added them to your locations in locations.lua
- The amount in dollars required for a player to refill an Empty NOS can.
- Note: There is also the option of a mechanic crafting them for you.
- The default is `1000`

### Config.NosTopSpeed
- Controls the top speed "multiplier" when boosting
- Functions a bit weirdly - 55.0 isn't 55 times normal speed, but seems a good boost value
- Default - `55.0`
- This seems to be a fair number but people have said that in their servers this number is too powerful and needed to be lowered
- Removing this config option or setting this to `-1.0` disables it and leaves the accelleration boost on.

### Config.NosBoostPower
- Fine controls over the accelleration power for each boost level
- Shown as a table for optimization
```lua
NosBoostPower = {
	10.0, -- Level 1
	30.0, -- Level 2
	50.0, -- Level 3
},
```
- These values seem a good default, but may need adjusting if you have customised vehicle meta files

### Config.NosBindings
- Simply, this is the location of the NOS keybindings
- A handful of people reported "36" just didn't work for them, so this is to make it easier to change
```lua
NosBindings = {
	36, -- Switch mode button - Default: 36 "LEFT CTRL"
	21, -- Activate NOS/Purge - Default: 21 "LEFT SHIFT"
	10, -- Boost/Purge UP - Default: 10 "PAGE UP"
	11, -- Boost/Purge Down - Default: 11 "PAGE DOWN"
},
```

### Config.NitrousUseRate
- This is how fast the nitrous drains
- Default - `0.4`
- Boost Level 1 changes this number minus half of this number (0.4 - (0.4 / 2))
- Boost Level 3 changes this number plus half of this number (0.4 + (0.4 / 2))

### Config.NitrousCoolDown
- This is how long a player has to wait before the boost works again
- Default - `7000`
- 7 seconds seems to be enough time for it to cooldown, setting this too low allows some servers players to travel at insane speeds after spamming the button
- Set to `0` to disable this

### Config.CooldownConfirm
- Simply, this will play a confirmation beep when cooldown is complete
- Made is toggleable in the config in case people didn't like it

### Config.nosDamage
- This enables NOS causing damage to engine while boosting
- Boosting for too long will play sound alerts and damage the Engine.

### Config.boostExplode
- If boosting too long at Boost Level 3 the NOS tank will explode.
- Will cause damage to the vehicle and cause a fire.
- This will remove remaining NOS from the vehicle and not give an empty tank

### Config.EnableFlame
- `true` adds exhaut flame effects while boosting
### Config.EnableTrails
- `true` adds taillight effects while boosting
### Config.EnableScreen
- `true` True adds screen effects while boosting

### Config.skillcheck
- When adding Nos to a vehicle there are three skillcheck script options available
	- "qb-skillbar"
	- "qb-lock"
	- "ps-ui"

### Config.explosiveFail
- When `true` there is a `1 in 10` chance for when you fail the skillcheck for the tank to explode in the vehicle.
- Doesn't cause much damage, but fill push the player and vehicle back

### Config.explosiveFailJob
- When `false` mecahnics WILL **NOT** cause explosions on failing the skill check
- When `true` mechanics **CAN** cause explosions on failing the skill check

### Config.DiscordPreview
- This enables or disables the Discord Reports for the `/preview` command
- When `true` this system will send the report to a specified discord channel using a webhook
- When `false` this system will be ignored/disabled

### Config.DiscordDefault
- So people seem to be confused by this one.
- This is the default channel that will be used, no matter where you are.
- If you haven't set specific discord channels in a location, it **should** "default" to this link.

### Config.DiscordColour
- You don't need to touch this, but this is the default colour of the post in the discord channel
- The default colour is `16753920` - this is a "decimal" colour number, which is a yellow colour.


### Repair requirements
- These are the repair costs and materials that are needed
- Each one has to have **1** set item
- The cost for each is a MAX amount, eg. 100% damage would be this number, 50% would be half this number.
- The defaults:
```
RepairEngine = "iron",
RepairEngineCost = 8,
--
RepairBody = "plastic",
RepairBodyCost = 8,
--
RepairRadiator = "plastic",
RepairRadiatorCost = 8,
--
RepairAxle = "steel",
RepairAxleCost = 8,
--
RepairBrakes = "iron",
RepairBrakesCost = 8,
--
RepairClutch = "aluminum",
RepairClutchCost = 8,
--
RepairFuel = "plastic",
RepairFuelCost = 8,
```

### Duct tape:
- Many people forgot these are a thing while begging me to add repair benches..
- The Ducttape item is intended to be an alternative and customisable version of repairkits
- They are customisable and let even set the max amount of how much the parts get repaired

### Config.DuctSimpleMode
- This sets the duct tape item into simple mode, repairing to the amount every time
- `true` makes duct tape set every use to the amount set below at `MaxDuctEngine`
- `false` uses the `DuctAmountEngine` value to repair the by vehicle each use

### Config.MaxDuctEngine
- This is the MAX value the engine can be repaired by, leave this below 1000(100%) so people still need to use mechanic's
- If `DuctSimpleMode` is `true` will set it straight to this amount
- If `DuctSimpleMode` is `false` it will be the max amount it can be repaired to
- Default = `450.0` - (45% health)

### Config.DuctAmountEngine
- The amount to repair your engine by each ducttape item use
- This is only used if `DuctSimpleMode` is `false`
- Default = `100.0` - (10% Health)

### Config.DuctTapeBody
- Setting this to `true` allows the body to be repaired along side the engine
- This is also affected by `DuctSimpleMode` in the same ways

### Config.MaxDuctBody
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

### Config.Jobroles:
- This only matters if Config.RequiresJob is enabled and is specifcally for the ability to use the mecahnic items and use `/preview` command
- These are the job roles that you want to be able to use the items in this script
- Example layout for multiple job roles: `JobRoles = { "mechanic", "tuner" }`
- The defualt setting is = `{ "mechanic" }`

### Config.nosBarColour
- When set to true it will create a "progressbar" for a value in colour
	- <span style='color:green'>▓</span><span style='color:yellow'>▓</span><span style='color:red'>▓</span><span style='color:grey'>░</span>
- when set to false it will leave the bars as white and grey
	- <span style='color:white'>▓</span><span style='color:grey'>░</span>

### Config.nosBarFull
- This is the symbol used to indicate a full segment in the bar
	- Default = `▓`

### Config.nosBarEmpty
- This is the symbol used to indicate an empty segment in the bar
	- Default = `░`

------------------
## Locations.lua

- This is one of the most important files in the script
	- It holds all the locations for going on duty, where people can apply mods etc.
- I have tried to include as many default mechanic shops as possible (All Gabz MLO's supported)
- These are easy to edit, change or remove, make a new polyzone using the commands
	1. `/pzcreate poly`
	2.  `/pzadd`
	3. `/pzfinish`
- The main building's polyzones are made use of when `Config.LocationRequired = true` enabling this makes it so mechanic items can only used these zones.
- If you have `Config.RequiresJob = false` then anyone can use the items in this location, setting this config option to `true` makes it so mechanic workers are the only ones who can use them.

### Explanation of the locations and how to make one
```lua
{	job = "mechanic",
	zones = {
		vector2(154.69816589355, -3007.0153808594),
		vector2(120.64015197754, -3006.7275390625),
		vector2(120.48593902588, -3051.8874511719),
		vector2(154.61296081543, -3051.5419921875)
	},
	stash = { { coords = vector3(144.38, -3051.3, 7.04), w = 0.6, d = 3.6, heading = 0.0 }, },
	store = { { coords = vector3(128.64, -3014.68, 7.04), w = 1.6, d = 3.0, heading = 0.0, }, },
	crafting = { { coords = vector3(136.71, -3051.29, 7.04), w = 0.6, d = 1.0, heading = 0.0, }, },
	clockin = { { coords = vector3(145.29, -3012.93, 6.94), heading = 86.0, }, },
	nosrefill = { { coords = vector4(121.17, -3044.73, 7.04, 268.96) } },
	garage = { spawn = vector4(163.22, -3009.31, 5.27, 89.72),
				out = vector4(157.37, -3016.57, 7.04, 179.58),
				list = { "towtruck", "panto", "slamtruck", "cheburek", "utillitruck3" } },
	payments = { coords = vector3(146.44, -3014.09, 6.94), heading = 195.0, img = "<center><p><img src=https://static.wikia.nocookie.net/gtawiki/images/f/f2/GTAV-LSCustoms-Logo.png width=150px></p>" },
	blip = vector3(139.91, -3023.83, 7.04),
	bliplabel = "LS Tuner Shop",
	blipcolor = 81,
	discordlink = "",
	discordcolour = 2571775,
},
```
### Explanation of each part of the location snippet
- `job`
	- The job that will work in this building
- `zones`
	- This is a batch of vector2 locations (usually corners of a building) to create a polyzone
- `stash`
	- Where the job stashes will be accessible
	- Only appears if `Config.stashCraft` or `Config.stashRepair` are `true`
- `store` - Where the job lock stores will be accessible
	- These stores are set in the recipes.lua
	- By default the items are priced at $0 (free)
- `crafting`
	- Where the crafting stations will be accessible
- `clockin`
	- Where the player can go on duty
- `nosrefill`
	- Where the non-mechanic nos refill station will be
- `garage` - The "job garage" system that spawns a fresh temporary car
	- `spawn` - The vector4 location and direction where the spawned vehicle will appear
	- `out` - The vector4 location and direction of the "parking meter" prop used to access the spawn menu
	- `list` - The list of vehicle spawn codes that will appear in the garage's menu
- `payments`
	- Location, heading, and job's logo used for access payment scripts (default: [jim-payments](https://github.com/jimathy/jim-payments))
- `blip`
	- Where the map maker of the building will appear
- `bliplabel`
	- The name of the job/building that will appear on the map
- `blipcolor`
	- The colour id of the map marker
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

------------------
## Installation Notes

### Add the script to the server resources
- I highly recommend putting the `jim-mechanic` folder in a new folder called `[jim]`
- Then add `ensure [jim]` AFTER your other scripts in your server.cfg


### Item installation
- Add the image files from the zip to your `qb-inventory > html > images` folder
- Add these lines to your qb-core > shared lua under the Items section

```lua
--Jim-Mechanic Vehicles
["mechanic_tools"] 				= {["name"] = "mechanic_tools", 			["label"] = "Mechanic tools", 		    ["weight"] = 0, 		["type"] = "item", 		["image"] = "mechanic_tools.png", 		["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "Needed for vehicle repairs"},
["toolbox"] 					= {["name"] = "toolbox", 			 	  	["label"] = "Toolbox", 		            ["weight"] = 0, 		["type"] = "item", 		["image"] = "toolbox.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "Needed for Performance part removal"},
["ducttape"] 					= {["name"] = "ducttape", 			 	  	["label"] = "Duct Tape", 		       	["weight"] = 0, 		["type"] = "item", 		["image"] = "bodyrepair.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "Good for quick fixes"},
["mechboard"] 					= {["name"] = "mechboard", 			 	  	["label"] = "Mechanic Sheet", 		   	["weight"] = 0, 		["type"] = "item", 		["image"] = "mechboard.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

--Performance
["turbo"] 		 	 		 	= {["name"] = "turbo", 						["label"] = "Supercharger Turbo", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "turbo.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "Who doesn't need a 65mm Turbo??"},
["car_armor"] 					= {["name"] = "car_armor", 					["label"] = "Vehicle Armor", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "armour.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["nos"] 					    = {["name"] = "nos", 			 	  	  	["label"] = "NOS Bottle", 		        ["weight"] = 0, 		["type"] = "item", 		["image"] = "nos.png", 				    ["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "A full bottle of NOS"},
["noscan"] 					    = {["name"] = "noscan", 			 	  	["label"] = "Empty NOS Bottle", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "noscan.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,  ["combinable"] = nil,   ["description"] = "An Empty bottle of NOS"},
["noscolour"] 					= {["name"] = "noscolour", 			 	  	["label"] = "NOS Colour Injector", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "noscolour.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = false,  ["combinable"] = nil,   ["description"] = "Make that purge spray"},

["engine1"] 				    = {["name"] = "engine1", 			 	  	["label"] = "Shonen Engine",            ["weight"] = 0, 		["type"] = "item", 		["image"] = "shonen.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["engine2"] 				    = {["name"] = "engine2", 			 	  	["label"] = "V8 Engine",        	    ["weight"] = 0, 		["type"] = "item", 		["image"] = "v8engine.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["engine3"] 				    = {["name"] = "engine3", 			 	  	["label"] = "V10 Engine",          		["weight"] = 0, 		["type"] = "item", 		["image"] = "v10engine.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["engine4"] 				    = {["name"] = "engine4", 			 	  	["label"] = "V12 Engine",               ["weight"] = 0, 		["type"] = "item", 		["image"] = "v12engine.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["transmission1"] 				= {["name"] = "transmission1", 				["label"] = "Transmission Lvl 1",       ["weight"] = 0, 		["type"] = "item", 		["image"] = "transmission1.png",  		["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["transmission2"] 				= {["name"] = "transmission2", 				["label"] = "Transmission Lvl 2",       ["weight"] = 0, 		["type"] = "item", 		["image"] = "transmission2.png",  		["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["transmission3"] 				= {["name"] = "transmission3",				["label"] = "Transmission Lvl 3",       ["weight"] = 0, 		["type"] = "item", 		["image"] = "transmission3.png",   		["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["brakes1"] 					= {["name"] = "brakes1", 			 		["label"] = "Performance Brakes",       ["weight"] = 0, 		["type"] = "item", 		["image"] = "brakes1.png", 		    	["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["brakes2"] 					= {["name"] = "brakes2", 			 		["label"] = "GT Big Brakes",            ["weight"] = 0, 		["type"] = "item", 		["image"] = "brakes2.png", 		    	["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["brakes3"] 					= {["name"] = "brakes3", 			 		["label"] = "Competition Brakes",       ["weight"] = 0, 		["type"] = "item", 		["image"] = "brakes3.png", 		    	["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["suspension1"] 				= {["name"] = "suspension1", 				["label"] = "Lowered Suspension", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "suspension1.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["suspension2"] 				= {["name"] = "suspension2",  				["label"] = "Street Suspension",		["weight"] = 0, 		["type"] = "item", 		["image"] = "suspension2.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "Street Racing level Suspension"},
["suspension3"] 				= {["name"] = "suspension3",  				["label"] = "Racing Suspension",		["weight"] = 0, 		["type"] = "item", 		["image"] = "suspension3.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "Street Racing level Suspension"},
["suspension4"] 				= {["name"] = "suspension4",  				["label"] = "Rally Suspension",			["weight"] = 0, 		["type"] = "item", 		["image"] = "suspension4.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = "Street Racing level Suspension"},

["bprooftires"] 				= {["name"] = "bprooftires", 			   	["label"] = "Bulletproof Tires", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "bprooftires.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["drifttires"] 					= {["name"] = "drifttires", 			   	["label"] = "Drift Tires", 				["weight"] = 0, 		["type"] = "item", 		["image"] = "drifttires.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

--Cosmetics
["underglow_controller"] 		 = {["name"] = "underglow_controller", 		["label"] = "Neon Controller", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "underglow_controller.png", ["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   	["description"] = "RGB LED Vehicle Remote"},
["headlights"] 		 	 		 = {["name"] = "headlights", 				["label"] = "Xenon Headlights", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "headlights.png", 			["unique"] = true, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   	["description"] = "8k HID headlights"},

["tint_supplies"] 				 = {["name"] = "tint_supplies", 			["label"] = "Tint Supplies", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "tint_supplies.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,	   ["combinable"] = nil,    ["description"] = "Supplies for window tinting"},

["customplate"] 				 = {["name"] = "customplate", 				["label"] = "Customized Plates", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "plate.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["hood"] 						 = {["name"] = "hood", 						["label"] = "Vehicle Hood", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "hood.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["roof"] 						 = {["name"] = "roof", 						["label"] = "Vehicle Roof", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "roof.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["spoiler"] 					 = {["name"] = "spoiler", 					["label"] = "Vehicle Spoiler", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "spoiler.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["bumper"] 						 = {["name"] = "bumper", 					["label"] = "Vehicle Bumper", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "bumper.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["skirts"] 						 = {["name"] = "skirts", 					["label"] = "Vehicle Skirts", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "skirts.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["exhaust"] 					 = {["name"] = "exhaust", 					["label"] = "Vehicle Exhaust", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "exhaust.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["seat"] 						 = {["name"] = "seat", 						["label"] = "Seat Cosmetics", 			["weight"] = 0, 		["type"] = "item", 		["image"] = "seat.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["rollcage"] 					 = {["name"] = "rollcage", 					["label"] = "Roll Cage", 				["weight"] = 0, 		["type"] = "item", 		["image"] = "rollcage.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["rims"] 						 = {["name"] = "rims", 						["label"] = "Custom Wheel Rims", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "rims.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["livery"] 						 = {["name"] = "livery", 					["label"] = "Livery Roll", 				["weight"] = 0, 		["type"] = "item", 		["image"] = "livery.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["paintcan"] 					 = {["name"] = "paintcan", 					["label"] = "Vehicle Spray Can", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "spraycan.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["tires"] 						 = {["name"] = "tires", 					["label"] = "Drift Smoke Tires",        ["weight"] = 0, 		["type"] = "item", 		["image"] = "tires.png", 	  		    ["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["horn"] 						 = {["name"] = "horn", 						["label"] = "Custom Vehicle Horn", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "horn.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

["internals"] 					 = {["name"] = "internals", 				["label"] = "Internal Cosmetics", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "internals.png", 			["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},
["externals"] 					 = {["name"] = "externals", 				["label"] = "Exterior Cosmetics", 		["weight"] = 0, 		["type"] = "item", 		["image"] = "mirror.png", 				["unique"] = true, 		["useable"] = true, 	["shouldClose"] = true,   ["combinable"] = nil,   ["description"] = ""},

```

## Dependancies
- This script requires `qb-menu` and `qb-input` for the menu systems
- This script requires `qb-target` for opening stores, crafting tables, cash registers, going on duty, nos refill
- This script is also designed to use [jim-payments](https://github.com/jimathy/jim-payments) for charging customers and sending money to the society accounts

## NOS + Odometer
- There are expanded features included in this scripts with SQL
- The included `vehaddon.sql` file needs to be imported into your player_vehicles database to add the appropriate columns (traveldistance, hasnitro, noslevel)
- The `hasnitro` and `noslevel` columns being added enables the of saving Nitrous levels through server restarts
- The `traveldistance` column adds an Odometer to the toolbox/mechanic_tools menus, this this can retrieved in miles or kilometers.


## "mechboard" item
- **This isn't fully required but helps organise multiples of the "mechboard"**
- The MechBoard item is an item given to the person who uses the preview menu and makes changes
- To make full use of this item you need to add the ability for the item to show item info in your inventory system
- I have only done this with `qb-inventory` and `lj-inventory` as they are similar
	- `qb-inventory/html/js/app.js`

- Search for "harness" or Scroll down until you find:
```js
} else if (itemData.name == "harness") {
	$(".item-info-title").html("<p>" + itemData.label + "</p>");
	$(".item-info-description").html(
		"<p>" + itemData.info.uses + " uses left.</p>"
	);
```
- Directly underneath this add:
```js
} else if (itemData.name == "mechboard") {
	$(".item-info-title").html("<p>" + itemData.label + "</p>");
	$(".item-info-description").html(
		"<p>" + itemData.info.vehplate + "</p>" +
		"<p>" + itemData.info.veh + "</p>"
	);
```
- When successfully added the mechboards will show the vehicle and plate number

## Updating core events
- To add the ability to save RGB paints, their colour finishes and drift/bulletproof tires you need to change two functions in your qb-core/client/functions.lua
- Replace `GetVehicleProperties` and `SetVehicleProperties` functions with these:
```lua
function QBCore.Functions.GetVehicleProperties(vehicle)
    if DoesEntityExist(vehicle) then
        local pearlescentColor, wheelColor = GetVehicleExtraColours(vehicle)
		local colorPrimary, colorSecondary = GetVehicleColours(vehicle)

        if GetIsVehiclePrimaryColourCustom(vehicle) then
            local r, g, b = GetVehicleCustomPrimaryColour(vehicle)
            colorPrimary = { r, g, b, colorPrimary }
        end
        if GetIsVehicleSecondaryColourCustom(vehicle) then
            local r, g, b = GetVehicleCustomSecondaryColour(vehicle)
            colorSecondary = { r, g, b, colorSecondary }
        end
        local extras = {}
        for extraId = 0, 12 do
            if DoesExtraExist(vehicle, extraId) then
                local state = IsVehicleExtraTurnedOn(vehicle, extraId) == 1
                extras[tostring(extraId)] = state
            end
        end
        local modLivery = GetVehicleMod(vehicle, 48)
        if GetVehicleMod(vehicle, 48) == -1 and GetVehicleLivery(vehicle) ~= 0 then modLivery = GetVehicleLivery(vehicle) end
        local tireHealth = {}
        for i = 0, 3 do tireHealth[i] = GetVehicleWheelHealth(vehicle, i) end
        local tireBurstState = {}
        for i = 0, 5 do tireBurstState[i] = IsVehicleTyreBurst(vehicle, i, false) end
        local tireBurstCompletely = {}
        for i = 0, 5 do tireBurstCompletely[i] = IsVehicleTyreBurst(vehicle, i, true) end
        local windowStatus = {}
        for i = 0, 7 do windowStatus[i] = IsVehicleWindowIntact(vehicle, i) == 1 end
        local doorStatus = {}
        for i = 0, 5 do doorStatus[i] = IsVehicleDoorDamaged(vehicle, i) == 1 end
        return {
            model = GetEntityModel(vehicle),
            plate = QBCore.Functions.GetPlate(vehicle),
            plateIndex = GetVehicleNumberPlateTextIndex(vehicle),
            bodyHealth = QBCore.Shared.Round(GetVehicleBodyHealth(vehicle), 0.1),
            engineHealth = QBCore.Shared.Round(GetVehicleEngineHealth(vehicle), 0.1),
            tankHealth = QBCore.Shared.Round(GetVehiclePetrolTankHealth(vehicle), 0.1),
            fuelLevel = QBCore.Shared.Round(GetVehicleFuelLevel(vehicle), 0.1),
            dirtLevel = QBCore.Shared.Round(GetVehicleDirtLevel(vehicle), 0.1),
            oilLevel = QBCore.Shared.Round(GetVehicleOilLevel(vehicle), 0.1),
            color1 = colorPrimary,
            color2 = colorSecondary,
            pearlescentColor = pearlescentColor,
            dashboardColor = GetVehicleDashboardColour(vehicle),
            wheelColor = wheelColor,
            wheels = GetVehicleWheelType(vehicle),
            wheelSize = GetVehicleWheelSize(vehicle),
            wheelWidth = GetVehicleWheelWidth(vehicle),
            tireHealth = tireHealth,
            tireBurstState = tireBurstState,
            tireBurstCompletely = tireBurstCompletely,
            windowTint = GetVehicleWindowTint(vehicle),
            windowStatus = windowStatus,
            doorStatus = doorStatus,
            xenonColor = GetVehicleXenonLightsColour(vehicle),
            neonEnabled = {
                IsVehicleNeonLightEnabled(vehicle, 0),
                IsVehicleNeonLightEnabled(vehicle, 1),
                IsVehicleNeonLightEnabled(vehicle, 2),
                IsVehicleNeonLightEnabled(vehicle, 3)
            },
            neonColor = table.pack(GetVehicleNeonLightsColour(vehicle)),
            headlightColor = GetVehicleHeadlightsColour(vehicle),
            interiorColor = GetVehicleInteriorColour(vehicle),
            extras = extras,
            tyreSmokeColor = table.pack(GetVehicleTyreSmokeColor(vehicle)),
            modSpoilers = GetVehicleMod(vehicle, 0),
            modFrontBumper = GetVehicleMod(vehicle, 1),
            modRearBumper = GetVehicleMod(vehicle, 2),
            modSideSkirt = GetVehicleMod(vehicle, 3),
            modExhaust = GetVehicleMod(vehicle, 4),
            modFrame = GetVehicleMod(vehicle, 5),
            modGrille = GetVehicleMod(vehicle, 6),
            modHood = GetVehicleMod(vehicle, 7),
            modFender = GetVehicleMod(vehicle, 8),
            modRightFender = GetVehicleMod(vehicle, 9),
            modRoof = GetVehicleMod(vehicle, 10),
            modEngine = GetVehicleMod(vehicle, 11),
            modBrakes = GetVehicleMod(vehicle, 12),
            modTransmission = GetVehicleMod(vehicle, 13),
            modHorns = GetVehicleMod(vehicle, 14),
            modSuspension = GetVehicleMod(vehicle, 15),
            modArmor = GetVehicleMod(vehicle, 16),
            modKit17 = GetVehicleMod(vehicle, 17),
            modTurbo = IsToggleModOn(vehicle, 18),
            modKit19 = GetVehicleMod(vehicle, 19),
            modSmokeEnabled = IsToggleModOn(vehicle, 20),
            modKit21 = GetVehicleMod(vehicle, 21),
            modXenon = IsToggleModOn(vehicle, 22),
            modFrontWheels = GetVehicleMod(vehicle, 23),
            modBackWheels = GetVehicleMod(vehicle, 24),
            modCustomTiresF = GetVehicleModVariation(vehicle, 23),
            modCustomTiresR = GetVehicleModVariation(vehicle, 24),
            modPlateHolder = GetVehicleMod(vehicle, 25),
            modVanityPlate = GetVehicleMod(vehicle, 26),
            modTrimA = GetVehicleMod(vehicle, 27),
            modOrnaments = GetVehicleMod(vehicle, 28),
            modDashboard = GetVehicleMod(vehicle, 29),
            modDial = GetVehicleMod(vehicle, 30),
            modDoorSpeaker = GetVehicleMod(vehicle, 31),
            modSeats = GetVehicleMod(vehicle, 32),
            modSteeringWheel = GetVehicleMod(vehicle, 33),
            modShifterLeavers = GetVehicleMod(vehicle, 34),
            modAPlate = GetVehicleMod(vehicle, 35),
            modSpeakers = GetVehicleMod(vehicle, 36),
            modTrunk = GetVehicleMod(vehicle, 37),
            modHydrolic = GetVehicleMod(vehicle, 38),
            modEngineBlock = GetVehicleMod(vehicle, 39),
            modAirFilter = GetVehicleMod(vehicle, 40),
            modStruts = GetVehicleMod(vehicle, 41),
            modArchCover = GetVehicleMod(vehicle, 42),
            modAerials = GetVehicleMod(vehicle, 43),
            modTrimB = GetVehicleMod(vehicle, 44),
            modTank = GetVehicleMod(vehicle, 45),
            modWindows = GetVehicleMod(vehicle, 46),
            modKit47 = GetVehicleMod(vehicle, 47),
            modLivery = modLivery,
            modKit49 = GetVehicleMod(vehicle, 49),
            liveryRoof = GetVehicleRoofLivery(vehicle),
			modDrift = GetDriftTyresEnabled(vehicle),
			modBProofTires = not GetVehicleTyresCanBurst(vehicle),
        }
    else
        return
    end
end

function QBCore.Functions.SetVehicleProperties(vehicle, props)
    if DoesEntityExist(vehicle) then
        if props.extras then
            for id, enabled in pairs(props.extras) do
                if enabled then
                    SetVehicleExtra(vehicle, tonumber(id), 0)
                else
                    SetVehicleExtra(vehicle, tonumber(id), 1)
                end
            end
        end
        local colorPrimary, colorSecondary = GetVehicleColours(vehicle)
        local pearlescentColor, wheelColor = GetVehicleExtraColours(vehicle)
        SetVehicleModKit(vehicle, 0)
        if props.plate then SetVehicleNumberPlateText(vehicle, props.plate) end
        if props.plateIndex then SetVehicleNumberPlateTextIndex(vehicle, props.plateIndex) end
        if props.bodyHealth then SetVehicleBodyHealth(vehicle, props.bodyHealth + 0.0) end
        if props.engineHealth then SetVehicleEngineHealth(vehicle, props.engineHealth + 0.0) end
        if props.tankHealth then SetVehiclePetrolTankHealth(vehicle, props.tankHealth) end
        if props.fuelLevel then SetVehicleFuelLevel(vehicle, props.fuelLevel + 0.0) end
        if props.dirtLevel then SetVehicleDirtLevel(vehicle, props.dirtLevel + 0.0) end
        if props.oilLevel then SetVehicleOilLevel(vehicle, props.oilLevel) end
        if props.color1 then
			if type(props.color1) == "number" then
				colorPrimary = props.color1
				SetVehicleColours(vehicle, colorPrimary, colorSecondary)
			else
				colorPrimary = props.color1[4]
				SetVehicleCustomPrimaryColour(vehicle, props.color1[1], props.color1[2], props.color1[3])
				SetVehicleColours(vehicle, props.color1[4], colorSecondary)
           end
        end
        if props.color2 then
            if type(props.color2) == "number" then
				SetVehicleColours(vehicle, colorPrimary, props.color2)
			else
                SetVehicleCustomSecondaryColour(vehicle, props.color2[1], props.color2[2], props.color2[3])
				SetVehicleColours(vehicle, colorPrimary, props.color2[4])
           end
        end
        if props.pearlescentColor then SetVehicleExtraColours(vehicle, props.pearlescentColor, wheelColor) end
        if props.interiorColor then SetVehicleInteriorColor(vehicle, props.interiorColor) end
        if props.dashboardColor then SetVehicleDashboardColour(vehicle, props.dashboardColor) end
        if props.wheelColor then SetVehicleExtraColours(vehicle, props.pearlescentColor or pearlescentColor, props.wheelColor) end
        if props.wheels then SetVehicleWheelType(vehicle, props.wheels) end
        if props.tireHealth then
            for wheelIndex, health in pairs(props.tireHealth) do
                SetVehicleWheelHealth(vehicle, wheelIndex, health)
            end
        end
        if props.tireBurstState then
            for wheelIndex, burstState in pairs(props.tireBurstState) do
                if burstState then
                    SetVehicleTyreBurst(vehicle, tonumber(wheelIndex), false, 1000.0)
                end
            end
        end
        if props.tireBurstCompletely then
            for wheelIndex, burstState in pairs(props.tireBurstCompletely) do
                if burstState then
                    SetVehicleTyreBurst(vehicle, tonumber(wheelIndex), true, 1000.0)
                end
            end
        end
        if props.windowTint then SetVehicleWindowTint(vehicle, props.windowTint) end
        if props.windowStatus then
			for windowIndex, smashWindow in pairs(props.windowStatus) do
                if not smashWindow then SmashVehicleWindow(vehicle, windowIndex) end
            end
        end
		if props.doorStatus then
            for doorIndex, breakDoor in pairs(props.doorStatus) do
                if breakDoor then
                    SetVehicleDoorBroken(vehicle, tonumber(doorIndex), true)
                end
            end
        end
        if props.neonEnabled then
            SetVehicleNeonLightEnabled(vehicle, 0, props.neonEnabled[1])
            SetVehicleNeonLightEnabled(vehicle, 1, props.neonEnabled[2])
            SetVehicleNeonLightEnabled(vehicle, 2, props.neonEnabled[3])
            SetVehicleNeonLightEnabled(vehicle, 3, props.neonEnabled[4])
        end
		if props.neonColor then SetVehicleNeonLightsColour(vehicle, props.neonColor[1], props.neonColor[2], props.neonColor[3]) end
        if props.headlightColor then SetVehicleHeadlightsColour(vehicle, props.headlightColor) end
        if props.interiorColor then SetVehicleInteriorColour(vehicle, props.interiorColor) end
        if props.wheelSize then SetVehicleWheelSize(vehicle, props.wheelSize) end
        if props.wheelWidth then SetVehicleWheelWidth(vehicle, props.wheelWidth) end
        if props.tyreSmokeColor then SetVehicleTyreSmokeColor(vehicle, props.tyreSmokeColor[1], props.tyreSmokeColor[2], props.tyreSmokeColor[3]) end
        if props.modSpoilers then SetVehicleMod(vehicle, 0, props.modSpoilers, false) end
        if props.modFrontBumper then SetVehicleMod(vehicle, 1, props.modFrontBumper, false) end
        if props.modRearBumper then SetVehicleMod(vehicle, 2, props.modRearBumper, false) end
        if props.modSideSkirt then SetVehicleMod(vehicle, 3, props.modSideSkirt, false) end
        if props.modExhaust then SetVehicleMod(vehicle, 4, props.modExhaust, false) end
        if props.modFrame then SetVehicleMod(vehicle, 5, props.modFrame, false) end
        if props.modGrille then SetVehicleMod(vehicle, 6, props.modGrille, false) end
        if props.modHood then SetVehicleMod(vehicle, 7, props.modHood, false) end
        if props.modFender then SetVehicleMod(vehicle, 8, props.modFender, false) end
        if props.modRightFender then SetVehicleMod(vehicle, 9, props.modRightFender, false) end
        if props.modRoof then SetVehicleMod(vehicle, 10, props.modRoof, false) end
        if props.modEngine then SetVehicleMod(vehicle, 11, props.modEngine, false) end
        if props.modBrakes then SetVehicleMod(vehicle, 12, props.modBrakes, false) end
		if props.modTransmission then SetVehicleMod(vehicle, 13, props.modTransmission, false) end
        if props.modHorns then SetVehicleMod(vehicle, 14, props.modHorns, false) end
        if props.modSuspension then SetVehicleMod(vehicle, 15, props.modSuspension, false) end
        if props.modArmor then SetVehicleMod(vehicle, 16, props.modArmor, false) end
        if props.modKit17 then SetVehicleMod(vehicle, 17, props.modKit17, false) end
        if props.modTurbo then ToggleVehicleMod(vehicle, 18, props.modTurbo) end
        if props.modKit19 then SetVehicleMod(vehicle, 19, props.modKit19, false) end
        if props.modSmokeEnabled then ToggleVehicleMod(vehicle, 20, props.modSmokeEnabled) end
        if props.modKit21 then SetVehicleMod(vehicle, 21, props.modKit21, false) end
        if props.modXenon then ToggleVehicleMod(vehicle, 22, props.modXenon) end
        if props.xenonColor then SetVehicleXenonLightsColor(vehicle, props.xenonColor) end
        if props.modFrontWheels then SetVehicleMod(vehicle, 23, props.modFrontWheels, false) end
        if props.modBackWheels then SetVehicleMod(vehicle, 24, props.modBackWheels, false) end
        if props.modCustomTiresF then SetVehicleMod(vehicle, 23, props.modFrontWheels, props.modCustomTiresF) end
        if props.modCustomTiresR then SetVehicleMod(vehicle, 24, props.modBackWheels, props.modCustomTiresR) end
		if props.modPlateHolder then SetVehicleMod(vehicle, 25, props.modPlateHolder, false) end
        if props.modVanityPlate then SetVehicleMod(vehicle, 26, props.modVanityPlate, false) end
        if props.modTrimA then SetVehicleMod(vehicle, 27, props.modTrimA, false) end
        if props.modOrnaments then SetVehicleMod(vehicle, 28, props.modOrnaments, false) end
        if props.modDashboard then SetVehicleMod(vehicle, 29, props.modDashboard, false) end
        if props.modDial then SetVehicleMod(vehicle, 30, props.modDial, false) end
        if props.modDoorSpeaker then SetVehicleMod(vehicle, 31, props.modDoorSpeaker, false) end
        if props.modSeats then SetVehicleMod(vehicle, 32, props.modSeats, false) end
        if props.modSteeringWheel then SetVehicleMod(vehicle, 33, props.modSteeringWheel, false) end
        if props.modShifterLeavers then SetVehicleMod(vehicle, 34, props.modShifterLeavers, false) end
        if props.modAPlate then SetVehicleMod(vehicle, 35, props.modAPlate, false) end
        if props.modSpeakers then SetVehicleMod(vehicle, 36, props.modSpeakers, false) end
        if props.modTrunk then SetVehicleMod(vehicle, 37, props.modTrunk, false) end
        if props.modHydrolic then SetVehicleMod(vehicle, 38, props.modHydrolic, false) end
        if props.modEngineBlock then SetVehicleMod(vehicle, 39, props.modEngineBlock, false) end
        if props.modAirFilter then SetVehicleMod(vehicle, 40, props.modAirFilter, false) end
        if props.modStruts then SetVehicleMod(vehicle, 41, props.modStruts, false) end
        if props.modArchCover then SetVehicleMod(vehicle, 42, props.modArchCover, false) end
        if props.modAerials then SetVehicleMod(vehicle, 43, props.modAerials, false) end
        if props.modTrimB then SetVehicleMod(vehicle, 44, props.modTrimB, false) end
        if props.modTank then SetVehicleMod(vehicle, 45, props.modTank, false) end
        if props.modWindows then SetVehicleMod(vehicle, 46, props.modWindows, false) end
        if props.modKit47 then SetVehicleMod(vehicle, 47, props.modKit47, false) end
        if props.modLivery then SetVehicleMod(vehicle, 48, props.modLivery, false) SetVehicleLivery(vehicle, props.modLivery) end
        if props.modKit49 then SetVehicleMod(vehicle, 49, props.modKit49, false) end
        if props.liveryRoof then SetVehicleRoofLivery(vehicle, props.liveryRoof) end
		if props.modDrift then SetDriftTyresEnabled(vehicle, true) end
		SetVehicleTyresCanBurst(vehicle, not props.modBProofTires)
		TriggerServerEvent('jim-mechanic:server:loadStatus', props.plate)
    end
end
```

## QB-MechanicJob
- **You don't NEED qb-mechaicjob to use Jim-Mechanic but doing so grants extra features**
- Extra damages will be enabled by default if you use `qb-mechanicjob` and `qb-vehiclefailure`
- This needs to be added the the main script, but if you **DON'T** want to use qb-mechanicjob but have an updated qb-vehiclefailure
- Replace this event in qb-vehiclefailure > client.lua.
- This will make it only work if qb-mechanicjob is started.

```lua
-- Functions
local function DamageRandomComponent()
	if GetResourceState('qb-mechanicjob') ~= "started" then return end
    local dmgFctr = math.random() + math.random(0, 2)
    local randomComponent = DamageComponents[math.random(1, #DamageComponents)]
    local randomDamage = (math.random() + math.random(0, 1)) * dmgFctr
    exports['qb-mechanicjob']:SetVehicleStatus(QBCore.Functions.GetPlate(vehicle), randomComponent, exports['qb-mechanicjob']:GetVehicleStatus(QBCore.Functions.GetPlate(vehicle), randomComponent) - randomDamage)
end
```
## QB-MechanicJob Optimization
- I recently realised that `qb-mechanicjob` by default has a seemingly currently unnecessary database change, every 2 seconds of driving a vehicle.
	- Some servers have over 100 people in. If all players are in cars at the same time that would be 100 database changes every 2 seconds.
- Long explanation is that the distance travelled is set to `0` on script/server starts
	- As you drive your car it updates the distance travelled.
	- This is then used to calculate damages and other things.
	- This is saved server side but also updates the database with the numbers.
	- This isn't needed to be saved as it is saved server side already and never calls it FROM the database and is just a waste and laggy
- **TLDR**: `qb-mechanicjob` has a useless database check that can cause lag for servers with lots of players
```lua
-- Go to qb-mechanicjob server/main.lua and find:
RegisterNetEvent('qb-vehicletuning:server:UpdateDrivingDistance', function(amount, plate)

-- Remove or comment out:
local result = MySQL.Sync.fetchAll('SELECT plate FROM player_vehicles WHERE plate = ?', {plate})
if result[1] ~= nil then
    MySQL.Async.execute('UPDATE player_vehicles SET drivingdistance = ? WHERE plate = ?', {amount, plate})
end
```
- It will work exactly the same way but no extra database lag

## Blue Nos Flames / Nopixel Style
- [Download the FiveM version of this file](https://www.gta5-mods.com/misc/purple-blue-flames-replace-sp-fivem)
- UnZip the file
- Copy the `stream` folder into the `jim-mechanic` folder (next to the fxmanifest.lua)
- Set `OldFlame = true` in nos.lua
	- this also changes the default "backfire" effect in my script too, but OldFlame is more visible
- Restart the script. Done.