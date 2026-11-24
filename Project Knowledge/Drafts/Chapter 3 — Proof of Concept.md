**Author’s Note:**

First, my sincere apologies for the delay! I know I missed my promised update date by over a week. Overhauling Chapters 1 and 2 into the new prose style while finishing Chapters 3 and 4 took more time than anticipated, but I wanted to make sure the technical accuracy, pacing, and continuity hit the mark for this new direction.

**Note for Returning Subscribers:** If you were following the previous version of _Road to the Stars_, **please make sure to go back and re-read Chapter 1 (and Chapter 2)!** The opening chapters have been completely rewritten from the ground up to establish our new prose style, tighter character dynamics, and updated continuity. Reading Chapter 1 again is essential for getting the full context of this new version.

I wanted this chapter to explore the difference between theoretical knowledge and practical results. Kenji may have an unusual advantage, but that doesn't mean everything will work perfectly the first time. Ideas still need testing, problems still need solving, and assumptions still need to be challenged.

I hope readers enjoy seeing the process behind technological development rather than treating every invention as something that simply appears because the protagonist knows how it works. The journey from concept to working technology is part of the achievement.

Looking for Advanced Chapters? If you don't want to wait for the public posting schedule, advanced chapters are live right now on my ***Patreon**.

---
Disclaimer

Road to the Stars is an unofficial work of fanfiction inspired by the Mass Effect franchise and other fictional properties. This story is not affiliated with, endorsed by, or sponsored by Electronic Arts, BioWare, or any other relevant rights holder.

---
**Chapter 3 — Proof of Concept**

The fourth face of the gantry frame came off the mill at ten past eleven on Monday night, and I could feel the error with my thumbnail.

It wasn't much. A step the width of a few sheets of paper where the two halves of the cut met in the middle. The mill's table traveled about a third of a meter less than the frame was long, so I'd cut each side in two setups and tied them together with a datum bore. In theory the bore made the two setups agree. In practice, a twenty-year-old mill with worn table screws agreed with itself to about a tenth of a millimeter on a good day.

A tenth was too much. The actuators would bolt to those faces: one each for the X and Z axes, and a pair for Y, one on either side of the bridge, driving it in lockstep. Two actuators mounted on faces that weren't level with each other would fight over every move until one of them stalled or the motors cooked.

I carried the frame to my mother's cast-iron surface plate, pulled off the dish cloth, and rubbed a thin film of blue dye across the mounting face. When I rocked the frame against the plate, the dye transferred in two islands with a bare stretch between them.

"Okay," I said. "That's honest, at least."

I couldn't re-cut it. The stock was gone, and another extrusion that size cost more than the transducers I'd ordered. So I measured the error instead. I walked a dial indicator across each mounting face in a grid, fed the readings to the system, and asked for the shim schedule that would bring all four actuator seats into one plane.

It came back in ninety seconds: a table of positions and thicknesses, with a note beside three of the cells.

_Shim stack exceeds 0.15 mm at positions C3, C4, D1. Stacked shims compress under load. Recommend re-machining or bonding._

That was the system telling me where its math stopped being trustworthy. I took the advice on C3 and C4 and ignored it on D1, where one precision-ground shim from the parts-room drawer would do the work of three thin ones. Then I spent forty minutes with a scraper and a fine stone, dressing the high spots until the dye spread evenly, and shimmed what was left.

At midnight, the faces sat inside two hundredths of a millimeter of each other. My mother's plate had once again been right about everything.

I wrote the number in the log and underlined it. The transducers were due Wednesday, and I'd just spent most of the cushion in my head on a box of crystals that I couldn't afford to replace. Everything I mounted near them had better be flat.

---

Dolores delivered the transducers on Wednesday, holding the box out at arm's length like a dead bird.

"Eight hundred and sixty-one dollars of tiny crystals," she said. "Sign here. And don't tell me what they do."

"They listen to the inside of things."

"I said don't tell me."

I signed. She stayed long enough to look at the frame on the workbench, an aluminum rectangle with four actuators bolted to it and a nest of cable ties around it. "That's it? That's the miracle?"

