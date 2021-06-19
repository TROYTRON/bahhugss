# ARCOLOGY MECHANICS

As described in [DN#3](docs/TMM%203.md), Arcologies are intended to marry TI's vanilla space habitat mechanics with the Earth nation mechanics. This aims to represent the social and economic shifts that humanity's in-setting aggregation within such constructs implies, as well as the increasing political and economic power taken on by Valkyries and the factions they represent.

Since mechanics from both halves of the game are involved, I figured it would be good to include a refresher on how some of those work.

## NATION STATS

Described in [DD#4](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=27816).

The dev diary already explains how nations work pretty well, so I'll just leave it there. More info about how the stats are implemented in this scenario can be found in [DN#5](docs/TMM%205.md).

One derived stat I am considering adding is **Secrecy**, similar to the Elite Dissatisfaction derived stat that can be seen in [this screenshot](https://discord.com/channels/462769550841348126/606164360720809984/763414372281352232). Secrecy would affect the propensity of information leaks, the ability for councillors or special forces to act freely within the nation, and possibly other things. Higher Democracy would reduce Secrecy, while higher Cohesion would raise it.

I also plan to add a new **Morale** stat for armies, which complements Miltech and likewise affects their combat efficacy. Individual armies can gain Morale from fighting and surviving battles, from the presence of certain Arcology modules in their headquarters region, and possibly from some faction projects or global events.

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
| Resettlement | +Moves population from "refugees" to "citizens" status. | New priority. See below for explanation of population mechanics.<br>Disregard is unable to invest in this priority. |
| Knowledge | +Democracy increases.<br>+Education increases.<br>+Cohesion moves towards 5.<br>-Inequality increases.<br>Overfunding Knowledge reduces the nation's Secrecy. | Mostly the same as in TI, with the addition of a small Inequality penalty reflecting academic elitism and the diversion of resources towards "ivory tower" vanity projects. |
| Unity | +Cohesion increases.<br>-Democracy decreases.<br>+Public Opinion moves towards controlling faction(s). | Unchanged from TI. |
| Military | +If Unrest is low, Miltech score increases.<br>+If Unrest is high, Unrest decreases. | Unchanged from TI. |
| Spoils | +Grants huge lump sum of Money to controlling faction(s).<br>-Democracy decreases.<br>-Inequality increases.<br>-Environmental damage increases.<br>Underfunding Spoils causes dissatisfied elites, increasing the risk of a coup. | Unchanged from TI. |
| Funding | +Annual Money income increases.<br>-Cohesion decreases. | Similar to TI, but with a small Cohesion penalty to represent divided opinions about where the cash ends up. Might end up removing this priority altogether. |
| Higgs | +Higgs income from Breaches increases. | Required tech: _Higgs Particle Extraction_.<br>Replaces Boost priority from TI, as the Boost resource is repurposed in this scenario.<br>Note that this priority is only available during the Higgs Golden Age. It becomes unavailable upon the Antagonists' arrival. |
| STRATNET | +STRATNET capacity increases by 1.<br>-Democracy decreases. | Rebranded Mission Control priority from TI. Democracy penalty reflects increased elite control over society enabled by STRATNET.<br>Note that the Democracy decrease from this priority is a one-time event, compared to the continuous-over-time decrease from STRATNET Nodes in Arcologies. |
| Build Army | +Nation gains one new conventional army. | Required tech: _Military Salvage_.<br>Each non-colony region in a nation can support one conventional army.<br>Excess armies are held in reserve, being automatically deployed if an existing army is destroyed. |
| Build Navy | +One conventional army in this nation gains a navy. | Required tech: _International Trade and Travel_.<br>Navies allow armies to travel overseas.<br>Excess navies are held in reserve, and will be assigned to reserve armies that are deployed. |
| Nuclear Weapons | +Nation gains one nuclear barrage. | Required tech: _Strategic Deterrence_. |
| Fortifications | +One region in this nation gains a fortification. | Required tech: _Regional Defense Doctrine_.<br>Rebranded "Space Defences" priority from TI. STO defenses still function the same way, but now also grant defensive combat bonuses to friendly armies stationed in the region. Can also be repeated multiple times to improve the bonus. |

### Population Mechanics

The scenario divides regional populations into three categories: citizens, refugees, and Arcology.

**Citizens** are considered to be the "standard" population for the purposes of TI's nation mechanics.

**Refugees** depict the social pressures caused and experienced by refugees in the BAHHSCQ setting. They are created when warfare, instability, and other disasters cause region populations to flee into neighbouring regions; many nations will have a random number of refugees resulting from Impact at scenario start. Existing refugees may also migrate to neighbouring regions if the conditions there are favourable.

Refugees do not contribute to GDP, and are not considered in GDPpc calculations; but their presence in a nation corrodes all the nice stats, especially Inequality and Cohesion (and thus Unrest). This can be averted by investing in the Resettlement priority, or by having Valkyries and armies perform the Reconstruction mission, both of which move a number of refugees to the citizens category.

Note that nations controlled by Disregard will not admit _any_ refugees, while nations controlled by Enlighten will admit double.

**Arcology** populations are those who live inside Arcologies. Residential modules be built to house them, which will drain population from the citizens category over time (and then refugees, if no citizens are present). If an Arcology's population ever exceeds its residential capacity, the excess population is immediately kicked out and resigned to refugee status, making the sabotage of residential modules a nice way to destabilize a nation.

Arcology populations are safe from most depradations and more prosperous than ordinary citizens, improving the nation's Money and Research outputs; but they are very sensitive to drops in living standards, and highly susceptible to propaganda.

## FACTION RESOURCES

Described in [DD#3](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=27135&sid=d0f4d4feb17e5e0597b4ba068021b582).

Remains mostly the same as in vanilla TI, with some changes to account for the differences in setting.

### Earth Resources

| Resource | Sources | Uses |
| --- | --- | --- |
| Money | Councillors, nations, Arcology modules. | Allows factions to Direct Invest in nations.<br>Can be spent to rush-build warships and Arcology modules. |
| Influence | Councillors, nations, Arcology modules.<br>Nations provide factions with Influence income based on Public Opinion. | Used for recruiting councillors, purchasing orgs, subverting nations, and conducting diplomacy. |
| Ops | Councillors, Arcology modules. | Spent to perform salvage and special operations. |
| Higgs | Breaches in nations provide Higgs during the Higgs Golden Age (pre-Antagonists only).<br>Destroying Antagonist Type Zeroes and Hives distributes Higgs income to participating factions.<br>United Nations member nations receive a small Higgs income. | Can be spent to rush-build warships and Arcology modules, and is required to build and operate some of them.<br>Used for various Valkyrie-related applications, such as upgrading Valkyrie-councillors and Valkyrie-armies. | Repurposed Boost from TI. |
| STRATNET | Councillors, nations, Arcology modules.<br>STRATNET Nodes can be built in nations and Arcologies. | Limits the number of Arcologies, warships, and Valkyrie-armies the faction may safely control.<br>Exceeding the limit results in various penalties. |
| Research | Councillors, nations, Arcology modules. | Allocated towards researching global public techs or faction private projects. |
| Projects | Councillors, Arcology modules. | Multiplies research speed of faction private projects.<br>Orgs with +Project income unlock the faction's 2nd project slot.<br>Arcology modules with +Project income unlock the faction's 3rd project slot. |

### Arcology Resources

Arcology resources are produced in Earth regions by Arcologies and distributed to the faction pool. They are expected to be used for building, upgrading, and maintaining nice things such as Arcology facilities, Valkyrie-armies, and space warships. They can also be sold off for quick cash.

| Resource | Sources | Uses |
| --- | --- | --- |
| Water | Availability in regions varies based on typical moisture levels. | Used for supporting Arcology populations, fusion and warship fuel, and various industrial applications. |
| Volatiles | Definition expanded to include things like industrial gases and specialty chemicals.<br>Available in regions with natural gas and shale gas reserves. | Used for fuel, munitions, and industrial applications. |
| Metals | Availabile in regions with iron, nickel, and copper deposits. | Used for manufacturing most things, particularly heavy machinery.  |
| Nobles | Availabile in regions with deposits of gold and rare earth elements. | Key component in computers, electronics, batteries, and energy infrastructure. |
| Fissiles | Available in regions with deposits of uranium, plutonium, and thorium. | Used for nuclear fission, which is handy for powering Arcology modules, warships, and early Valkyries. |
| Antimatter | Manufactured in small quantities by certain Arcology modules. | Used to power advanced warships, weapons, and Valkyries. |
| Exotics | Manufactured in small quantities by certain Arcology modules.<br>Can also be looted from Antagonists. | Used for all sorts of esoteric and specialist applications. |

### Research Categories

TI's research mechanics are described in [DD#10](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=28950&sid=a3e1d2d6c88da0a7164062b896c82dc0).

The current planned tech tree for this scenario is [here](BAHHSCQ%20Tech%20Tree-Techs%203c.png).

Techs and projects are planned to be divided into nine categories:
- Infrastructure.
- Valkyries.
- Energy.
- Materials.
- Information.
- Biotechnology.
- Social Science.
- Military Science.
- Antagonists.

Some Arcology modules will provide bonuses to specific research categories, effectively multiplying Research output for those categories. Notably, these bonuses stack *geometrically*, creating an incentive for factions to specialize their research instead of generalizing.

# PROPOSED ARCOLOGY MODULES

## Module Attributes

Terra Invicta's hab mechanics are described in [DD#13](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=28980&sid=6fc72d17246d07bd0cce2446f108e275).

**Defense rating**: This determines how strongly the Arcology will resist external invasion attempts. Councillors belonging to the controlling faction (or its allies) will also benefit from an Arcology's Defense rating while they are inside it.

**Atrocity module**: The functions of these modules are considered an atrocity and thus kept secret. If the module is ever destroyed (e.g. by a councillor sabotaging it), its existence will be revealed, and the controlling faction suffers an atrocity event and corresponding Public Opinion loss. Alternatively, disgruntled employees in low-Secrecy nations may randomly leak the facility's existence, Snowden-style.

Note that all proposed stats are merely indicative and subject to change.

## Basic Modules

| Module | Required Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- |

## General Modules

| Module | Required Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- |

## Power Modules

| Module | Required Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- |

## Habitation Modules

| Module | Required Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- |

Biome:
-	Required tech: Arcology Living.
-	Upgrade tech: Environmental Stewardship.
-	I don’t really know what this should do mechanics-wise, but this should be here for setting reasons.

Hydroponics:
-	Required tech: Economies of Density.
-	Something to do with food? Water and Volatiles?


## Science Modules

| Module | Required Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- |

## Military Modules

| Module | Required Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- |

## Valkyrie Modules

| Module | Required Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- |

## United Nations Modules

These modules gain significantly increased stats if the controlling faction owns the respective org.

| Module | Required Tech | Upgrade Tech | Construction | Production | Maintenance | Research Bonuses | Investment Bonuses | Effects |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| UNESCO Heritage Site | Environmental Stewardship | --- | --- | +(+)Research | --- | --- | +(++)Knowledge | --- |
| UNARD Design Bureau | Technological Optimization<br>Network Effects | --- | --- | +(+)Projects | --- | +(++)Military Science | +(+)Military | --- |
| UNDHMOR Distribution Centre | Post-Scarcity Economics | --- | --- | +(+++)Money<br>+Higgs | --- | --- | +(+)Economy<br>(+)Welfare | --- |
| UNHCR Branch Office | Arcology Living | --- | --- | --- | --- | +(++)Infrastructure | +(+)Welfare<br>+(++)Resettlement | Increases this Arcology’s maximum population size. |
| UNPO Station | Arcology Living | --- | --- | +(++)Ops | --- | --- | --- | (+)Defence rating.<br>Improves the rate of Unrest decreases in this nation. |
| UNOMI Listening Post | Self-Adapting Algorithms | --- | --- | +(++)Influence | --- | +(++)Social Science | +(+)STRATNET | Improves this nation’s Secrecy value. |






