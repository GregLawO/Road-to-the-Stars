# Droid Production Rate: Proposed Model

*Proposal for author review, 9 November 2026. All numbers are my decisions, open to overrule. Canon anchors come from the project files.*

## What actually limits the rate

I checked each possible bottleneck for a Tier II droid of about 250 kg (my assumption).

| Limit | Calculation | Verdict |
| --- | --- | --- |
| **Materials** | The arrays take scrap by the ton. 250 kg per droid × 5,000 droids a month = 1,250 t a month, about 42 t a day. | Not a limit |
| **Energy** | Vaporizing and sorting steel costs about 8 MJ/kg in physics terms. At roughly 10× real-world inefficiency that is about 22 kWh/kg, so about 5.5 MWh per frame. With fabrication, call it 7 MWh per droid. One 50 MW tokamak gives 1,200 MWh a day, enough for about 170 droids a day. | Not a limit |
| **Core loading** | The rule says more loading devices load more cores, so loading never caps output. | Not a limit |
| **Assembly** | One cell is one Tier II operator plus three Tier I fixtures. It builds one finished droid in about 10 days, so about 3 a month. | The real limit |
| **Human validation** | Humans sign each production lot, so signatures cap the number of lots, not droids. | Soft limit |

Capacity is easy once the self-building line exists. The rate is therefore a policy choice by Kenji (secrecy, who he trusts, how much he stockpiles), not a technical one.

## Proposed schedule

| Date | Droids built (cumulative) | Rate | Basis |
| --- | --- | --- | --- |
| Oct 2052 | 4 | about 1.3/month | Canon (A2.4). Hand-built in Oyama's toolroom from July. |
| Dec 2052 | about 10 | about 3/month | The Tier I fixture line is still being built first. |
| Mar 2053 | about 34 | about 8/month | The fixtures now make Tier II frames. |
| Jun 2053 | about 94 | about 20/month | Enough to cover the hidden wings. |

### The June 2053 check

I assume 25 droids per site for the pod rooms, wing corridors, dock and perimeter. Three clinics need 75, and the warehouse and Oyama's plants need about 20 more. That is about 95, so the schedule matches the canon need for guards on every pod by summer 2053.

### After summer 2053

Tier III units take over the guard posts, and Tier II units convert to operators by crystal swap. That gives about 60 cells by late 2053, which is about 180 droids a month of capacity.

### The 2057 anchor

Oyama's first Level 1 arms reach the quay in September 2057. These are fixture-class, so they come off the Tier I line. About 300 cells by then is plenty.

### The 2066 anchor

Level 2 and 3 labor robots go public in 2066. I suggest 5,000 a month at launch, rising to about 20,000 a month (240,000 a year) by 2069.

- For scale, roughly half a million industrial robots a year were installed worldwide in the early 2020s. As far as I know, that figure is right.
- 240,000 general-purpose labor robots a year is enough to wreck specific trades in specific districts, which is what the A3 strike needs, without wrecking the whole economy.
- It needs about 1,700 cells, a 24% annual growth from 300 in 2057. Capacity at that size is about 5,000 droids a month, so no part of the plan is a stretch.
- It also explains A3.9's price below the robots' metal cost: the metal is free, because it comes from scrap through the arrays.

### The two Level 5 droids

Keep them at two. Kenji builds them himself over about nine months, October 2052 to summer 2053.

## The decision for you

Any cell count above 300 by 2057 means Kenji could be producing far more than he sells. Options:

- **No stockpile:** build only to order.
- **A guard-only reserve:** a few hundred Tier II/III units held back.
- **A larger standing reserve:** a real cost in secrecy risk.

I'd pick the first or second. A big stockpile is a story fact that later chapters would have to honor.

## Two conflicts the numbers ran into

- **Battery mass.** The battery sheet gives 6.4 MWh at 850 Wh/kg, which is about 7.5 tonnes per pack. That cannot fit in a 235 kg suit or a human-sized droid. If you meant 6.4 kWh, the mass works for suits but not for the 135 kW × 48 h endurance figure. I did not use pack mass in the model.
- **Tier mapping.** The story's Robotics Levels 1 to 5 and the droid sheet's Tiers I to V are still not mapped to each other. I used "guard" and "operator" for the droids described in the story.
