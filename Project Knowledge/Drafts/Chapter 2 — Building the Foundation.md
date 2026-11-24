**Author’s Note:**

Welcome to Chapter 2! As mentioned in Chapter 1, this chapter replaces the older draft to fit our updated narrative direction and prose style.

This chapter is about the less glamorous side of building something from nothing. I wanted to show that having knowledge, ideas, and ambition doesn't automatically translate into success. There are practical problems to solve, mistakes to make, and countless small decisions that determine whether an idea can become reality.

I hope readers appreciate the importance of patience, preparation, and persistence. Great achievements rarely emerge fully formed. More often, they're built through countless small steps that don't seem particularly impressive on their own.

Looking for Advanced Chapters? If you don't want to wait for the public posting schedule, advanced chapters are live right now on my ***Patreon**.

---
Disclaimer

Road to the Stars is an unofficial work of fanfiction inspired by the Mass Effect franchise and other fictional properties. This story is not affiliated with, endorsed by, or sponsored by Electronic Arts, BioWare, or any other relevant rights holder.

---
**Chapter 2 — Building the Foundation**

The task manager was lying to me, and it took until three in the morning to figure out how.

It wasn't lying on purpose. It was reporting every job as complete the instant it was queued, so the status screen showed a column of cheerful green marks over work that hadn't started. I'd spent twenty minutes impressed with how fast the second workstation was before I noticed it hadn't produced a single result.

I leaned back on my mother's stool and rubbed my eyes. The loft smelled like solder and cold coffee. "Fast" was what you got when nothing was being done.

The bug was in the handoff. The core marked a job finished when the worker acknowledged receiving it, not when the worker returned a result. It was a one-line mistake from a one-evening skeleton. I split the state in two, _received_ and _completed_, queued two hundred trivial calculations, and watched the marks turn green one at a time. Eleven seconds. Trivial arithmetic wasn't the point.

The point was the work I'd been putting off. Before the system could help with anything real, it needed to know what the Med-Pod project actually contained, in a form it could search and cross-check. So I spent the rest of the night feeding it my notes. One entry per component, with its requirements, its dependencies, its source (_measured_, _calculated_, _datasheet_, or _my estimate_), and a confidence tag. Every number had to carry its origin. It was tedious, and I'd decided it was worth it the first time the sorter caught me contradicting myself.

By the time the sky went gray behind the loft window I had about three hundred entries in, and the scanner subsystem was in decent shape. The treatment modules were mostly question marks with arrows between them, which was honest.

Then I wrote the module I'd been saving. A calculation engine took a plain description of a problem, picked a model from a small library I'd written, ran it, and returned the answer with its assumptions listed beside it. Beam deflection, heat flow through simple geometries, basic fluid resistance, electrical loads. It wasn't clever. It was a very fast, very obedient version of the reference tables my mother kept on the shelf above the oscilloscope.

I ran the first real query at ten past six, as the shop's compressor kicked on downstairs on its timer.

_Temperature rise, aluminum actuator housing, 12 W dissipation, natural convection, 22 C ambient._

It answered in under a second. I pulled out the old tables anyway and worked it by hand, because the first answer from any new instrument gets checked against a known one. We disagreed by about four percent. The engine's library used a slightly different convection coefficient than the table, and neither was wrong. Natural convection coefficients are a range, not a point. I changed the entry so the system would report the range, saved everything, and went down to open the shop.

Two vans were already idling at the curb.

They were white, with PACIFIC LINEN SERVICE on the doors and a woman in the lead cab who climbed down holding a tablet like a summons. "Ms. Bautista," she said. "Mr. Okafor said you'd fit us in. Both of them throw a drive fault when they're loaded, and I have hotel contracts that start Friday."

I looked at the vans. I looked at the three bays, one of which still had a half-finished brake job in it.

"Friday," I said.

"Friday."

"Pay on delivery?"

She almost smiled. "That's the arrangement Mr. Okafor said you'd ask for."

---

The vans ate the better part of three days. One had a corroded charge-port contact and the other a failing cooling pump, so they were two ordinary jobs, but ordinary jobs don't care what you built the night before. The project got my nights. I fell into a rhythm of repair until six, a sandwich, and the loft until I couldn't read the screen.

Most of what the system did that week was catch me out.

The first was a unit error. I asked for deflection of the scanner's gantry frame under its rated load, and the answer came back lower than my hand calculation by a factor of about eight. The assumptions list showed the frame's tube wall as three centimeters thick. I'd typed _3_ meaning millimeters, in sloppy shorthand, and the importer had guessed. A tube with a three-centimeter wall wasn't a frame. It was a girder. I fixed the entry, then fixed the cause. The importer now rejected anything ambiguous and flagged it for me, and no result could be marked _usable_ if its inputs included a guessed unit. Then I went back through all three hundred entries. The importer had quietly guessed in eleven places, and two of them mattered.

