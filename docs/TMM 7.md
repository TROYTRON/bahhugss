**DISCLAIMER**: Due to the nature of closed beta, I have made sure to include public sources for all relevant information about Terra Invicta's mechanics. Any divergence from those sources is purely speculative thinking on my part related to the scenario, and does not reflect anything about the actual state of the game.

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
| Resettlement | +Moves population from "refugees" to "citizens" status. | New priority. See below for explanation of population mechanics.<br>Not available to Disregard. |
| Knowledge | +Democracy increases.<br>+Education increases.<br>+Cohesion moves towards 5.<br>-Inequality increases.<br>Overfunding Knowledge reduces the nation's Secrecy. | Mostly the same as in TI, with the addition of an Inequality penalty reflecting academic elitism and the diversion of resources towards "ivory tower" vanity projects. |
| Unity | +Cohesion increases.<br>-Democracy decreases.<br>+Public Opinion moves towards controlling faction(s). | Unchanged from TI.<br>Not available to Self-Sustain. |
| Military | +If Unrest is low, Miltech score increases.<br>+If Unrest is high, Unrest decreases. | Unchanged from TI. |
| Spoils | +Grants huge lump sum of Money to controlling faction(s).<br>-Democracy decreases.<br>-Inequality increases.<br>-Environmental damage increases.<br>Underfunding Spoils causes dissatisfied elites, increasing the risk of a coup. | Unchanged from TI.<br>Not available to Enlighten. |
| Funding | +Annual Money income increases.<br>-Cohesion decreases. | Similar to TI, but with a small Cohesion penalty to represent divided opinions about where the cash ends up. Might end up removing this priority altogether. |
| Higgs | +Higgs income from Breaches increases. | Required tech: _Higgs Particle Extraction_.<br>Replaces Boost priority from TI, as the Boost resource is repurposed in this scenario.<br>Note that this priority is only available during the Higgs Golden Age. It becomes unavailable upon the Antagonists' arrival. |
| STRATNET | +STRATNET capacity increases by 1.<br>-Democracy decreases. | Rebranded Mission Control priority from TI. Democracy penalty reflects increased elite control over society enabled by STRATNET.<br>Note that the Democracy decrease from this priority is a one-time event, compared to the continuous-over-time decrease from STRATNET Nodes in Arcologies. |
| Build Arcology | +An Arcology is constructed in a region in this nation. | Required tech: _Arcology Construction_.<br>The capital is selected first, then coreEco regions, then descending by population. |
| Build Army | +Nation gains one new conventional army. | Required tech: _Military Salvage_.<br>Each non-colony region in a nation can support one conventional army. |
| Build Navy | +One conventional army in this nation gains a navy. | Required tech: _International Trade and Travel_. |
| Nuclear Weapons | +Nation gains one nuclear barrage. | Required tech: _Strategic Deterrence_. |
| Fortifications | +One region in this nation gains a fortification. | Required tech: _Regional Defense Doctrine_.<br>Rebranded "Space Defences" priority from TI. STO defenses still function the same way, but now also grant defensive combat bonuses to friendly armies stationed in the region. |

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

### Political Resources

