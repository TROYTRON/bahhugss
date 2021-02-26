[BAHHSCQ Nation Stats](https://docs.google.com/spreadsheets/d/1Q24q10s4prjF_WJb0rQBVoIWNEGoloshCUb2pn2M-oI/edit#gid=2095197382)

Behold, the product of a month's worth of research and number-crunching. This spreadsheet is not 100% complete due to my remaining uncertain about a few things, and some of the removed or reshuffled countries will obviously require access to a working map generator; but other than that, I should be able to paste all these numbers into the config and test it out once I get my hands on the game.

The regions list in particular is somewhat barebones right now, mostly due to insufficient information about how they work in TI and / or needing to do even *more* research to figure out an appropriate setting.

I'm going to take a break from numbers and try to draw some pretty graphics now.

## GDP and IPs

GDP numbers didn't change overly much from my first country-by-country analysis, and mostly went higher so that ~~fewer people would complain about their homeland's fate~~ they'd be considered more attractive to pursue. In a few cases I fudged the numbers so that nations would have 2 CPs instead of 1.

The amount of IPs I computed here does not quite match that shown in game screenshots, which makes me wonder what I'm missing. It does seem that changing from 1 month-turn to a 2 week-turn structure caused the number of IPs (and other resources) to vary between screenshots. But the amounts seem close enough to be indicative.

One interesting thing I noticed is that because IPs increase in proportion with GDP^(1/4), a doubling in GDP does not result in having double the IPs. This means it can actually be beneficial to keep nations balkanized in order to maximize the number of IPs.

The large thresholds for adding more CPs (it would take *seven* 2-CP nations to add up to a single 3-CP one!) also provide a compelling reason to keep nations balkanized, considering the planned UNSC mechanics where 1 CP = 1 vote.

Of course, the downside is that multiple smaller nations are easier for rival factions to pick off than one bigger one. And having more nations means more micromanagement.

## Democracy

TI's model of democracy conflates it with human rights, civil liberties, and economic liberalism. This works fine for the modern 2021 setting, where there *is* something of a correlation between these things - and also has the nice benefit of being able to point at Real Numbers:tm: and say "see, we're not biased!"

But it doesn't fit as well with the BAHHSCQ setting, where the means of production are centralized in Arcologies and almost entirely under UN control, completely decoupled from any human entrepeneurial spirit; where it is not only viable but actually optimal for decision-making to be centralized within a specialized, exclusive elite; where mass surveillance is not just necessary but literally impossible to avoid; and where the exigencies of war, the inherent transhumanist themes of the setting, and the more abstract visions of the five factions compared to TI's seven lead to greater motivation to push ethical boundaries and redefine what's *really* important in the human condition.

So I did the TNO thing and came up with my own democracy scale. With blackjack and hookers.

In the end, I don't think it made a huge amount of difference to the final ratings. Some nations went higher, some went lower, few flipped outright. Mostly, it just made it easier to evaluate certain countries with only one variable to take into account.

## Unrest

Took a wild stab at it based on the flavour text labels ("Peaceful", "Subversion", "Guerrilla War", "Civil War", etc.) and the associated lore for the nation.

It's noteworthy that even relatively small shifts in unrest can have a huge impact on a nation's available IPs.

## Higgs and STRATNET

Due to the de-emphasis on space in this scenario compared to TI, I am repurposing the Boost and Mission Control variables for regions.

Boost is being repurposed as Higgs. This will probably only be used during the brief window between discovering Higgs tech and the Antagonists appearing. Regions with Breaches will provide a Higgs income to their owner, and investing in the Higgs priority will make it bigger.

A neat side effect of this is that I can subsequently repurpose the "use Boost to build things in space without space resources" functionality as a "use Higgs to expedite construction" mechanic with hopefully not too much rejigging.

Mission Control is being repurposed as STRATNET. The actual gameplay effect of limiting a faction's ability to control habs and fleets is the same; the lore explanation is that STRATNET nodes represent humanity's capacity to collate, process, and store the huge amounts of data needed to run Arcologies and coordinate the war effort. As such, the pre-existing STRATNET markers are named after various prominent data centres and SIGINT stations. They provide a nice little prize as a reason to invest in certain regions, particularly the future war zones.

## Military

This is a tricky one I'm still not really sure about. My general schema for miltech goes something like this:
2.0 (Industrial Age): The nation possesses little more than light infantry militia with rifles and technicals.
3.0 (Atomic Age): The nation has a professional standing force, but it is either underdeveloped or missing some key capabilities.
4.0 (Information Age): The nation retains a modern force with full combined arms and reliable logistics.

There is also the issue of balance. Adding an army to a single-region nation effectively doubles its miltech (since the army must be engaged before the capital can be occupied), and there are a lot of single-region nations in this scenario.

Currently, East and South Asia are the most heavily militarized theatres on post-Impact Earth, with some 11 armies slugging it out plus 1 from Australia.
Africa comes second with a total of 7.
Western Asia and the Americas both have 2 armies each, and some middle powers start 50% towards building one.

3 of the world's 4 navies are in Asia. The general threshold for having one seems to be "operates aircraft carriers and / or has significant amphibious landing capability".

To prevent upsetting the existing balance of power, nobody starts with any nukes in this scenario. The IRL nuclear powers start 75% towards building one. The lore reason for this is that stockpiles were either lost or neglected in the post-Impact chaos, so there aren't enough nukes immediately operational to launch an effective strike.

## Education

Following JL's method, I used the Barro-Lee years-of-schooling dataset for 25 year olds, scaled to a maximum of 10. The resulting numbers were not quite the same as in TI, but close enough. In general, I used the data for 2000 rather than 2010, to represent most nations regressing due to Impact.

Some nations were not listed in the dataset. For those I just synthesized something based on their neighbours.

## Cohesion

For the most part I just pulled a number out of thin air based on ~~two minutes' Googling~~ *extensive research* on the country in question.

The various flavour text labels ("Sectarian", "Polarized", "Diverse", etc.) did a lot to inform where certain countries ended up.

## Inequality

For most nations, I used the World Bank Gini values divided by 10 as a baseline, as this seemed to match the numbers in TI. Most nations got a little bit worse after Impact. Some became vastly better or worse depending on their associated lore.

## Regions

Since I don't actually have the full list of TI regions, I usually just guessed their name based on what cities popped out on a world map. If a particular location was featured in BAHHSCQ, I would usually endeavour to name the region after it, with some exceptions. There is a trend in BAHHSCQ for Arcologies and Breaches to be named after the nearest prominent real-world city, even when that city has been flooded, which I stuck with for the most part, with various successor states being the main exception to this rule.

## Claims

These are initial claims meant to shape the various regional conflicts between nations in the post-Impact world. I kept these conservative, since a great number of claims will be unlocked by projects throughout the game.

## International Relations

These are not super easy to determine, especially in the chaos of the post-Impact world. One guideline I stuck to is that because of the loss of global communications and travel, most nations will initially not have any stance with anyone more than 1 nation away.

It's important to note that "allies" specifically refers to *military* alliances, with allied nations being allowed to station armies in each other's territory and obliged to defend each other in a war.

DD#5 describes "rivalry" as a requirement for nations to go to war, but I don't know how easy it is to change rival status in TI.

"Federations" have been described as close-knit groups of allies who share Money and Boost with each other. I am not sure how many of these sorts of organizations actually exist in real life. I also never got an answer as to if and how new federations are formed in the course of a campaign, so I'll hold off planning too many until I find out.

## National Orgs

As the name indicates, these are orgs for which you need to have a CP in the nation or a councilor originating there to buy. This is not an exhaustive list - I plan to reuse most of the ones from TI to save myself effort. The labels in parentheses indicate their intended purpose - most should be self-explanatory.

See if you can catch all the references.