The second was a gift. I fed the scanner subsystem in and asked it to map dependencies, what had to be decided before what, and the graph showed me a loop I'd missed. The sensor array's thermal budget depended on the gantry actuator's dissipation, which depended on scan speed, which depended on the image resolution I wanted, which depended on the sensor's sampling rate. Four decisions chasing each other. I broke it by fixing the scan speed first and letting the rest follow, and wrote down why.

The third took a full night, and I was least sure of it, because it involved the transducer.

Ultrasound doesn't measure density. It tells you how a pulse travels through a material and how much of it bounces back at a boundary, and the property that governs the bounce is acoustic impedance, density multiplied by the speed of sound. So that was what I asked for. I gave the system pulse-echo traces from the used transducer module I'd bought, aimed at a gel phantom I'd cast on the bench the weekend before from gelatin and graphite powder, a crude stand-in for soft tissue. It compared the echo off the water-to-gel boundary against the echo off a steel plate of known properties, worked out the reflection coefficient, and backed out the gel's impedance. I'd recorded two hundred pulses from one placement of the transducer.

The interval it returned was so tight it made me suspicious.

So I took the ultrasound out of it. I weighed the block and measured its volume by water displacement, which gave me density from a kitchen scale and a measuring jug. Then I timed a pulse through the block on the oscilloscope, measured the thickness with calipers, and got the sound speed. Density times speed gave me a reference impedance that didn't depend on the system at all. It landed inside the system's interval, but nowhere near the center. The estimate wasn't bad. The confidence was.

The trouble was that all two hundred pulses had come from one placement, through the same film of coupling gel, at the same angle, seconds apart. Noise averaged away, which was what the tight interval reflected. Any error in the placement was baked into every pulse identically. Two hundred readings of the same bias aren't two hundred pieces of information. They're one, repeated. To be sure, I lifted the transducer, wiped it, re-coupled it, and took ten pulses, eight times over. Within each set the readings agreed beautifully. Between sets they wandered far more than the interval allowed.

I rewrote that part of the model so it separated the error shared within a placement from the noise between pulses, and counted placements, not pulses, as the number of independent measurements. The interval widened to something honest, with the reference value comfortably inside. It was less impressive and it was correct, and for anything that might one day sit near a patient, that was the trade I wanted.

I wrote a rule on the whiteboard next to the oscilloscope. _Nothing goes into a design until I've checked it._ Below it I added: _And check the inputs first._

The last job I queued that night was a thermal model of the sensor array, nothing exotic. An hour and ten minutes later it was still running, the fans were screaming, and the cursor had stopped responding. I killed it. I'd learned what I needed to know. The framework worked, and the hardware under it didn't.

I pulled the pad over. Property tax on the building and house was due on the thirtieth. Ms. Bautista's invoice wouldn't clear until Friday. The savings account was a number I could look at without flinching and couldn't spend carelessly, because everything after this phase would need it too. I wrote a ceiling for compute and workshop upgrades, four thousand dollars, and underlined it twice. Then I turned to the green ledger my mother had kept for twenty-two years, found my own page under her last entry, and wrote the ceiling there too. She'd have wanted it in ink.

It was midnight. I picked up the phone anyway, because I knew who would still be awake.

---

"You want _what_?" said Dolores.

She was the parts supplier's delivery driver, a broad woman in a reflective vest who'd been dropping boxes at the shop since before I could drive and who treated every unusual request as a personal affront. She'd come by Friday morning with a pallet of brake pads and found me standing in the bay with a list.

"Used server blades," I said. "From the liquidator in the industrial park. Four, maybe six. Mismatched is fine. I need compute, not matching stickers."

"That's a bunch of dead computers."

"They're only mostly dead."

She read the list again, then looked at me over it. "Your mother would've said you were out of your mind."

"My mother would've asked what they cost and whether I could pay in parts."

That got a snort, and then, to my surprise, a conversation. The yard's foreman owed her for a favor involving a pallet jack and a lost weekend, she told me, and the liquidator priced by weight and mood, not by what anything did. If I walked in alone, a twenty-year-old asking about servers, I'd pay the mood. "Saturday," she said. "I'm borrowing the van. Technically I'm not supposed to. Don't say anything to anyone."

I'd spent Thursday night on the yard's online inventory sheet. The system had ranked the blades by usable compute per watt and flagged the ones whose power draw wouldn't share a circuit. Its output was short and unfriendly: _Units 2, 4, 7, 9 recommended. Units 2 and 9 together exceed single-circuit load. Memory modules: age and condition unknown; test before use. Price data not provided._ I'd printed it and folded it into my pocket. Dolores read it in the van at a red light, grunted, and said, "At least it knows what it doesn't know. My nephew doesn't."

