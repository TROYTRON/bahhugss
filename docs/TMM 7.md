# ARCOLOGY MECHANICS

As described in [DN#3](docs/TMM%203.md), Arcologies are intended to marry TI's vanilla space habitat mechanics with the Earth nation mechanics. This aims to represent the social and economic shifts that humanity's in-setting aggregation within such constructs implies, as well as the increasing political and economic power taken on by Valkyries and the factions they represent.

Since mechanics from both halves of the game are involved, I figured it would be good to include a refresher on how some of those work.

## NATION STATS

Described in [DD#4](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=27816).

The dev diary already explains it pretty well, so I'll just leave it there.

More info about how the stats are implemented in this scenario can be found in [DN#5](docs/TMM%205.md).

### National Priority Investment

Described in [DD#5](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=27839&sid=4037ec51f9d957808cc86e652836f04c).

Nations in TI have a certain amount of Investment Points (IPs) available, effectively their budget, which factions can direct towards filling up various priority "buckets". When the bucket is full, the priority is considered complete, and some effect takes place in the nation (usually a stats change).

Some Arcology modules will provide a bonus to national investments. This means that factions with such bonuses are able to fill up the buckets faster, triggering the relevant effects for completing the priority more often.

In addition to IPs, factions can also Direct Invest, which allows them to spend Money to instantly fill priority buckets.

The scenario mostly retains the same set of priorities as TI, with a few additions and modifications.

| Priority | Effects | Notes |
| --- | --- | --- |
| Economy | +GDP per capita increases.<br>-Inequality increases.<br>-Environmental damage increases. | Unchanged from TI. |
| Welfare | +Inequality decreases.<br>+Environmental damage decreases. | Unchanged from TI. |
| Resettlement | +Moves population from "refugees" to "citizens" status. | New priority. See below for explanation of population mechanics. |
| Knowledge | +Democracy increases.<br>+Education increases.<br>+Cohesion moves towards 5.<br>-Inequality increases. | Mostly the same as in TI, with the addition of a small Inequality penalty reflecting academic elitism and the diversion of resources towards "ivory tower" vanity projects. |
| Unity | +Cohesion increases.<br>-Democracy decreases.<br>+Public Opinion moves towards controlling faction(s). | Unchanged from TI. |
| Military | +If Unrest is low, Miltech score increases.<br>+If Unrest is high, Unrest decreases. | Unchanged from TI. |
| Spoils | +Grants huge lump sum of Money to controlling faction(s).<br>-Democracy decreases.<br>-Inequality increases.<br>-Environmental damage increases. | Unchanged from TI. |
| Funding | +Annual Money income increases.<br>-Cohesion decreases. | Similar to TI, but with a small Cohesion penalty to represent divided opinions about where the cash ends up. Might end up removing this priority altogether. |
| Higgs | +Higgs income from Breaches increases. | Required tech: _Higgs Particle Extraction_.<br>Replaces "Boost" priority from TI, as the Boost resource is repurposed in this scenario.<br>Note that this priority is only available during the Higgs Golden Age. It becomes unavailable upon the Antagonists' arrival. |
| STRATNET | +STRATNET capacity increases by 1. | Rebranded "Mission Control" priority from TI. Otherwise functions identically. |
| Build Army | +Nation gains one new conventional army. | Required tech: _Military Salvage_.<br>Each non-colony region in a nation can support one conventional army. |
| Build Navy | +One conventional army in this nation gains a navy. | Required tech: _International Trade and Travel_.<br>Navies allow armies to travel overseas. |
| Nuclear Weapons | +Nation gains one nuke. | Required tech: _Strategic Deterrence_. |
| Fortifications | +One region in this nation gains a fortification. | Required tech: _Regional Defense Doctrine_.<br>Rebranded "Space Defences" priority from TI. STO defenses still function the same way, but now also grant defensive combat bonuses to friendly armies stationed in the region. Can also be repeated multiple times to improve the bonus. |

## FACTION RESOURCES

Described in [DD#3](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=27135&sid=d0f4d4feb17e5e0597b4ba068021b582).

Remains mostly the same as in vanilla TI, with some changes to account for the differences in setting.

### Earth Resources

| Resource | Sources | Uses | Notes |
| --- | --- | --- | --- |
| Money | Councillors, nations, Arcology modules. | Allows factions to Direct Invest in nations.<br>Can be spent to rush-build warships and Arcology modules. | --- |
| Influence | Councillors, nations, Arcology modules.<br>Nations provide factions with Influence income based on Public Opinion. | Used for recruiting councillors, purchasing orgs, subverting nations, and conducting diplomacy. | --- |
| Ops | Councillors, Arcology modules. | Spent to perform salvage and special operations. | --- |
| Higgs | Breaches in nations provide Higgs during the Higgs Golden Age (pre-Antagonists only).<br>Destroying Antagonist Type Zeroes and Hives distributes Higgs income to participating factions.<br>United Nations member nations receive a small Higgs income. | Can be spent to rush-build warships and Arcology modules, and is required to build and operate some of them.<br>Used for various Valkyrie-related applications, such as upgrading Valkyrie-councillors and Valkyrie-armies. | Repurposed Boost from TI. |
| STRATNET | Councillors, nations, Arcology modules.<br>STRATNET Nodes can be built in nations and Arcologies. | Limits the number of Arcologies, warships, and Valkyrie-armies the faction may safely control.<br>Exceeding the limit results in various penalties. | Rebranded Mission Control from TI. Otherwise identical. |
| Research | Councillors, nations, Arcology modules. | Allocated towards researching global public techs or faction private projects. | --- |
| Projects | Councillors, Arcology modules. | Multiplies research speed of faction private projects.<br>Orgs with +Project income unlock the faction's 2nd project slot.<br>Arcology modules with +Project income unlock the faction's 3rd project slot. | --- |

### Arcology Resources

Arcology resources are produced in Earth regions by Arcologies and distributed to the faction pool. They are expected to be used for building, upgrading, and maintaining nice things such as Arcology facilities, Valkyrie-armies, and space warships. They can also be sold off for quick cash.

| Resource | Sources | Uses | Notes |
| --- | --- | --- | --- |
| Water | Availability in regions varies based on typical moisture levels. | Used for supporting Arcology populations, fusion and warship fuel, and various industrial applications. | --- |
| Volatiles | Definition expanded to include things like industrial gases and specialty chemicals.<br>Available in regions with natural gas and shale gas reserves. | Used for fuel, munitions, and industrial applications. | --- |
| Metals | Availabile in regions with iron, nickel, and copper deposits. | Used for manufacturing most things, particularly heavy machinery.  | --- |
| Nobles | Availabile in regions with deposits of gold and rare earth elements. | Key component in computers, electronics, batteries, and  | --- |
| Fissiles | Available in regions with deposits of uranium, plutonium, and thorium. | Used for nuclear fission, which is handy for powering Arcology modules, warships, and early Valkyries. | --- |
| Antimatter | Manufactured in small quantities by certain Arcology modules. | Used to power advanced warships, weapons, and Valkyries. | --- |
| Exotics | Manufactured in small quantities by certain Arcology modules.<br>Can also be looted from Antagonists. | Used for all sorts of esoteric and specialist applications. | --- |

### Research Categories

More information on how research works in TI can be found in [DD#10](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=28950&sid=a3e1d2d6c88da0a7164062b896c82dc0).

- Infrastructure.
- Valkyries.
- Energy.
- Materials.
- Information.
- Biotechnology.
- Social Science.
- Military Science.
- Antagonists.

The current planned tech tree for this scenario is [here](BAHHSCQ%20Tech%20Tree-Techs%203c.png).

# PROPOSED ARCOLOGY MODULES

TODO