| Resource | Sources | Uses |
| --- | --- | --- |
| Money | Councillors, nations, Arcology modules. | Allows factions to Direct Invest in nations.<br>Can be spent to rush-build warships and Arcology modules. |
| Influence | Councillors, nations, Arcology modules.<br>[Nations provide factions with Influence income based on Public Opinion.](https://www.pavonisinteractive.com/phpBB3/viewtopic.php?f=7&t=28083&sid=228110f05d74650747999ac6e9711bca) | Used for recruiting councillors, purchasing orgs, subverting nations, and conducting diplomacy. |
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

**Shipyard**: This module allows space warships to be constructed and housed at the Arcology. These are typically located in space for efficiency and balance reasons.

**Factory module**: The presence of this module allows the controlling faction to manually construct Arcologies on Earth (as opposed to using the Build Arcology priority).

**Atrocity module**: The functions of these modules are considered an atrocity and thus kept secret. If the module is ever destroyed (e.g. by a councillor sabotaging it), its existence will be revealed, and the controlling faction suffers an atrocity event and corresponding Public Opinion loss. Alternatively, disgruntled employees in low-Secrecy nations may randomly leak the module's existence.

Note that all proposed stats are merely indicative and subject to change.

## Basic Modules

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| Extractor | --- | --- | --- | --- | One per Arcology.<br>Rebranded Mines from TI. Self-explanatory: it provides output of the Arcology resources available in that region. |
| Condenser | Atmospheric Refactoring | --- | ++Water<br>-Power | --- | Produces large quantities of Water, since that’s so abundant on Earth. |
| Refinery / Chemical Plant | _Fossil Fuel Extraction_<br>Chemical Synthesis | ++Volatiles<br>-Power | --- | --- | Produces large quantities of Volatiles, since they're so abundant on Earth. |
| Residential Tower | --- | --- | ---Water<br>-Volatiles<br>--Power | --- | Increases this Arcology’s maximum population size, facilitating a drain from this nation’s citizen and refugee populations.<br>Note that simply cramming millions of humans inside Arcologies without proper facilities should be very detrimental.<br>Note that Arcology population drains Water and Volatiles from the faction resources. |
| STRATNET Node | _Satellite Communications_<br>Wider Arcology Network<br>Self-Adapting Algorithms<br>Expert Systems<br>Artificial General Intelligence | --- | +STRATNET<br>+Projects<br>-Power | +Infrastructure<br>+Information | Boosts this nation’s GDP growth.<br>Armies stationed in this region fight more effectively.<br>Corrodes Democracy over time in this nation. |

## General Modules

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| Nerve Stapler | _Neural Restructuring_ | --- | --- | +++Unity | One per Arcology.<br>Atrocity facility.<br>All your Unrest problems will be solved forever, at the small cost of reducing your entire population to mindless drones! Not that it would be so undesirable for some factions...<br>This nation’s Cohesion cannot fall below 10 * regions with staplers / total regions.<br>Corrodes Democracy over time in this nation. |
| Neuromod Fabricator | _Expedited Education_ | --- | -Nobles<br>-Exotics<br>--Power<br>-Population | --- | Atrocity facility.<br>Reduces costs for augmenting councillors and upgrading armies.<br>The army headquartered in this region receives one morale level.<br>Improves the rate of Education increases in this nation. |
| Environmental Regenerator | _Environmental Stewardship_ | --- | --Water<br>--Volatiles<br>-Power | --- | Improves the rate of environmental repair in this nation. |
| Cryptominer | _Non-Linear Mathematics_ | ---Nobles | ++++Money<br>---Power | +++Spoils | Makes mega money and does little else. |
| Nanorecycler | _Arcology Living<br>Industrial Nanorobotics_ | --- | -Population | +++Spoils<br>+Fortifications | Atrocity facility.<br>Reduces drains of Metals and Nobles. |
| Fabrication Chamber | _Industrial Nanorobotics_<br> | Exotic Matter Manipulation<br>Atomic Assembly<br>Subatomic Assembly | --- | ++Economy<br>+Build Army<br>+Fortifications | Boosts this nation’s GDP growth. |
| Universal Constructor | _Subatomic Assembly<br>Exotic Matter Manipulation_<br>Matter Supercompression<br>Directed Optimization | --- | +Exotics<br>--Water<br>--Volatiles<br>--Metals<br>--Nobles<br>---Power | +++Economy<br>+Build Army<br>++Fortifications | Counts as a shipyard and a factory module.<br>Boosts this nation’s GDP growth.<br>Provides discount to space warship construction. |
| Individual Utility Maximizer | _Post-Scarcity Economics_<br>Integrated Logistics<br>Inter-Human Networking | --- | --- | +Infrastructure<br>+Social Science<br>++Welfare | Calculates the exact optimum distribution of goods in order to ensure that all citizens receive exactly what they need to attain maximum satisfaction.<br>Improves the rate of Inequality decreases in this nation.<br>Corrodes Democracy over time in this nation. |
| Automated Dockyards | _Expert Systems<br>Naval Warfare Doctrine_ | --- | --- | ++Economy<br>++Build Navy | Can only be built in Arcologies in coastal regions.<br>The army headquartered in this region receives one morale level if it has a navy attached. |
| Maritime Control Centre | _Linear-Superpolynomial Equivalence<br>Naval Warfare Doctrine_ | --- | --- | +++Build Navy | Can only be built in Arcologies in coastal regions.<br>The army headquartered in this region receives one morale level if it has a navy attached.<br>Each MCC built in this nation geometrically increases naval score. |
| Space Elevator | _Mission to Orbit<br>Exotic Matter Manipulation_ | ---Power | +++Economy | --- | One per Arcology.<br>Provides massive industrial boost to this nation and Arcology.<br>Boosts this nation’s GDP growth.<br>Provides discount to space warship construction. |
| Shipping Coordinator | _Wider Arcology Network_<br>Integrated Logistics | --- | +Population<br>-Power | +Social Science | Increases population growth in this nation. |
| Exowomb Array | _Protein Synthesis_<br>Germline Modification<br>Expedited Education | --- | ++Population<br>--Water<br>--Volatiles<br>--Power | --- | Massively increases population growth in this nation. |
| Cloning Vats | _Subatomic Assembly_ | --- | +++Population<br>---Water<br>---Volatiles<br>---Power | --- | Vastly increases population growth in this nation. |
| Augmentation Clinic | _Retroviral Modification_ | --- | --- | +Economy | The army headquartered in this region receives one morale level. |
| Cyborg Factory | _Mind-Machine Interface_<br>Inter-Human Networking | --- | --- | +Economy<br>+Knowledge | The army headquartered in this region receives one morale level. |
| Demarchy Coordinator | _Wider Arcology Network_<br>Mind-Machine Interface<br>Inter-Human Networking | --- | --- | +Infrastructure<br>++Social Science | Significantly improves Democracy in this nation over time. |

## Power Modules

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| Solar Array | _Renewable Energy Paradigm_<br>Atmospheric Refactoring | -Nobles | +Power | --- | Cheap and basic power generation module.<br>Receives massive boosts with the development of orbital power transmitters, each of which this faction controls in orbit providing a bonus to this module’s Power output. |
| Fission Reactor | _Mineral Resource Prospecting_ | -Metals, --Fissiles | ++Power<br>-Water<br>-Fissiles | --- | Interim power plant in the event that solar doesn’t cut it and your faction misses out on fusion power for whatever reason.<br>Fissiles drain can be reduced with breeding and recycling projects, making it vaguely more competitive with fusion which consumes MEGA Water. |
| Fusion Reactor | _Nuclear Fusion Power_<br>Exotic Matter Manipulation<br>Antimatter Production | ---Water<br>-Metals<br>--Nobles | +++Power<br>---Water | --- | I’m not actually sure if there are any real differences between an ICF and a MCF reactor. I think it’d be popamole to have to weigh up more than one, anyway.<br>It might be better to handle it as being chance based. Fusion power has a low chance to be unlocked, but you have three chances: ICF, MCF, and Z-pinch. If nobody unlocks it, you’ll be stuck with solar and fission for life.<br>Also, fusion reactors are fail-deadly in BAHHSCQ. If someone sabotages them, they will take out another module in the explosion. |
| Higgs Generator | _Higgs Particle Extraction_ | --Higgs | ++Higgs<br>+++Power | +Higgs | One per Arcology. |

## Residential Modules

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| Biome | _Arcology Living_<br>Environmental Stewardship | --- | --- | --- | I don’t really know what this should do mechanics-wise, but this should be here for setting reasons. |
| Hydroponics Chamber | _Economies of Density_ | --- | --Water<br>--Volatiles<br>--Power | --- | Multiplies existing Arcology residential capacity. |

## Science Modules

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| Medical Laboratory | _Biological Optimization_<br>Retroviral Modification | --- | -Power<br>-Population | +++Biotechnology | Atrocity module.<br>Armies repair notably faster when stationed in this region. |
| High Yield Weapons Laboratory | _Strategic Deterrence_<br>Antimatter Production | --- | --Fissiles<br>---Power | ++Energy<br>++Nuclear Weapons | Drains Fissiles stockpiles in exchange for accelerating the construction of nukes in this nation.<br>Enables Valkyrie-armies to be equipped with nukes (manifesting as great improvements in combat performance). |
|	Exotic Physics Laboratory | _Exotic Matter Manipulation_ | --- | +Exotics<br>--Nobles<br>--Power | ++Materials<br>+Antagonists | --- |
| Supercollider | _Antimatter Production_ | --- | +Antimatter<br>---Fissiles<br>---Power | +++Energy<br>++Knowledge | --- |

## Military Modules

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| Special Forces Platoon / Barracks | --- | --- | ++Ops | --- | +Defence rating.<br>Rebranded Marines from TI. These can’t directly assault other Arcologies, but they can sabotage region facilities and Arcology modules without any direct councillor involvement. And, of course, prevent other factions from doing the same.<br>Armies stationed in this region fight more effectively.<br>The army headquartered in this region receives one morale level. |
| SAM Complex / Integrated Air Defence System | _Air Warfare Doctrine_ | --- | --- | --- | ++Defence rating.<br>Hostile Valkyrie-armies and Type Zeroes take more damage attempting to assault this Arcology.<br>Counters the effects of Antagonist Type 5 army upgrades. |
| Drone Printer | _Expert Systems<br>Industrial Nanorobotics<br>Ground Warfare Doctrine_ | --- | --- | +Military<br>+Build Army | Armies repair notably faster when stationed in this region. (Army repair rates will be somewhat reduced from vanilla TI – all of that fancy tech doesn’t replenish itself for free!)<br>The army headquartered in this region receives one morale level. |
| Strategic Yield Weapon | _Strategic Deterrence_ | ---Fissiles<br>--Higgs | -Fissiles<br>-Power | --- | One per Arcology.<br>Atrocity facility.<br>Hugely expensive trinket that acts as a deterrent against Arcology invasion. Any attempt to invade with conventional forces results in the offending faction having its headquarters and surrounding region(s) burned to a fine molecular crisp.<br>Cannot be manually activated (to prevent player abuse and having to add new buttons to the menu). Useless against Antagonists without further research. Prime sabotage target. |
| Interdiction Field | _Advanced Impeller Techniques<br>Higgs-Impeller Substitution<br>Arcology Defence Doctrine_ | --- | -Higgs<br>---Power | --- | +++Defence rating.<br>Prevents all hostile teleportation within this region.<br>Armies stationed in this region fight more effectively. |
| Strategic Teleporter | _Bulk Matter Transmission_ | --- | --- | --- | One per Arcology.<br>Allow friendly armies stationed in this region to instantly teleport to any other friendly Arcology with a Strategic Teleporter.<br>A friendly Arcology is defined as: host nation is allied with this nation; controlling faction is the same or is allied with controlling faction of this Arcology.<br>All linked Arcologies will receive more refugees in the event that this Arcology is besieged and destroyed, increasing survival rate. |

## Valkyrie Modules

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| Valkyrie Academy | _Valkyrie Core Militarization_<br>Air Warfare Doctrine<br>Valkyrie Psychology Studies<br>Directed Optimization | --- | +Ops<br>-STRATNET | +Valkyries | +++Defence rating.<br>Allows this Arcology to host one Valkyrie-army.<br>If a faction has more Valkyrie-armies than Valkyrie Academies, all enemy attempts to subvert this Arcology gain a significant bonus.<br>Reduce XP costs for augmenting Valkyrie-councillors. |
| Higgs Simulator | _Advanced Impeller Techniques<br>Higgs-Impeller Substitution_<br>Subjective Experience Studies | --- | -Higgs<br>---Power | --- | Reduce XP and Higgs costs for augmenting Valkyrie-councillors.<br>Valkyrie-armies headquartered in this Arcology receive one free morale level. |
| Elite Classroom | _Intermediate Impeller Techniques<br>Valkyrie Psychology Studies_<br>Directed Optimization | --- | --- | --- | +++Defence rating.<br>Valkyrie-armies headquartered in this Arcology receive one free morale level. |
| Architecture Classroom | _Valkyrie Construction Framework_<br>Atomic Assembly | --- | +Projects | +++Infrastructure<br>++Materials<br>++Resettlement | --- |
| Crafting Classroom | _Exotic Matter Manipulation_<br>Matter Supercompression<br>Directed Optimization | --- | +Projects<br>---Metals<br>--Nobles<br>-Exotics | +Infrastructure<br>+++Materials<br>+Antagonists<br>++Knowledge | --- |
| Demolitions Classroom | _Air Warfare Doctrine_<br>Superstring Theory<br>Antimatter Production | --- | +Ops<br>+Projects<br>---Volatiles<br>--Fissiles | +Valkyries<br>+++Military Science<br>+Antagonists<br>+Knowledge<br>+Military | --- |
| Electronics Classroom | _Quantum Computing_<br>Linear-Superpolynomial Equivalence | --- | +Projects<br>--Metals<br>---Nobles<br>-Exotics | +Infrastructure<br>+Materials<br>+++Information<br>+Knowledge<br>+STRATNET | --- |
| Gambling Classroom | _Chaos Theory_<br>Probability Mechanics | --- | +Projects<br>-STRATNET<br>---Power | +Information<br>++++Social Science<br>+Knowledge<br>+Unity | --- |

## United Nations Modules

These modules gain significantly increased stats if the controlling faction owns the respective org.

| Module | _Required Tech_<br>Upgrade Tech | Construction | Production & Maintenance | Research & Investment Bonus | Effects & Notes |
| --- | --- | --- | --- | --- | --- |
| UNESCO Heritage Site | _Environmental Stewardship_ | --- | --- | +(+)Research | +(++)Knowledge | --- |
| UNARD Design Bureau | _Technological Optimization<br>Network Effects_ | --- | +(+)Projects | +(++)Military Science<br>+(+)Military | --- |
| UNDHMOR Distribution Centre | _Post-Scarcity Economics_ | --- | --- | +(+++)Money<br>+Higgs | +(+)Economy<br>(+)Welfare | --- |
| UNHCR Branch Office | _Arcology Living_ | --- | --- | --- | +(++)Infrastructure<br>+(+)Welfare<br>+(++)Resettlement | Increases this Arcology’s maximum population size. |
| UNPO Station | _Arcology Living_ | --- | --- | +(++)Ops | --- | (+)Defence rating.<br>Improves the rate of Unrest decreases in this nation. |
| UNOMI Listening Post | _Self-Adapting Algorithms_ | --- | --- | +(++)Influence | +(++)Social Science<br>+(+)STRATNET | Improves this nation’s Secrecy value. |