The yard was an acre of shelving behind a chain-link fence, with a forklift that beeped whenever it moved and a foreman who greeted Dolores like a creditor. The blades were in a data center's worth of cages, stacked like pizza boxes. The sticker on the lot I wanted said three thousand one hundred. Dolores walked the aisle with her hands behind her back, picked up a blade, set it down, and said, "Dead center of a flooded building, these were. See the rust on the rails?"

"Flooded?" said the foreman. "That was a roof leak."

"Roof leak, flooded. It's a long way to the same place." She tapped my printout. "He wants five blades, the chassis with the broken power supply, and the pallet of memory nobody's touched in a year. All of it. Cash."

They went three rounds. I stood there, as instructed, looking like a man who might walk away. When it was over, the number was twenty-four hundred and fifty. Dolores took the receipt, folded it once, and handed it to me. I counted the bills out from the savings withdrawal, and that was the first money I'd taken out of savings for the project.

It was while they were loading the pallet that I noticed the other one. It sat near the back, shrink-wrapped, a stack of small articulated arms pulled from an assembler that had gone bankrupt, controllers still attached. Most had burned-out joints. One, a compact six-axis unit with a reach of about half a meter, had a note taped to it that said _works_, in handwriting I trusted more than the inventory sheet.

I asked the price. It was less than a decent set of wrenches. I also did the arithmetic on what was left under my ceiling, with the tax due and the vans unpaid, and I said, "Not today."

"Scrapper takes those Friday," the foreman said.

"Tuesday," I said.

He looked at Dolores. Dolores looked at the ceiling. "I'll tell him it's spoken for," she said, to nobody. "He owes me."

On the drive back, she kept both hands on the wheel and said, "Your mother used to make me carry the receipts, too. She said the day I stopped checking them was the day I'd be buying a pallet of air."

---

I tested the modules on a bench rig Saturday night and kept most of them. The memory was a lottery. A third of it threw errors, which I discarded, and the rest passed. Three blades booted clean, a fourth after I reseated its processor, and the fifth went into the parts bin for scavenging.

By Sunday afternoon I had four working blades in a salvaged chassis on a sturdy shelf at the back of the loft. The dead power supply I replaced with one from the shop's parts room, rated for more than the load. I added a fan, because the ventilation up there had been designed for storing tires, and gave the cluster its own power circuit, which took an hour with a conduit bender and a long conversation with the breaker panel.

Late that night, I connected it all to the framework and queued the thermal model that had choked the first workstation. It finished in six minutes.

I stood there with my arms folded, listening to the blades settle. Forty times the processing capacity, and not one of the vans had been mine to build it with. Then I turned off the loft light and went to bed, because the vans were due back Friday and it was only Sunday, and my body had other opinions about sleep.

---

On Monday morning I walked the building before the first customer came in, with a clipboard and a cup of the good coffee, the way my mother used to walk it every Monday of my life. _First you look at what's in your way,_ she'd said. _Then you decide what to do about it._

What was in my way was that I was doing two jobs in one room. The loft had become the project, but it still shared a building and most of my attention with a repair business that paid for everything. Customers were walking past half-assembled sensor gear to get to the restroom. A tablet with three weeks of design notes sat two feet from a transmission jack, and Ms. Bautista's driver had already leaned on the stair rail asking what I was building up there. I'd said "a hobby," and he'd said, "Looks expensive."

So I separated them. The three bays stayed repair. The loft became a proper development area behind a lockable door at the top of the stairs. I added a cabinet for anything I couldn't afford to lose and a fresh coat of paint on the worktable so I could see what I'd spilled. In the corner farthest from the stairs, I partitioned a clean bench with plastic sheeting on a pipe frame and a cheap air filter, the closest thing to a clean area I could build. It wasn't sterile and wasn't meant to be. But sensors and optics that would one day sit near a patient shouldn't be assembled next to a lathe.

Ms. Bautista paid on Monday. Both vans ran clean. I watched them pull out and felt the account go back to a number I could work with.

Then I went looking for the things I did over and over, and calibration was the worst. Every sensor had to be moved through a set of known positions while I recorded readings, which meant hours at the bench repositioning a probe by hand and writing numbers into a log. The data was only as good as my patience at hour four, and my patience at hour four was bad.

I bought the arm on Tuesday. Dolores met me at the yard gate with her arms folded and said the scrapper had been "very disappointed." It took two evenings to get it running. The controller's software was proprietary and a decade out of date, but its protocol was documented well enough that I could write a simple interface for it. The system helped there, in its way. It ran the manual's timing tables against my first attempts and told me the second joint's acceleration limit was eight times what the hardware could take, which saved me a gear train. I mounted the arm on a steel plate at the end of the calibration bench and clamped a transducer to its tool flange.

