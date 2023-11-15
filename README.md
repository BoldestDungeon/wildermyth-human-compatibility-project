# Wildermyth: Human Compatibility Project
A small project intended to allow multiple mods to extend the base human history and aspect to allow more mods to be cross-compatible with each other.


## Concept
This module breaks down the `human` aspect into multiple smaller aspects that can be overridden individually, which should allow more mods that affect the base `human` experience to run at the same time.  In addition, placeholder aspects are included in the `humanBase` history entry that can allow multiple mods to inject more aspects (and features) for humans at the same time. (Please submit a pull request to update this README with your mod if you would like to claim one of these extra slots)

## Usage

This mod should be loaded at a lower priority than any mods that are built on top of it.  If using the Steam Workshop, this mod should be listed as a required mod for your feature mod.

This mod includes the following files:

* assets/data/aspects/human.json: This breaks the `human` aspect down into 5 additional aspects:
  * `humanBaseStats`: Includes all of the base human stats EXCEPT retirement age. Override this aspect to modify the basic human prowess.
  * `humanBaseRetirement`: Sets the base retirement age. Mods that only want to change the retirement threshold can do so without affecting the other stats.
  * `humanVoice`: Sets the character's voice to `human`. Allows keeping human base stats & effects without the voice when creating non-human races.
  * `heroicActions`: Includes all of the basic effects, such as `run` and `openDoor`, that all heroes get to do. Generally should not be modified - use one of the extra aspects to add new effects instead.
  * `basicInterfusionRecipes`: Includes all of the basic interfusion spells. Characters who get alternate interfusion spells, such as custom non-human races, can remove or omit this aspect to substitute their own list.
* assets/data/history/humanBase.json: Adds all of the above aspects to the `humanBase.001` entry, plus a number of placeholder extra aspects that mods can claim.
* assets/data/effects/migrations/migrateHumanAspects.json: An effect for upgrading heroes to the new system mid-campaign
