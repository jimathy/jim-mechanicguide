# Mechanic Guide
Read this before opening a ticket.

1. [Performance Items](https://github.com/jimathy/jim-mechanicguide#performance-items)
2. [Cosmetic Items](https://github.com/jimathy/jim-mechanicguide#cosmetic-items)
3. [Config.lua](https://github.com/jimathy/jim-mechanicguide#cosmetic-items)
	- [Config.Debug]()
	- [Config.img]()
	- [Config.JimShops]()
	- [Config.JimMenu]()
	- [Config.distkph]()
4.
5.

------------------
## Performance Items

- These all work very similarly
- Stand next to the vehicle and use these items.
	- If the upgrade can not be put on the car, you will get a notification telling you so.
	- If it can, you will begin adding it to the vehicle.
- If you have an upgraded part already in the vehicle, adding a different level item will remove the previous upgrade from the car and place it in your inventory.
- The mechanic's `toolbox` item is used to remove these upgrades and set them back to stock.
- The items classed as costmetic items include:
	- car_armor
	- brakes (level 1 to 3)
	- engines (level 1 to 4)
	- suspension (level 1 to 4)
	- transmission (level 1 to 3)
	- drifttires
	- bprooftires
	- turbo
	- headlights

------------------
## Cosmetic Items

- These all work very similarly
- Stand next to or get in the vehicle and use these items, if options are available for the car this will bring up a menu that shows a list of possible cosmetics
- To reset back to default, use another of the same item, as you are putting the "stock" on
- The items classed as costmetic items include:
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

### Config.RequiresJob:
- This locks the mechanics performance items and cosmetic items behind a job role.
- The jobs are set lower in the config.lua file at `Config.JobRoles`

### Config.LocationBlips
- This enables your locations blips even if you disable location requirements

### Config.LocationRequired
- This makes it so items become locationbased. You will only be able to work if you are in a polyzone for a job's location (items will only work in a set mechanic shop)
- This this is disabled items can be used anywhere.

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

### Config.ManualRepairBased

### Config.ManualRepairPercent

### Config.repairEngine

### Config.repairExtras

### Config.dutyMessage

### Config.repairAnimate

### Config.repairSpeed


### Config.Repair*:
These are the repair costs and materials that are needed
Each one has to have a set item
The cost for each is a MAX amount, eg. 100% damage would be this number, 50% would be half this number.

### Ducttape configs:
This are for the alternative item to repairkits
They are customisable and let even set the max amount of how much the parts get repaired

### Config.Jobroles:
These are the job roles that you want to be able to use the items in this script (if Config.RequiresJob is enabled)
The defualt setting is just "mechanic".

---

-- Check_tunes.lua --

This is all about the item "toolbox" this item is only usable by mechanics(if job requirements are enabled)

This is expanded by added an INT column to player_vehicles called "traveldistance"
This will add an odometer to the info and show it as Milage or Kilometers.
If you don't add this column this will not show.

This will show info about installed performance items, which part and level is installed, wether they are even able to be installed.
If there is a part installed, you can click the item to remove it and set it back to Stock.

At the bottom is an option to view a list of available cosmetics for the current vehicle, you cannot do anything here, just view what is possible to change on it.

---

-- Repair.lua --

This is actiavted by the item "mechanic_tools"
You will check the engine and body for damage and then get a list of damages.
There are Config settings to fine tune how this works
FreeRepair will allow you to repair the car with no requirements
StashRepair will place a stash location for the mechanics to place their materials so they can be used when repairing.

The locations for the mechanics stashes are set at the top of the file, the default is set to Gabz Tuners.

-----------------------------------------------------------------------------------------------------------------------

-- Locations.lua --

This is one of the most important files in the script
It holds all the locations for going on duty, where people can apply mods etc.

I have tried to include as many default mechanic shops as possible
These are easy to edit, change or remove, make a new polyzone using the commands /pzcreate poly, /pzadd and /pzfinish

These are made use of in Config.LocationRequired, enabling this makes it to performance items can only be added to cars in this zone.
If you have Config.RequiresJob disabled, anyone can use the items in this location, enabling this makes it so mechanic workers are the only ones who can use them.
Enabling Config.JobRequiredForLocation makes it so you need to have have the specified job for the specified building, eg. Benny's workers can only work in the Benny's Building.

If you have these enabled, the workers will be automatically clocked in when entering the building and clocked out when exiting the building.

If you want to add a new polyzone location, to start you need to be near the building you want to add.

Type "/pzcreate poly" to start creating a PolyZone. Pick a name, this doesn't matter as you set this later in locations.lua
You will then get a red line right where you are standing.

Use your ARROW keys to move this around to the first corner/point you want to place.
When its in the correct place, type "/pzadd" and this will lock the current point and allow you to create another
Repeat this until your last corner/point where you will type "/pzfinish".

This will save all the vectors of the points you have chosen and place them in a file called: "polyzone_created_zones.txt"

In this file is the vectors that you need to copy over to my scripts.


	- Crafting -
This hold the crafting abilities for mechanics
You can enable or disable this entirely in the Config.lua with Config.Crafting
This is a crafting system with the recipes kept in recipes.lua.

	- Stores -
This is a basic "shop" for mechanics, this allows them to quickly grab the items they need to customise a vehicle
The prices, amounts and such can all be edited within the recipes.lua.

	- Payments -
This script is mainly controlled by my free payment script: jim-payments (https://github.com/jimathy/jim-payments)
This location spawns with a cash register prop to help find it.

On accepting of the payment, everyone with the correct job and who is on duty, will get a receipt. This can be cashed in at the bank to for an amount set in the jim-payments config.

There is also a very basic built in /charge command that works like the /bill command.
It sends an invoice to the customer who can then pay it on their phone.

-----------------------------------------------------------------------------------------------------------------------

-- NOS.lua --

The nos features are expanded if you add two new columns to your player_vehicles database

One column needs to be a boolean column called "hasnitro"
The other needs to be an INT colum called "noslevel"

Adding these will save the NOS between server restarts for player owned vehicles, otherwise the amount of nos left over will be lost at a script or server restart

To add NOS to a vehicle you will first need Turbo to be installed on the vehicle.
Then you will need a full NOS cannister(nos) and to use it outside of the vehicle. This will start a skill check to install it.

To use the NOS boost inside the vehicle, use the "Left Shift" button.
This will activate the nitrous purge if you are travelling under a certain speed.

When the NOS runs out, the driver will receive an empty nos car, which can be refilled/crafted to make it full again.
If you put in a new can before you run out of NOS in the vehicle you will also recieve an empty can.

---

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