"That's the skeleton."

"Looks like a bad bed frame." She lingered a second at the door, looking at the box in my hands, and I realized she'd noticed how carefully I was holding it. "You drop that, you're not getting another one on credit," she said. "Your mother would've put it in a drawer and locked the drawer."

"I'm going to put it in a drawer and lock the drawer."

"Good." She left, pleased with herself.

I unboxed the array on the clean bench. Sixty-four elements on a curved face the size of a playing card, ribbon-cabled to a driver board, and it weighed less than a sandwich. The bench rig confirmed that every element fired. Then I put the whole thing in the cabinet and locked it, because I'd decided there would be no powering it until everything around it had earned the right.

Over the next four days I built everything else, between customers.

The printers ran nearly nonstop. The sensor carriage came first, a shell around the array with a duct that carried heat out to the frame, built from the redesign the thermal run had demanded. The optical module housings, the cable guides, and a stiffener plate followed, the last one overbuilt, because I'd been wrong about the frame's stiffness once already. The first prints came off warped. I flipped the part orientation in the slicer and ran them again, and then there was a wait I filled with a transmission.

The treatment head took the longest. The Med-Pod had to do more than see damage. It had to fix some of it, and the full version of that was years away. It would need medical-grade materials, sterile fluid paths, and expertise I didn't have. What I could build was a bench-scale head that demonstrated the principle: locate a wound from the scan, plan a path along it, and lay a closure agent where it belonged. So I built the dullest version I could. A printed head carried a blunt dispensing needle, with a small roller foot trailing behind it to press the wound edges together and a vertical axis to hold the needle at constant height over uneven skin. The feed was a syringe pump I put together from a stepper motor, a lead screw, and a ten-milliliter lab syringe. The agent was a stand-in, a bright blue gel I mixed from dyed silicone and thinner until it flowed. The real thing, a tissue adhesive or closure compound, was a regulated medical product, and I had no business near it.

I labeled the head _BENCH SURROGATE ONLY_ with a strip of tape, because I knew myself. In six months I'd forget what it was approved for.

The unit itself I sized to what I could prove. A full-body scanner was out of reach. The frame closed around a bench-scale bay, big enough for a limb section about the length of a forearm. Anything that worked at that scale would be a design I could grow from.

By Sunday the frame stood on its steel base in the middle of the clean area with the carriage mounted but not wired, and I'd used nearly every spool of filament in the loft. I looked at it. An aluminum frame the size of a bread box, a carriage, a mess of unconnected cable.

"Not bad," I told it. "Let's see if you move."

---

It moved, and it lied about where it ended up.

The test was whether the gantry could return to a position and land in the same place. I clamped the calibration arm to the base plate with a dial probe on its tool flange. The system drove the carriage to a point, the arm touched off against it, and the number went into the log. Then the carriage moved away, came back, and the arm touched off again. A hundred and twenty cycles over three axes.

X and Z came out clean, repeatable to a few hundredths of a millimeter, better than I'd hoped. Y was ugly. Moving left to right, it landed on the mark. Moving right to left, it fell about 0.18 millimeters short, every time, with a consistency that told me it wasn't noise. The datasheet promised backlash of 0.05 millimeters at most.

I wasn't worried until I put a felt-tip pen in the treatment head's mount and told the carriage to draw a one-centimeter square on a sheet of paper. The pen drew three sides, and on the fourth it came back to the start and missed. The square didn't close. There was a doubled line along one edge, thin as a hair, where the carriage had arrived from the wrong direction.

A hair's width wasn't much. But the wounds this head was meant to follow had lips a millimeter apart, and a path that wandered a fifth of a millimeter depending on which way it was traveling would lay the bead on one lip instead of across the seam.

"One of you is a bad part," I said, "or I put you in wrong."

I checked the mounting first, because the likelier mistake was mine. I loosened the near-side actuator, re-seated it on its shim, and ran the test again. Same result. Then I took both Y actuators apart. Each lead screw's anti-backlash nut was a plain plastic piece with a spring so weak I could compress it with a fingernail. They were within tolerance on paper, but the spec had been written for a lighter carriage than mine. I'd bought the cheapest parts that fit the requirements, and the requirements hadn't known about the stiffener plate.