The first run overshot twice and nearly clipped the bench lamp. I spent an hour on its motion limits. On the second run, it moved through ninety-six positions, paused at each, and logged the readings into the knowledge base while I stood and watched.

It took forty minutes. By hand it would have been an afternoon.

I left it running and went down to the shop to do an actual repair. When I came back, there was a complete calibration data set sitting in the system and nothing to enter by hand. The coffee was still warm.

I didn't stop there. The parts room was a mess of handwritten tags, and every Friday I burned most of an evening reconciling invoices against inventory. So I pointed a small piece of the same software at it. A script read my supplier invoices, matched them to stock, flagged what was running low, and drafted the order. I still approved every purchase. Friday evenings got shorter, and I spent the difference checking calibration results.

---

On Thursday I sat down at the clean bench with the Med-Pod project open from the top.

The scanner was the first thing I wanted to get right. The architecture was a gantry carrying a sensor array across the patient, each pass building a picture from several kinds of measurement: ultrasonic imaging for structure, electrical impedance for tissue type, optical sensors for blood oxygenation and surface condition. No single sensor saw enough. The combination did, if the software could fuse their readings into one picture and say honestly how sure it was.

I asked the system to enumerate everything the scanner depended on. In under a minute it handed me a table of forty-one components, each tagged with source and status, and flagged six where my entries conflicted. For each one, I made the call. I couldn't have delegated that part.

Then I asked the harder question. _What can I build here, and what do I have to buy?_

The first pile was what I could fabricate myself: the gantry frame, machined from aluminum extrusion on the mill, the sensor housings and cable guides from the printers, and the mounts and brackets, ordinary shop work. The second was what I'd have to buy and couldn't improve: transducer arrays, optical sensor modules, precision linear actuators, all built to tolerances my mill couldn't touch. I priced them, ordered the cheapest options that met the thermal and accuracy requirements, and had the system run each against the design checks. Two failed. I swapped them, and the swap cost me more than I'd planned.

The third pile was things I couldn't build or buy yet: a medical-grade fluid system, sterile materials, a treatment module of any kind. They were real parts of the Med-Pod, and I wasn't going to pretend otherwise. They'd have to wait for money, a better lab, and a lot more help than a man alone in a loft. I wrote them on the last page under _Later_ and didn't feel bad about it.

I ran the first simulation of the gantry frame with the corrected geometry. The cluster returned its result in under four minutes, with margin to spare, and my hand calculation agreed to within a few percent. The thermal model of the sensor array was less kind. The optical modules ran hotter than I'd assumed, and the housing I'd sketched would have cooked them. I redesigned it with a heat path into the frame, simulated the new version, and sent the file to the printer.

It started to hum. For the first time since I'd begun, there was something on the bed besides a test.

---

By Sunday evening, the printer had finished the new housings and the first brackets, and I had a mill setup ready to cut the gantry frame on Monday.

I sat down with my mother's green ledger. The receipts for the whole phase were in a folder, every purchase earned its place, and the total ran a little over the ceiling I'd set and a little under what I'd feared. The property tax was paid, with the shop's cushion untouched. I wrote the figure under hers in the ledger and added a line about the transducer order, which hadn't been counted yet. The page looked like it belonged beside hers.

In the project log I wrote an honest assessment, the only kind that helped. _System: functional. Good at calculations, documentation, dependency mapping, bulk data. Weak at anything the data doesn't contain. Must verify inputs and outputs. Compute adequate for now; will need more for tissue modeling. Workshop: usable, repair and development separated, no sterile capability. Scanner: designed to the point of fabrication. Treatment, fluid handling, sterile systems: not started._ Below that I wrote the line I cared about most. _Nothing here goes near a living person. Bench, phantoms, and simulation until the data says otherwise. Then proper trials, with proper people. No shortcuts._

Then I closed the log, erased the old list on the whiteboard, and wrote a new one in the order the work would happen.

_1. Machine gantry frame._  
_2. Assemble and align sensor array._  
_3. Integrate scanner with the system._  
_4. Calibrate against phantoms._  
_5. Find out what breaks._

The last item made me smile. Something always broke. That was what the first four were for.

Downstairs, the shop was quiet and the invoices were reconciled. Mr. Okafor's truck had run without trouble since I'd fixed it, and his referral had paid for half of what I'd built. The transducers would arrive Wednesday, according to the tracking page, and Dolores had threatened to deliver them herself. I had two days to cut the frame and get it square.

I loaded a length of aluminum extrusion into the vise and indicated it in, sweeping the dial gauge slowly along the edge until the needle stopped moving. My mother had taught me that. _You can't cut straight until you've measured straight._

I set the zero, started the spindle, and made the first cut.