# WoW Sounds
**Find specific sounds from the World of Warcraft (WoW) clients.**

This repository currently supports the World of Warcraft: The Lich King (WotLK) 3.3.5a client. It contains a listing of all sounds in the client, which are represented as paths under the WoW `Data` folder. 

Note. these sound locations may contain many if not all sounds from WoW clients prior to 3.3.5a too.

## How It Works
1. WoW first looks up the location of many individual data files, like sounds, at specific locations *before* it looks them up in the listfiles of its MPQ data archives.
2. This means you can easily customize individual files by placing a file at those paths.
3. By placing an empty file at sound file paths, WoW attempts to play empty sounds and therefore effectively mutes that sound.
4. You can find associated sounds to spells, items and other in-game sources by checking a WoW database like [Wowhead](https://wotlk.classic.wowhead) or just searching the files in this repository directly.

## Example
You find the Priest class's spell ability "Inner Focus" irritating. The primary sound that is looped for this spell can be found by searching for "Sounds" under [Inner Fire on Wowhead](https://www.wowhead.com/wotlk/spell=14751/inner-focus#sounds). It is called "PreCastMageLow". Now confirm that "PreCastMageLow" is indeed in one of the sound files in this repository - "wow-sounds-wotlk-3.3.5a-Spells.csv" being an obvious choice to check first, by typing it in the file's searchbox. And there you have it,

*Sound\Spells\PreCastHolyMagicLow.wav*

 **Muting:** simply create a new empty file under your WoW\Data folder, e.g. `World of Warcraft 3.3.5a\Data\Sound\Spells\PreCastHolyMagicLow.wav`.
 **Un-muting:** just delete this empty file, e.g. delete `World of Warcraft 3.3.5a\Data\Sound\Spells\PreCastHolyMagicLow.wav`.

## Bonus: difficult to find sounds
Some sound names can be tricky to find, e.g. they are not directly associated with a spell in a WoW database. I will list them here - with credit - and you are welcome to provide others to benefit the WoW community:

### Spell ###
* Priest Prayer of Mending [credit: fondlez]: *Sound\Spells\prayerofmending_impact_head.wav*