I machined replacement nut housings from brass scrap, fitted them with stiffer springs from the parts-room assortment, and tuned the preload by feel and then by number until the arm's readings matched in both directions. The motors ran warmer, and the system flagged it, and I wrote that down too. Backlash came out under 0.03 millimeters. I drew the square again. This time it closed.

The array was next, and it was misbehaving in a way that took me longer to see.

I took it out of the drawer, mounted it over a fresh gel phantom with a steel pin drilled in at a known depth, and fired a single element. One clean echo off the pin. Then I fired the whole array in sequence and got the echo off the pin and a faint second one, a few microseconds behind it.

The system put the second echo in its report as a separate reflector, thirty-one millimeters deep, size unknown.

There was nothing at thirty-one millimeters. There was gel all the way down to the bottom of the block. But that was how a clinician would read the picture: a second object, deeper, possibly a foreign body, possibly a bleed. A machine that invented features couldn't be left near anyone who'd believe it.

The system cross-correlated the channels and found that the ghost's timing didn't match any physical path through the phantom. It matched the electrical delay along the ribbon cable. A fraction of each firing was leaking into its neighbors before it ever left the array. The cable had one ground wire shared by every channel, running half a meter, and every channel's return current was riding it.

I rebuilt the cable with a ground wire between each signal pair, shortened it by fifteen centimeters, and wrapped the run in copper shielding tape. The ghost dropped by an order of magnitude, to just under the noise floor. I ran the phantom again and the thirty-one-millimeter reflector was gone. I put the array back in its drawer and locked it, because I'd just remembered the price.

The optical modules needed less work. They had already taught me about heat, and the new housing held them steady. I tested each against reflectance cards of known gray levels, which told me what I needed at this stage: that every module responded to light consistently, that the modules agreed with one another, and that their readings sat inside the datasheet's range. That was all the cards could tell me. A gray card has no hemoglobin in it. Measuring blood oxygenation would take proper reference materials with known and stable optical properties, and later a reference instrument under controlled conditions. Until then, the oxygenation channel was uncalibrated, and I marked it that way in the log and in the software, so I couldn't talk myself into trusting it. After fifteen minutes the housing temperature leveled off, but the baseline had crept upward the whole time. I noted it, put a flag on it, and moved on. It would matter later.

The pump was the last on the list and the least trustworthy. A commanded milliliter of dyed water onto a scale came out at 0.93, then 0.94. The error was steady, which made it fixable: backlash in the screw and compliance in the plunger. I added a prime-and-retract move to take up the slack and a correction factor in the control software, and ran the whole range from one to eight milliliters. Within three percent, then within one after a second correction.

Five subsystems, and five things I'd fixed or flagged to get them there. I wrote the numbers in the log, one line each, with dates, and then I closed it, because the next thing on the list couldn't be tested in pieces.

---

The assembly took two days, and I did it slowly, because every connection was a place for the thing to go wrong.

I wired the array into the carriage, mounted the optical modules beside it, and ran the cable bundle through a drag chain I'd printed to keep it off the frame. The treatment head went on last, with the pump on a bracket behind it. The control electronics sat in a steel enclosure at the back of the base: motor drivers, a microcontroller for real-time motion, and a power supply with a hardware current limit that I set low enough to protect the array.

The safety circuit I wired separately, on purpose. A hardwired chain with no software in it: the door switch, an overtravel switch at the far end of each axis, and the emergency stop, all in series through a safety relay that fed power to the motor drivers. If any contact opened, the relay dropped and the drivers lost power. The microcontroller could watch the chain but couldn't override it. A controller can be wrong. I wanted something under it that couldn't be talked out of anything. The emergency stop went on a mushroom button at the end of a long cable, so I could keep it in my hand.

Before I let the machine see mains power, I tested the chain with a meter. I opened every contact one at a time and confirmed that the relay dropped each time. Then I opened two at once, which proved nothing, and I did it anyway. By the time I was done, it was after eleven on a Wednesday night and the loft was quiet except for the cluster.

