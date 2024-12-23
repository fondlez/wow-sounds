# World of Warcraft (WoW) Sounds

This repository contains a text listing of all sounds in each WoW client, which are represented as paths under the WoW `Data` folder. It currently supports all WoW clients until the Mists of Pandaria expansion: vanilla (1.12.1), The Burning Crusade (2.4.3), Wrath of the Lich King (3.3.5a aka. 3.3.5 build 12340), Cataclysm (4.3.4) and Mists of Pandaria (5.4.8).

The files `wow-sounds-ALL-*.csv` contains the full list of all sounds within each client. However, if searching online, you may find it easier to search the other files which have been broadly split up based on WoW's sound categories. Currently the category files are limited to the [WotLK client](https://github.com/fondlez/wow-sounds/tree/main/wotlk).

Sound locations in later clients may contain many if not all sounds from prior WoW versions. So, you can use the WotLK category files to search for most vanilla sounds, for example.

## How WoW Searches Sounds
1. WoW first looks up the location of many individual data files, like sounds, at specific locations *before* it looks them up in the listfiles of its MPQ data archives.
2. This means you can easily customize individual files by placing a file at those paths.
3. By placing an empty file at sound file paths, WoW attempts to play empty sounds and therefore effectively mutes that sound.
4. You can find associated sounds to spells, NPCs, items and other in-game sources by checking a WoW database like [Wowhead](https://wotlk.wowhead.com) or just searching the files in this repository directly.

## Playing the Sound In-game
You can play any of the sounds by putting the path inside a script with the `PlaySoundFile()` function, e.g. `/script PlaySoundFile([[Sound\Creature\AmbassadorHellmaw\Auch_Helmaw_Slay02.wav]])`. Then copy-paste this script into your WoW chat in-game.

For convenience, I have modified the sound paths into scripts for all the sound category files. If you want just the sound path itself, simply copy the path inside the `[[]]` brackets or download and copy from the full list in one of the `wow-sounds-ALL-*.csv` files which contains only sound paths.

## Example
You find the Priest class's spell ability "Inner Focus" irritating. The primary sound that is looped for this spell can be found by searching for "Sounds" under [Inner Fire on Wowhead](https://www.wowhead.com/wotlk/spell=14751/inner-focus#sounds). It is called "PreCastMageLow". Now confirm that "PreCastMageLow" is indeed in one of the sound files in this repository - with [wow-sounds-wotlk-3.3.5a-Spells.csv](https://github.com/fondlez/wow-sounds/blob/main/wotlk/wow-sounds-wotlk-3.3.5a-Spells.csv) being an obvious choice to check first - by typing it in the file's searchbox. There you find,

* *Sound\Spells\PreCastMageLow.wav*

 **Muting:** simply create a new empty file under your WoW\Data folder, e.g. `World of Warcraft 3.3.5a\Data\Sound\Spells\PreCastMageLow.wav`.
 
 **Un-muting:** just delete this empty file, e.g. delete `World of Warcraft 3.3.5a\Data\Sound\Spells\PreCastMageLow.wav`.

## Tricky Sounds
Some sound names can be tricky to find, e.g. they are not directly associated with a spell or NPC in a WoW database. I will list them here - with credit - and you are welcome to provide others to benefit the WoW community:

* Ability global cooldown fizzles:
    * `/script PlaySoundFile([[Sound\Spells\Fizzle\FizzleFireA.wav]])`
    * `/script PlaySoundFile([[Sound\Spells\Fizzle\FizzleFrostA.wav]])`
    * `/script PlaySoundFile([[Sound\Spells\Fizzle\FizzleHolyA.wav]])`
    * `/script PlaySoundFile([[Sound\Spells\Fizzle\FizzleNatureA.wav]])`
    * `/script PlaySoundFile([[Sound\Spells\Fizzle\FizzleShadowA.wav]])`
    * `/script PlaySoundFile([[Sound\Interface\uEscapeScreenOpen.wav]])`
* Gnome Mechanostrider mount noises:
    * `/script PlaySoundFile([[Sound\Creature\MechaStrider\MechaStriderLoop.wav]])`
    * `/script PlaySoundFile([[Sound\Creature\GnomeSpiderTank\GnomeSpiderTankWoundD.wav]])`
    * `/script PlaySoundFile([[Sound\Creature\GnomeSpiderTank\GnomeSpiderTankWoundE.wav]])`
    * `/script PlaySoundFile([[Sound\Creature\GnomeSpiderTank\GnomeSpiderTankWoundF.wav]])`
* Priest - Prayer of Mending bounce: 
    * `/script PlaySoundFile([[Sound\Spells\prayerofmending_impact_head.wav]])`

## Mute Packs 

I have created some convenient packs for muting specific sounds under [Releases](https://github.com/fondlez/wow-sounds/releases/latest). Just unzip them into your WoW Data folder and the zero-length files inside will mute the sounds.

## Statistics

* **Vanilla (2006-09-19)**: 7354 unique sound paths
* **The Burning Crusade (2008-07-10)**: 12632 unique sound paths
* **Wrath of the Lich King (2010-06-24)**: 21065 unique sound paths
* **Cataclysm (2012-04-10)**: 37544 unique sound paths
* **Mists of Pandaria (2014-06-13)**: 55117 unique sound paths
