# Mechanic Guide
Read this before opening a ticket.

---
### Index:
1. [Performance Items](https://github.com/jimathy/jim-mechanicguide#performance-items)
2. [Cosmetic Items](https://github.com/jimathy/jim-mechanicguide#cosmetic-items)
3. [Mechanic Items](https://github.com/jimathy/jim-mechanicguide#mechanic-items)
4. [Toolbox](https://github.com/jimathy/jim-mechanicguide#toolbox--check_tuneslua)
5. [Mechanic_Tools](https://github.com/jimathy/jim-mechanicguide#mechanic_tools--repairlua)
6. [Nitrous](https://github.com/jimathy/jim-mechanicguide#nitrous--noslua)
	1. [Nos.lua Config](https://github.com/jimathy/jim-mechanicguide#nos-config-options)
7. [Config.lua](https://github.com/jimathy/jim-mechanicguide#configuration---configlua)
	1. [Config.Lan](https://github.com/jimathy/jim-mechanicguide#configlan)
	1. [Config.Debug](https://github.com/jimathy/jim-mechanicguide#configdebug)
	2. [Config.img](https://github.com/jimathy/jim-mechanicguide#configimg)
	3. [Config.JimShops](https://github.com/jimathy/jim-mechanicguide#configjimshops)
	4. [Config.JimMenu](https://github.com/jimathy/jim-mechanicguide#configjimmenu)
	5. [Config.distkph](https://github.com/jimathy/jim-mechanicguide#configdistkph)
	6. [Config.isVehicleOwned](https://github.com/jimathy/jim-mechanicguide#configisvehicleowned)
	7. [Config.RequiresJob](https://github.com/jimathy/jim-mechanicguide#configrequiresjob)
	8. [Config.LocationBlips](https://github.com/jimathy/jim-mechanicguide#configlocationblips)
	9. [Config.LocationRequired](https://github.com/jimathy/jim-mechanicguide#configlocationrequired)
	10. [Config.CostmeticJob](https://github.com/jimathy/jim-mechanicguide#configcostmeticjob)
	11. [Config.FreeRepair](https://github.com/jimathy/jim-mechanicguide#configfreerepair)
	12. [Config.StashRepair](https://github.com/jimathy/jim-mechanicguide#configstashrepair)
	13. [Config.Stores](https://github.com/jimathy/jim-mechanicguide#configstores)
	14. [Config.StashCraft](https://github.com/jimathy/jim-mechanicguide#configstashcraft)
	15. [Config.Crafting](https://github.com/jimathy/jim-mechanicguide#configcrafting)
	16. [Config.PreviewPhone](https://github.com/jimathy/jim-mechanicguide#configpreviewphone)
	17. [Config.PreviewJob](https://github.com/jimathy/jim-mechanicguide#configpreviewjob)
	18. [Config.PreviewLocation](https://github.com/jimathy/jim-mechanicguide#configpreviewlocation)
	19. [Config.PhoneMail](https://github.com/jimathy/jim-mechanicguide#configphonemail)
	20. [Config.CosmeticRemoval](https://github.com/jimathy/jim-mechanicguide#configcosmeticremoval)
	21. [Config.ShowOdo](https://github.com/jimathy/jim-mechanicguide#configshowodo)
	22. [Config.OdoLocation](https://github.com/jimathy/jim-mechanicguide#configodolocation)
	23. [Config.ManualRepairCost](https://github.com/jimathy/jim-mechanicguide#configmanualrepaircost)
	24. [Config.ManualRepairBased](https://github.com/jimathy/jim-mechanicguide#configmanualrepairbased)
	25. [Config.ManualRepairPercent](https://github.com/jimathy/jim-mechanicguide#configmanualrepairpercent)
	26. [Config.repairEngine](https://github.com/jimathy/jim-mechanicguide#configrepairengine)
	27. [Config.repairExtras](https://github.com/jimathy/jim-mechanicguide#configrepairextras)
	28. [Config.dutyMessage](https://github.com/jimathy/jim-mechanicguide#configdutymessage)
	29. [Config.repairAnimate](https://github.com/jimathy/jim-mechanicguide#configrepairanimate)
	30. [Config.repairSpeed](https://github.com/jimathy/jim-mechanicguide#configrepairspeed)
	31. [Config.NosRefillCharge](https://github.com/jimathy/jim-mechanicguide#confignosrefillcharge)
	32. [Config.DiscordPreview](https://github.com/jimathy/jim-mechanicguide#configdiscordpreview)
	33. [Config.DiscordDefault](https://github.com/jimathy/jim-mechanicguide#configdiscorddefault)
	34. [Config.DiscordColour](https://github.com/jimathy/jim-mechanicguide#configdiscordcolour)
	35. [Repair requirements](https://github.com/jimathy/jim-mechanicguide#repairrequirements)
	36. [Duct tape](https://github.com/jimathy/jim-mechanicguide#duct-tape)
		1. [Config.DuctSimpleMode](https://github.com/jimathy/jim-mechanicguide#configductsimplemode)
		2. [Config.MaxDuctEngine](https://github.com/jimathy/jim-mechanicguide#configmaxductengine)
		3. [Config.DuctAmountEngine](https://github.com/jimathy/jim-mechanicguide#configductamountengine)
		4. [Config.DuctTapeBody](https://github.com/jimathy/jim-mechanicguide#configducttapebody)
		5. [Config.MaxDuctBody](https://github.com/jimathy/jim-mechanicguide#configmaxductbody)
		6. [Config.DuctAmountBody](https://github.com/jimathy/jim-mechanicguide#configductamountbody)
		7. [Config.RemoveDuctTape](https://github.com/jimathy/jim-mechanicguide#configremoveducttape)
	44. [Config.Jobroles](https://github.com/jimathy/jim-mechanicguide#configjobroles)
8. [Locations.lua](https://github.com/jimathy/jim-mechanicguide#locationslua)
	1. [Snippet](https://github.com/jimathy/jim-mechanicguide#explanation-of-the-locations-and-how-to-make-one)
	2. [PolyZone Help](https://github.com/jimathy/jim-mechanicguide#creating-a-new-polyzone-location)
9. []

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
- car_armor
- brakes1
- brakes2
- brakes3
- engine1
- engine2
- engine3
- engine4
- suspension1
- suspension2
- suspension3
- suspension4
- transmission1
- transmission2
- transmission3
- drifttires
- bprooftires
- turbo
- headlights
```
------------------
## Cosmetic Items

- These all work very similarly
- Stand next to or get in the vehicle and use these items, if options are available for the car this will bring up a menu that shows a list of possible cosmetics
- To reset back to default, use another of the same item, as you are putting the "stock" on
- The items classed as costmetic items include:
```
- bumper
- exhaust
- externals
- hood
- horn
- internals
- livery
- paintcan
- customplate
- rims
- roof
- rollcage
- seat
- skirts
- spoiler
- tires
- tint_supplies
```

------------------
## Mechanic Items

- This is the list of rest of the items that come with this script
```
- toolbox - This is the scripts main way to control the performance modifications in a car.
- mechanic_tools - This is the script's main repair tools
- nos - My scripts Nitrous Canister
- noscan - Empty Nitrous Canister
- ducttape - A configurable repair item
- mechboard - Given as a list of changes when completing a preview of the vehicle
- underglow_controller - Controls underglow style and colour + xenon headlight colours
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

- This menu is  activated by the item "mechanic_tools"
- Note: It tires to get all the information BEFORE the progressbars so if you don't get any animations, theres an error.
- It will start with an animated check of the engine and body for damage and then get a list what it found.
- How this menu fucntions is defined by the config options
	- `FreeRepair = true` will allow you to repair the car with no requirements
	- `StashRepair = true` will place a stash location for the mechanics to place their materials so they can be pulled from there and used when repairing
	- The locations for these mechanic stashes are set at the top of the file, the default is set to Gabz Tuners.

------------------
## Nitrous / nos.lua

- Nitrous relies on two columns in the database `player_vehicles`
	- `hasnitro` - Wether the vehicle has Nitrous in or not
	- `noslevel` - The amount of nos that is in the vehicle (max 100)
- A vehicle's NOS is saved between server restarts for player owned vehicles
- To add NOS to a vehicle you will first need `Turbo` to be installed on the vehicle.
	- Then you will need a NOS cannister(nos) and to use it outside of the vehicle. This will start a skill check to install it.
- To use the NOS boost inside the vehicle, use the `Left Shift` button.
	- This will activate the nitrous purge if you are travelling under a certain speed.
- When the NOS is used up in a vehicle, the driver will receive an empty nos can, which can be refilled/crafted to make it full again.
- If you put in a new can before you run out of NOS in the vehicle you will also recieve an empty can.
- NOS can be installed on almost any vehicle
	- If it allows you to install `Turbo` you can install NOS

#### NOS Config Options
- `NitrousBoost` - Controls how much power is given to the vehicle
	- Default - "55.0"
	- This seems to be a fair number but people have said that in their servers it too powerful and needs to be lowered
- `NitrousUseRate` - This is how fast the nitrous drains
	- Default - "0.5"
	- This seems to be a good number, 0.1 is really slow, 1.0 would be too fast
- `NitrousCoolDown` - This is how long a player has to wait before the boost works again
	- Default - "7000"
	- 7 seconds seems to be enough time for it to cooldown, setting this too low allows some servers players to travel at insane speeds after spamming the button
- `OldFlame` - This sets the boost's flame effect back to qb-tunerchip style
- `tyreSync` - Passing idea never completely finished, this sets the NOS Purge effects colours to the same as the vehicles tiresmoke
- `EnableTrails` - This enables the headlight trails while boosting
- `EnableScreen` - This enables the screen effects while boosting
- `useQBLock` - A toggle added to allow use of `qb-lock` instead of `qb-skillbar` for install NOS

------------------
## Configuration - Config.lua

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
- This only is used at Nos Refill stations, if you have added them to your locations in locations.lua
- The amount in dollars required for a player to refill an Empty NOS can.
- Note: There is also the option of a mechanic crafting them for you.
- The default is `1000`


### Config.DiscordPreview
- This enables or disables the Discord Reports for the `/preview` command
- When `true` this system will send the report to a specified discord channel using a webhook
- When `false` this system will be ignored/disabled

### Config.DiscordDefault
- So people seem to be confused by this one.
- This is the default channel that will be used, no matter where you are.
- If you haven't set specific discord channels in a location, it with "default" to this link.

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
- Explanation of each part of the location snippet
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

-- Police.lua --

This is intended to be for police/ambulance players
It adds a bench to the set locations where they can repair and change a few cosmetics/extras.
This is opened by using third eye/qb-target
You can add other roles to use this but it's not recommended.

---

-- QuickRepair.lua --

This is all about the ducttape item
ALOT of the settings for this are highly customisable and in the config.lua

---

-- Preview.lua --

The preview system is shown by typing /preview

This shows a menu with all possible cosmetic changes for the current vehicle
This will attempt to disable the engine so you can't change then drive away with the changes.

You are able to close the menu when picking cosmetics as it will only "finish" when you leave the drivers seat

Depending on the settings you have chosen in the Config.Lua you will either receive an item or and email with the list of changes

I recommend emails if you are only allowing mechanics to do the previews,

The item can either be mechanic only
or customers only and then passed to the mechanics.

I'm not sure how other phone systems work but the email side of this is made for qb-phone but may be able to be adapted to other phones