I ran the startup checklist aloud, because I'd written it down and wanted to hear it. "Enclosure closed. Safety chain closed. Supply current limit set to twelve amps. Phantom loaded. Emergency stop in hand."

The system showed the green lights it was supposed to. I had one thumb on the mushroom button and the other on the keyboard.

"Initializing."

The drivers hummed. The carriage lurched along the Y axis, away from the home position it was supposed to be seeking, and kept going. I hit the stop.

The safety circuit had already beaten me to it. The relay had dropped, the drivers had lost power, and the carriage coasted to a halt a few millimeters short of the end of travel. A red line appeared on the screen: _Safety chain open. Y overtravel. Drivers disabled._

I looked at the line for a second, with my heart going, and then I started laughing.

The mistake was small and stupid, and it was mine. The homing switches on X and Z were normally-open units, and the one on Y was normally-closed, a different part from a different bin. The controller's configuration assumed all three were wired the same way. It had read the Y switch as already pressed at power-on, concluded the axis was sitting at home, and executed the back-off move, in the wrong direction. It never saw the switch it was looking for because it believed it was already there. The controller had been wrong with complete confidence. What stopped the carriage was the overtravel switch at the far end of the rail, which sat on the hardwired chain and didn't care what the controller believed.

"That," I told the machine, "is why the safety circuit doesn't talk to the controller."

I fixed the configuration in two minutes and the wiring label in two more, because the mistake would happen again if the label still lied. Then I reset the chain, rearmed the supply, and tried again. This time the carriage homed on all three axes in sequence, touched each limit, and backed off. The self-check stepped every actuator through its range, listened to the array, the optics, and the pump, and reported _Initialization complete_, no faults.

I let out a breath I'd been holding for most of a minute. I wanted very much to scan something. I wasn't going to, because it was midnight and I'd already had one surprise. I ran a single blank-phantom scan to see if anything fell over, and nothing did, and I went to bed.

---

In the morning, I loaded a limb phantom into the bay, a block of gel with a silicone skin and nothing in it but a steel pin. I'd cast it the previous weekend and set the pin myself. I knew exactly where it was. That was the point. If the machine couldn't find a thing I'd put there, nothing else it said would matter.

I started the scan. Eleven minutes later, I had a smear.

I stood in front of the screen and let the picture teach me. The pin was in there, but it was long and streaked, as if someone had dragged a thumb through it. Under it, the tissue-type map showed bands of noise that didn't match anything physical. The optical map was readable. The impedance channel was garbage.

It was ten in the morning and I had a customer at eleven. I looked at the picture for a long time anyway, because I'd told myself that whatever happened in this room I would not skip the part where I looked.

The impedance channel mattered more than any other. It was how the machine told gel from skin, or tissue from fluid, and the whole reason the scanner combined three kinds of sensor was that no single one could be trusted alone. If the impedance map was noise, the machine would call fluid solid, or solid fluid, and the fusion I'd built the whole design around was a fiction.

I did the repair job at eleven and a second at one, and I came back up at six with a clear head and asked for a frequency analysis of the raw impedance channel during a scan.

The spectrum came up with a sharp spike in the middle of the trace, and the system tagged it before I did. It sat at a frequency that matched the step rate of the Y motors at my chosen scan speed, with harmonics marching up the plot like fence posts.

The motor drivers were putting a signal onto my sensor. Every step pulse was a small electrical kick, and the sensor was faithfully reporting it.

The system could tell me where the noise was. It couldn't tell me what to do about it. I had three options. I could filter the noise out in software, which would throw away real signal along with it. I could shield and separate the circuits, which would reduce the noise but not eliminate it while the motors ran. Or I could stop moving while I measured.

The third was obviously right. I'd been scanning on the move because I wanted speed, but speed wasn't what a prototype needed. It needed data I could trust. I rewrote the scan routine to move, stop, settle, and measure, then move again, and the drivers idled during acquisition so the sensor listened to a quiet machine. I separated the sensor ground from the motor ground at a single star point, wrapped ferrite beads around the motor cables, and moved the driver board to the far end of the enclosure.

