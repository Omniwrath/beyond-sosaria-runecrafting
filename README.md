# Omni Runecrafting

A free, standalone RazorEnhanced rune crafting script for the Beyond Sosaria shard, written for the TazUO client. One file: no other files to install, and no setup outside the game. It creates its own data folder named after the file, so you can rename it if you like.

More scripts: [Beyond Sosaria Scripts](../../../beyond-sosaria-scripts).

Pick an equipment slot, type the value you want for each rune, and it crafts the runes from your Rough Stone and applies them to your items until every stat gets there. Nothing is crafted or spent until you have seen the cost and your odds.

## What it does

- **Crafts and applies in one run.** Runes are crafted from the Rough Stone in your Runecrafting Storage, with the
  reagents taken straight from your Reagent Keys. Finished runes already in storage are used before any are crafted.
- **Shows the cost first.** A preview lists every stat and target, the applications, expected breaks and Rough Stone
  the run needs, how many finished items to expect and the odds the whole batch succeeds.
- **Suggests what is within reach.** When a target is unlikely, a Suggested button offers a lower target, or the same
  target on fewer items, that the simulation says will finish.
- **Works fewer items when that is enough.** When a few of your items can still give you a finished one, the preview
  offers buttons such as **Work 3 -- 95%**: the run starts on only the items likeliest to finish, with the odds that at
  least one comes out with every stat.
- **Always works the lowest item first, and never risks your last item.** A run stops with one item of the slot
  left.
- **Templates.** Save the runes and values you set under a name; every slot with all of those runes offers it as a
  button. Up to 10.
- **Works from a chest.** If the slot is empty in your pack, target a chest of those items near your Home rune; it works
  a few at a time and travels back for more as items break.
- **Keeps its tools and perk up.** It buys Rune Chisels from a Scribe when your stored charges fall below the target you
  set, and uses a Perk Deed from your chest when the Better Rune Crafting perk runs out.
- **Stays inside your weight limit** when Infinite Backpack Weight is not active: it stops crafting, or pulling items
  and runes out of storage, before the next one would go over.
- **Never runes a spellbook**, so it cannot break yours.
- **Updates itself if you let it.** With Check for updates on, it shows what changed in a newer version and asks first.

## What you need

- **300 Inscription** to apply runes. Crafting works at any skill, so a run below 300 still builds a stock of runes and
  stops before applying any.
- The **Better Rune Crafting** perk, active while runes are applied. The script uses a Perk Deed by itself when it runs
  out, from your pack or from your Perk Deed chest.
- In your backpack: your **Reagent Keys** and your **Runecrafting Storage** (holding the Rough Stone, blank runes,
  finished runes and Rune Chisel charges).
- For trips, two runes in one folder of your Account Runebook, named exactly:
  - **Home** -- beside your Perk Deed chest
  - **Scribe** -- beside a scribe who sells Rune Chisels
- Optional: **Infinite Backpack Weight**. With it, nothing watches your weight.

It does not check up front that you have enough gold or reagents. If a craft fails because you are short of either, the
script stops and says so.

## First run

A setup screen opens and checks everything above. Hover anything red for what it wants; green means ready.

1. Open your Account Runebook to the folder holding your Home and Scribe runes and press **Read**.
2. Stand by your Perk Deed chest, press **Target** on the Perk Deed Chest row and click the chest. It is found again by
   its name, so **if other chests near Home share that name** (every house chest starts out as "a glimmering chest of
   belongings"), **rename yours first** -- the script never opens a chest it can't tell apart.
3. Set **Rune Chisel Target** -- the charge balance to keep stocked. 10,000 is a fine default.

Your answers are saved, so this is once only.

## Using it

Press Play, pick an equipment slot, type a target value for each rune you want (leave the rest at 0) and press
**Calculate**. The preview shows the cost and the odds. From there:

- **Apply to <slot>** starts the run on every item of that slot.
- **Work N -- X%** starts it on only the N items likeliest to finish.
- **Suggested** starts it at the target the simulation says will finish.
- **Cancel** stops; nothing has been crafted or spent.

A boolean rune (Night Sight, Mage Armor, Spell Channeling and the like) is a checkbox: tick it for 1.

## Settings

On the setup screen. Every change is saved at once.

| Setting | What it does |
|---|---|
| Rune Chisel Target | How many chisel charges to keep in your Runecrafting Storage. Below it, a run buys more from the Scribe. |
| Calculations | On by default. Off: the run starts as soon as you submit, with no preview and no Suggested or Work buttons. |
| Check for updates | Off by default. On: at each start it looks for a newer version and shows what changed -- Update, Not now (asked again in 6 hours) or Skip this version. |
| Perk Deed Chest | Target the chest your spare Perk Deeds are kept in. |
| Account Runebook | Read the folder holding your Home and Scribe runes. |

## Its data folder

Next to the script, named after it (`Omni_Runecrafting`): your settings (`Setup.txt`), your templates
(`Templates.txt`) and the targets you last typed. An update keeps the old version of the script there too.

## Install

1. Download **Omni_Runecrafting.py** from the [latest release](../../releases/latest), or open the file above and use **Download raw file**.
2. Put it in your RazorEnhanced `Scripts` folder.
3. In RazorEnhanced, add it to your script list and press Play. The first run shows the setup screen.

## Update

With **Check for updates** on, press **Update** when the update window shows a newer version. An update is taken only
when its signature checks -- proof the author made it. With RazorEnhanced's **Auto Script Reload** ticked (Scripting
tab) the new version starts by itself; without it, press Refresh, then Play.

Or download the file again and replace the old one. Your settings live in the script's data folder, so they survive an
update. The [Releases](../../releases) page lists what changed in each version.

## Problems and ideas

Open an [issue](../../issues). Say its version, what you expected and what happened, and copy the lines
it printed in your journal.

## License

GNU General Public License v3.0 -- see [LICENSE](LICENSE). You may share and change this script; a changed version you hand out must stay under the same license, with its source.