A pass over the phantom had taken two minutes in the smeared version. The new one took eleven.

I accepted that. Eleven minutes was a prototype speed. I reran the scan and the impedance bands dropped to a faint hum. The pin came out sharp. The tissue-type map showed gel as gel and silicone skin as skin, with a clean boundary between them.

The second problem showed up as soon as I laid the ultrasound image over the optical one. The pin appeared in both, and the two pictures disagreed about where it was by two or three millimeters.

I'd expected that. The array and the optical modules sat side by side on the carriage, a few centimeters apart, and I'd measured the offset by eye. A medical device that aligned its pictures by eyeball was a toy. Two or three millimeters was bigger than the depth of the lacerations the machine was meant to find.

I built a registration target: an aluminum plate with a grid of nine blind holes and pins at known positions, set in a block of clear gel. Both sensors could see the pins, one through echoes and one through reflected light. I scanned it, handed the system both pictures, and asked for the transform that made them agree. It came back with an offset of 2.3 millimeters on one axis, 0.4 on the other, and a rotation of just under a degree. I'd misjudged the first, shrugged at the second, and ignored the third entirely. I put the numbers into the scan routine, rescanned the target, and the pins fell on top of each other to within a fraction of a millimeter.

The third problem I'd half expected, and it was my fault. When I put a wounded phantom in the bay and asked the treatment planner for a path, the path was beautiful and wrong. It hovered a few millimeters above the skin and traced a line that matched the laceration in the picture but not in the bay. The planner was working in the scanner's coordinates, and the treatment head had its own. They were two machines that had never met.

That was routine to fix. I dipped the needle in dye and touched it to a fiducial plate at four known points while the scanner viewed the same points, and the system worked out the transform between them. It took an hour and a lot of dye. When I replanned, the path landed on the cut.

Nothing was broken. But I'd made every one of those decisions one at a time: stand still while measuring, align the sensors to each other, align the head to both. Each had been waiting in the gap between parts that worked alone and a system that worked together.

---

The next full scan came back with its own report, and for the first time I read it before I looked at the image.

It listed what it had found, and in a separate section, what it wasn't sure about. The second section had one line. _Optical baseline drift, 6.2% over the scan duration. Cause: module warm-up. Reflectance values from latter rows unreliable._

I'd forgotten about the drift. I should have remembered. I pulled up the temperature curve I'd logged weeks earlier and laid it beside the drift, and they tracked each other almost exactly. The fix needed no new hardware. Before each scan, the modules would warm up for fifteen minutes. During each scan, the carriage would pass over a reference patch, a gray card mounted in the bay, once per row, and the system would use those readings to correct the baseline continuously.

It cost me two more minutes per scan and another evening to get right. The drift dropped to under half a percent. The scan took thirteen minutes now, and I stopped caring.

It was Friday, almost midnight, when I ran the treatment dry run. I removed the blank phantom and loaded a new one with a fine cut already in the skin layer, a single straight laceration about three centimeters long, made with a scalpel, with the lips parted slightly. The scanner found it. The planner drew a path along it. The carriage moved the head to the start point, lowered the needle to a millimeter above the skin, and began laying a bead of blue gel while the roller foot closed the lips behind it.

I watched the bead go down. It wobbled at one point where the skin dipped, then recovered, and the line ended exactly where the cut ended.

I took the phantom out and ran a thumb along it. The edges had closed. The seam held.

It had worked, on a phantom I'd made, with a cut I'd put there, in a bay I'd loaded myself. I wrote the result in the log and then I wrote, underneath it, _This proves nothing yet._ Every test I'd run had been a test I'd designed, and I knew every flaw in every phantom. A machine tested against its builder's expectations proves only that the builder expected correctly. I'd designed the system to say _I think this_ when it didn't know. I hadn't yet watched it do that on something I didn't know either.

I turned off the lights and didn't say anything aloud. There was no one to say it to.

---

"You want me to cut it where?" said Dolores.

"Anywhere. Anywhere you like. Just don't tell me where."

It was Saturday afternoon, and she'd shown up for her usual pickup and found me standing at the clean bench with a bag of silicone and a block of gel. She'd read my request twice, put her clipboard down on a stack of tires, and said she needed a knife.

Before she started, I did the one thing I'd learned to do. I took an index card, wrote the pass criteria on it, and taped it inside the cabinet door where I couldn't revise it later. _Laceration located within 1 mm. Hidden fluid located within 2 mm, volume inside the stated range. Anything the system can't identify must be flagged, not guessed. Treatment path within 1 mm of the cut. Anything else is a fail, however good it looks._

Then I turned around and faced the wall, and Dolores worked behind me, muttering. I heard the scrape of a knife, the pop of a balloon being filled, and the thud of a fist pressing something into gel.

"Done," she said.

"Cover it."

"Already did. It's under a dish towel."

"Do you remember what you did?"

"Every word. I'm not telling you."

I loaded the phantom into the bay under the towel, kept the towel on until the carriage hood closed, and went through the startup checklist again, because rituals keep you honest. Dolores leaned against the workbench with her arms folded and watched the carriage run its homing sequence.

"It's loud," she said.

"It's a prototype."

"Your mother's lift was louder."

"Fair."

I'd told myself I would stand back and watch the screen and not the machine, because a person standing over a moving gantry makes mistakes. I managed it for about four minutes. The scan took twelve, with the carriage stopping and starting along the phantom's length in its slow patient rhythm, and Dolores stayed through all of it, which surprised me. Halfway through, she offered the observation that it looked like a very expensive printer. I let that go.

The map assembled row by row. At the top, a laceration showed up as a sharp dark line running diagonally across the skin layer. Below the skin, something else appeared. A pocket, rounder than a bruise, with a boundary the ultrasound drew bright and the impedance sensors confirmed as fluid and not gel.

I realized I'd stopped breathing again, and started.

The report came up when the carriage parked.

_Surface laceration detected. Length approx. 41 mm. Depth approx. 4 mm. Edges parted, no foreign material._

_Subsurface fluid collection detected. Depth to center approx. 16.5 mm. Estimated volume 6 to 9 mL. Confidence: moderate._

_Region at lower-left, 12 to 20 mm from the edge: density variation detected. Cannot classify. Confidence: low._

I read the last line twice. I hadn't built a feature to say that. I'd built a rule distinguishing _I measured this_ from _I think this_, the first night, and the system had applied it to something it had never seen.

"What's the low-confidence thing?" Dolores had come around to look.

"It saw something it couldn't identify, and it's telling me so instead of guessing."

"That's more than my last boyfriend ever did."

I didn't have an answer for that.

"Is it right?" she asked. "The numbers. Is it right?"

"We'll see."

I authorized the treatment pass before I opened the bay, because I wanted the head's performance on its own. The system proposed a path along the laceration and marked the fluid pocket as _not for treatment, observation only_, which was correct for a surrogate that had no way to drain or treat it. The head lowered, the pump pushed, and the blue bead ran down the cut with the roller foot closing the seam behind it. It took ninety seconds.

I unlatched the hood, lifted the phantom out, and set it on the bench. The seam was closed and the line was straight.

"Okay," I said. "Now tell me what you did."

Dolores took a breath like someone about to confess. "I cut it with the box knife. Four centimeters, give or take. I put a balloon in with some saline and dye, eight milliliters, I used the syringe from your drawer. I shoved it in from the side, maybe two inches down." She frowned. "Then I stuck a pencil eraser in it, down low, off to the left. Wanted to see if it'd notice."

"The eraser's the low-confidence region."

"Is that what it found?"

"I think so."

She nodded slowly, and for a second looked almost impressed before she caught herself.

I got the card out of the cabinet and measured everything I could. The laceration was forty millimeters by my calipers, a millimeter off the scan, which was right at the edge of what I'd allowed. The balloon sat seventeen millimeters down to its center, within a millimeter and a half. The volume was eight milliliters, inside the system's range though nowhere near the middle of it, and the range itself was so wide it would never have helped a clinician. The blue line followed the cut with a worst-case deviation of about 0.8 millimeters. The eraser sat in the lower left of the block, where the system hadn't known what it was and had said so.

The machine had not been perfect, and I'd have been suspicious if it had. The depth estimate leaned shallow. The volume range was too wide to be useful. The system had no idea what the eraser was. But it had located the injury, characterized the hidden damage, planned a path, and treated the surface wound with a machine I'd built in a loft above a garage. It had told me honestly where its knowledge stopped. By the card, which I'd written before I knew the answers, it had passed.

"So it's a very expensive glue gun," Dolores said.

"Yes," I said. "Yes, that's exactly what it is. For now."

She picked up the phantom and bent the closed seam back and forth with her thumbs. The bead held. She set it down, picked up her clipboard, and looked at me for a moment with an expression I couldn't read.

"Your mother would've wanted to see this," she said.

"She'd have asked what it cost."

"And then she'd have asked who's going to buy it." She tucked the clipboard under her arm. "I'll be back Tuesday. Try not to blow anything up."

She left. The bay door rattled down behind her, and the loft went quiet, with only the cluster humming at the back wall.

---

I sat at the bench for a long time after that, with the phantom in front of me and the machine cooling behind it.

_Who's going to buy it._ It was the question I'd asked myself on the first night, and I'd been answering it with a list of things to build. She'd asked it in four words, with a clipboard under her arm, and no list of mine had an answer.

It worked. I let myself think the words once, plainly, and then put them aside, because they were only the beginning of another list.

It had worked on a silicone block. A silicone block didn't bleed, breathe, flinch, or run a fever. It had no allergies, no infection, no tissue that differed from the next person's tissue, and no history. The scanner had been tested on a handful of phantoms that I'd made or watched Dolores make. The treatment head had closed one cut with a gel that wasn't medicine. The prototype was a bench-scale unit that couldn't hold a whole patient, took thirteen minutes to do what it ought to do in one, and had a failure rate I couldn't state, because I'd run it fewer than two dozen times.

I pulled the pad toward me and wrote the list the way I'd learned to, honestly.

_Reliability: hundreds of scans, not dozens. Find out what breaks at the thousandth run._

_Safety: independent review of every interlock, fault mode, and failure. I designed them. I should not be the only person who has checked them._

_Accuracy: test across tissue types, conditions, injury patterns. A silicone forearm and a balloon don't count._

_Optical: oxygenation channel uncalibrated. Gray cards prove the sensor sees light, not blood. Calibrate against proper references before trusting a single number._

_Medical evaluation: physicians, not me. People who have treated real injuries and know what the machine would face._

_Facility: sterile, controlled, appropriate. Not a loft._

_Oversight: proper review, approvals, and a protocol before anything touches a human being._

I underlined the last two, because they were what stood between a working machine and a medical device, and no amount of engineering would get me across without them. I'd been honest about that at the start, and I intended to stay that way.

I looked at what I'd written. The list was long, and almost none of it was something I could do alone. A loft, a lathe, and a cluster of dead servers had taken me from a diagram to a machine that worked. The next steps needed lawyers to protect the design, accountants to keep the money straight, and engineers who could check what I'd built. They needed doctors who would tell me what I'd gotten wrong, and a building with a door that locked. They needed people, in other words, and a structure for them to work in, and a name on the paperwork that wasn't mine alone.

I thought about the shop downstairs, three bays and a faded sign, and the woman who'd built it from nothing, and the green ledger on the corner of the table with her handwriting at the top of every page. She'd have understood the problem immediately. _A good tool is only worth what you can do with it,_ she'd said, more than once, usually while handing me a wrench. _A shop is a tool too._

I turned the page and started a new list at the top, in a column of its own.

_1. Patent attorney._

_2. Business structure._

_3. Medical advisor._

_4. A real lab._

I looked at the machine one last time. Then I wrote the date at the bottom, closed the pad, and switched off the loft light.

In the morning there'd be a customer with a bad alternator, and I'd fix it.

After that, I had a company to start.