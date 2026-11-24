Author's Note:

Welcome to Chapter 5!

The first real opportunity to prove a company's worth rarely arrives under ideal circumstances.

With Akatsuki taking its first steps into the commercial world, Kenji discovers that developing impressive technology is only part of the challenge. Trust, responsibility, and the willingness to recognize a problem before it becomes a disaster matter just as much.

Looking for Advanced Chapters? If you don't want to wait for the public posting schedule, advanced chapters are live right now on my ***Patreon**.

---
Disclaimer

Road to the Stars is an unofficial work of fanfiction inspired by the Mass Effect franchise and other fictional properties. This story is not affiliated with, endorsed by, or sponsored by Electronic Arts, BioWare, or any other relevant rights holder.

---

**Chapter 5 — The First Business**

"You have a design history," Priya Raman said, "and you have no idea that you have one."

She sat at the steel table with my project log open in front of her and a legal pad covered in handwriting so small I had to lean in to confirm it was handwriting. She'd been in the loft forty minutes. I had expected questions about the machine. She had asked about the notebooks.

"I have a pile of notes," I said.

"You have requirements, design decisions, verification results, and change records, all dated, all in sequence. Everything an auditor wants is in here." She tapped the log. "It's in the wrong drawers. Marcus tells me you've got a system that can sort things."

"It can."

"Then let it sort. But a person signs. Always a person." She turned a page. "I'm told you want a regulatory consultant on contract, not an employee."

"I can't afford an employee who only does regulatory work. I can afford someone who tells me what I'm about to get wrong."

"That's roughly the job." She had twenty years in medical devices, a gray bob, and a face that gave away nothing until she was ready. Marcus had found her through a former colleague. "First question. What does the machine do?"

I started listing: the three-modality scan, the uncertainty map, the path planner, the closure head.

"Stop. That's what it can do. I asked what it's for."

"Imaging and treating soft-tissue injury."

"Those are two devices." She said it patiently, like someone who had given this speech to a lot of founders. "A machine that images tissue to help a clinician decide something climbs one mountain. A machine that puts a closure agent into a human being climbs a different, much steeper one. Intended use decides which mountain, what evidence you need, and what you're allowed to say in a brochure. You choose it before you choose anything else."

"I want both, eventually."

"Eventually is fine. Your first submission is one mountain." She flipped to a fresh page. "I'd pick the scanner. It's closer to ready, the risk is lower, and it can earn while the treatment side catches up. But it's your company."

"I'm not deciding before the evaluation. A trauma surgeon is going to look at the treatment head next week, and I want to hear him first."

"Good. Then I'll hold my opinion until you've heard his, and repeat it afterward." The corner of her mouth moved. She named a rate that was more than I wanted to pay. We went back and forth. I ended with a retainer of fifteen hours a month, additional hours approved in writing in advance, and she got a clause letting her refuse to review any document that claimed more than the data supported.

"You're giving me that for free?" she said.

"I was going to ask you to enforce it anyway."

"Everyone plans to." She capped her pen. "And don't print 'Med-Pod' on anything until we've talked. Someone will read it as a medical claim."

After she left, Marcus and I went through the technician applications. There were thirty-one. The system sorted them by keyword in four seconds, and I read the top ten myself, because it couldn't tell me which of them would say so when I was wrong. We shortlisted three and agreed to interview after the evaluation. I didn't want to hire anyone until I knew what I'd be asking them to build.

Dr. Reyes arrived at six with a paper bag from a diner and a list of names.

"I'm not sitting on your panel," she said, handing me a sandwich. "I'm your paid adviser. If I'm on it, the panel's opinion is worth nothing. I'll observe and keep my mouth shut. I'll fail, but I'll try."

She laid three names on the table. Dr. Samuel Adeyemi, trauma surgeon at the county hospital. Dr. Mei-Lin Zhao, a radiologist who specialized in ultrasound. Tomas Brecht, head of clinical engineering, the man who kept the hospital's equipment from electrocuting anyone.

"Adeyemi will hate it," she said. "Invite him anyway. If he doesn't hate it, you've done something wrong."

I paid each a flat day rate. Gloria drafted the agreements. They signed confidentiality terms, and I signed one promising that their written opinions would go into the design file exactly as written, unedited.

"Even the bad parts?" Brecht asked on the phone.

"Especially those."

---

Dr. Adeyemi arrived first, ten minutes early, and stood at the foot of the stairs looking at the faded red sign.

"Himura Auto," he said, when I came down. "I'm told this is a medical device company."

"It's upstairs. The garage pays for the building."

"Reyes said you'd say something like that." He was a broad, tired man in his fifties, with a surgeon's habit of looking at hands before faces. He looked at mine. "She also said the coffee here is acceptable."

"She was being polite."

"She drank it anyway. That told me something." He went up.

Zhao and Brecht came ten minutes later. Brecht carried a hard-shelled case in each hand. Zhao carried one flat case, the way someone carries a thing she doesn't trust a stranger's floor with. Dr. Reyes took the stool in the corner by the clean bench and visibly folded her hands.

I'd planned the morning in an order that made sense to me. Brecht ignored it.

"Electrical first," he said, setting down a case. "Before anyone touches a switch. Is the unit powered?"

"Off."

"Good. I want the enclosure open and your wiring in front of me, and then I want to measure it." Inside the case was a safety analyzer, a gray instrument with a lot of sockets. "You inject current into tissue."

"For the impedance channel. It's a current source with a hardware limit, independent of the software."

"Show me the limit."

Marcus took that one. He pulled the access panel and walked Brecht through the injection board while Brecht checked part numbers against a notebook of his own. They spoke in a shorthand I half followed. Then Brecht connected the analyzer and ran the leakage tests. The normal condition passed. He asked Marcus to open the ground connection to simulate a single fault.

The number on the display climbed and stayed there.

"Over," Brecht said. "Not by a lot. Over."

Marcus crouched by the supply and read the label. "Filter capacitors. The cheap ones leak to the chassis." He rubbed his jaw. "We reviewed the interlocks. We never ran a single-fault leakage test."

"That's why I'm here." Brecht made a note. "You'll want an isolated, medical-grade supply. They aren't cheap. Now the carriage. Printed shells, layer seams. How do you disinfect it?"

"Wipe-down. Honestly, it wasn't designed for it."

"Then say that, in those words, in every document. And find out what that plastic does after a hundred wipes with hospital disinfectant." He wrote it down. Marcus wrote it down too, in the same posture, and I noticed they were both nodding.

The unit had been powered for the leakage tests for most of an hour. When Brecht reached past the carriage to check the head's mounting, he stopped and laid the back of his fingers against the housing.

"Warm," he said.

"It's been energized a while."

"That's the part that goes near skin." He took a contact thermometer from his case, held the probe to the housing, and waited. He didn't announce the number. He showed it to Marcus, who exhaled through his nose. "Heat's coming up from the pump bracket and through the head mount. On a bench that's nothing. A patient-contact surface has limits, and a clinician who rests a hand on this after a long session shouldn't have to wonder. Log it as a finding."

"Logged," Marcus said, and I wrote it down myself, in the margin of the page, so there would be two records.

Zhao had said nothing. She unpacked a block of tissue-mimicking material the size of a loaf of bread, with a certificate in a sleeve taped to the lid. "Commercial phantom. Speed of sound fifteen-forty meters per second, attenuation calibrated, nylon wire targets at known depths, anechoic cylinders from two to eight millimeters. You didn't make it, so you don't know where anything is. Good?"

"Good."

She stood beside me through the whole scan while the carriage stepped and settled across the block. When the picture assembled, she studied it with her head tilted.

"The wires are in the right place," she said. "Roughly. Your depths read shallow."

She laid the certificate beside the screen and went through the targets one at a time. The deepest wire read about three percent shallow, which at forty millimeters was more than a millimeter off. "Lateral resolution is about two and a half millimeters. My clinical probe gives me one. You see the six- and eight-millimeter cylinders and you lose the four and the two. For a sixty-four element array on a bench, that's honest. I wouldn't call it diagnostic."

"Neither would I. It's a prototype."

"Good." She turned to face me. "What does the impedance channel add?"

"A tissue-type map. It separates fluid from solid from fat in ways ultrasound alone can't."

"Show me it's better than ultrasound alone."

I opened my mouth and closed it. "I have phantom data that says the fused map is clean. I don't have a comparison against ultrasound by itself."

"Then you don't know whether it adds value or only adds complexity." There was no malice in it. "I've watched three companies bolt a second sensor onto an ultrasound array and call it a breakthrough. Design a comparison and give me the raw data."

"I will."

"Bone, ribs, bowel gas. They throw shadows, and a shadow looks like a hole. What does your machine do with a shadow?"

"I don't know. I've never scanned anything that shadows."

She looked at me a second longer than she needed to. "Thank you for not guessing."

---

We ate lunch standing around the steel table, which turned out to be where the real evaluation happened.

"The fusion is the interesting part," Brecht said, around a sandwich. "If it works. Dr. Zhao's right that nobody's shown it does."

"Interesting isn't a reason to build it," Zhao said. "I'd rather have a clean one-modality image and a straight answer about its limits than three imperfect ones averaged together."

"The three modalities are there because no single one sees enough," I said.

"That's a hypothesis. You've written it down as a fact." She said it mildly, and I wrote it down as a task.

Adeyemi hadn't touched his food. "You're all arguing about the picture," he said. "Nobody in my department needs a better picture. We need to know what to do with it. Your machine's picture is going to be a line on a screen at three in the morning, with nine people in the waiting room and one tired person looking at it."

"That's the case for the scanner as a screening aid," Zhao said.

"It's the case for asking what happens after the screen." He looked at the carriage, parked at the end of the bench with its hood open. "Show me the other half. Reyes says it closes wounds."

"Samuel," Dr. Reyes said from her corner.

"I'm asking the man a question."

"You were supposed to let him finish lunch."

He pointed at the sandwich in my hand. "He can finish it while I work."

The phantom he'd brought was a silicone block in a small plastic case, with a clean three-centimeter laceration cut across the top. He didn't tell me what was in it. I loaded it into the bay, ran the startup checklist, and started the scan. Brecht came to stand beside the screen. Zhao stood on the other side.

The map built row by row. The laceration came up as a sharp line. Along the floor of the wound, the impedance channel and the ultrasound each showed something faint and bright, a scatter of small points that neither sensor agreed about.

The report appeared when the carriage parked. _Surface laceration detected. Length approx. 31 mm. Depth approx. 5 mm. Edges parted. Region along wound base: density variation detected. Cannot classify. Confidence: low._

"What's that?" Adeyemi asked.

"I don't know. It doesn't either. It flagged it as unidentified."

"Good. That's the part I wanted to see." He moved to the operator screen. "Now the planner. Pretend I'm a clinician with a full department."

The planner drew a path along the laceration. At the top of the screen, a small amber notice appeared: _Unclassified region along wound base. Review advisory before proceeding._ Beside it were two buttons, a gray _Review_ and a green _Authorize treatment_.

"Does it make me look at the advisory?" Adeyemi asked.

"It shows it."

"That's not what I asked."

"No," I said. "It doesn't make you."

He didn't hesitate. He did not examine the wound, because there was no step that asked him to. He did not irrigate it. He read the amber line the way a man reads the fifth alarm banner of the night, and tapped the green button.

The head lowered. The blue bead ran down the seam and the roller foot pinched the lips closed over whatever was underneath. It took ninety seconds. No one in the loft said anything.

Adeyemi lifted the phantom from the bay, turned it over, and pressed a thumbnail into the seam. Then he opened the plastic case, tipped it, and let a small pile of coarse tan grit run out into his palm.

"Beach sand," he said. "Real wounds come in dirty. A man comes off a motorcycle onto gravel, and there's gravel in the cut. You just sealed it in."

"I didn't," I said. "You did."

"Yes." He looked almost pleased. "I did. Say why."

I took the time to answer it properly. "The scanner found it. The planner flagged it. And all that stood between the flag and the closure was a person tapping a button. The machine did what I built it to do when a clinician authorized it. The flaw is that I let authorization be that easy."

"People tap buttons," Adeyemi said. "I've tapped a thousand of them, and I'm good at my job. At three in the morning the amber banner is wallpaper. I've seen alarm fatigue put people in the ground." He set down the phantom. "Your detection was accurate. That's the unsettling part. The machine knew something was wrong and told you so, and it still ended up where it did, because the workflow didn't care."

"What should it care about?"

"The hard part comes before the machine. A clinician examines the wound. Irrigates it. Looks for foreign material and tendon injury, deeper bleeds, signs of infection. Then they say, under their own name, that they've done it, and that nothing unresolved remains." He tipped the last of the sand into the case. "If the scanner flags something and the clinician decides it's nothing, fine. They're the clinician. But they say that out loud, in the record. They don't scroll past a banner."

"You don't want the machine to refuse you."

"God, no. A machine that overrides me is a different problem. I want one that makes me say what I'm doing." He shrugged. "That's all of it. The closing is the easy part. It's always the easy part."

Brecht, who had watched all of it with his arms folded, finally spoke. "That's an interlock," he said. "It's not a warning. You don't let the treatment mode start without it."

"A software interlock," Marcus said, "plus a hardware enable on the pump."

"If you can't bypass it, I'll sign it. If you can, I won't."

"Noted," Marcus said. For the first time that day, he looked at me instead of at Brecht, and I could see he was thinking exactly what I was.

"The scanner, though." Adeyemi turned back to the screen and found the fluid pocket in the old phantom scan I'd left open from earlier in the month. "The collection behind a closed wound, under skin that looks fine. If that works on real tissue, I'd use it tomorrow. As a screening aid. Not a diagnosis." He said it flatly. "Reyes told me you'd say that last part yourself."

"I would've."

"I know. That's what bothers me." He rubbed his eyes. "I came in expecting to hate a closure machine. I still do. But I'd like to see the scanner on a real patient."

Dr. Reyes made a small noise in her corner.

"Don't," Adeyemi said, without turning.

"I said nothing."

"You were thinking it loudly."

---

The written reports arrived a week later, three documents totaling thirty-one pages, and I put them in the design file without touching a word, as promised.

Then I fed them to the system.

I read each report twice first, so I'd have my own opinion before it gave me one. Then I asked it to extract every finding and sort them by the kind of problem they were. It returned forty-seven, in three groups.

The first was engineering problems I could fix: the leakage, the isolated supply, the cleaning of the shell, the depth bias, the heat rising into the treatment head. The second was validation questions I couldn't answer yet: whether fusion beat ultrasound alone, what shadows did, how any of it behaved on something that wasn't gel. The third was clinical and regulatory: intended use, the closure workflow, what anything could be called in print.

Then it noted what I hadn't asked for. Nearly every item in the second group traced to one root. _All performance data derived from phantoms. No data from human tissue._

"Yes," I told the empty loft. "I know."

It was true and it was fair, and it was something I couldn't fix with a mill. Human data meant an ethics review, volunteers, clinical sites, and a protocol someone else approved. I was months from being allowed to ask the question.

The depth bias I could fix, and I did, that afternoon. Zhao's certificate said 1540 meters per second. The value baked into my software, measured in my own gel weeks before, was about three percent lower. I'd stored it as a constant, and against any other medium the machine read shallow, exactly as her wires had shown. It belonged in the software as a parameter with an uncertainty attached. The system and I rebuilt that part of the depth calculation, I checked it by hand against her certificate, and on her phantom the bias collapsed to a fraction of a percent. I wrote in the log that this fixed my assumption and not the larger question. A phantom with a correct constant said nothing about tissue, which varies from person to person and from one inch to the next.

Then I called a meeting.

We sat around the steel table on a gray Thursday: Marcus, Dr. Reyes, Priya on speakerphone because another client's deadline had won, and me with three reports and a clean pad.

"My read," I said. "The engineering items belong to Marcus and me. We fix them first: isolated supply, disinfectant testing on the shell, depth correction, which is done. The validation items need data I can't get without human subjects. And the closure workflow needs a clinician gate that I'm not going to design alone."

"The scanner is the product," Priya said from the phone. "I said that two weeks ago, and I'm saying it with Dr. Adeyemi's report in front of me."

"I disagree," said Dr. Reyes.

I'd expected her to. "Go ahead."

"Everything Adeyemi said about exploration is right. He's also a trauma surgeon, and he treats every wound as a night in the OR. I see forty a shift who don't need one. If the closure head only ever lives in a research lab, you've built the wrong product for the people who need it most." She leaned forward. "Don't drop it. Gate it."

"I'm not dropping it. I'm sequencing it." I drew a line down the middle of the pad. "The scanner goes up the first mountain. It's closer, safer, and it earns while the rest catches up. Closure stays in development as research, behind a clinician gate that nobody will let me design alone. It doesn't ship, and I won't promise a date for it to anyone. When the scanner has earned some credibility and the gate has been built with clinicians, the head gets its own path."

"That's what I said," Priya said.

"You said it. I decided it."

"Noted." I could hear her smiling.

Dr. Reyes sat back. "That's fair. I want it in writing that I told you so, when it comes back around."

"I'll have Pruitt notarize it."

I wrote the roadmap down the page in order. A reliability campaign of a thousand logged scans. A comparison on phantoms, with Dr. Zhao reviewing the raw data, to learn whether fusion earned its place. Shadow phantoms with bone and gas mimics. Oximetry calibration against real references. Priya's quality system, which she'd already started by sorting my notebooks into drawers. And Dr. Reyes's protocol, rewritten as an ethics submission for a first study with volunteers and imaging only, where nobody was treated and nothing was closed.

Under that I wrote what we needed. A reference-grade ultrasound system to rent. A space with a door a regulator would respect. A technician, maybe two. And a partner site, because an ethics board wouldn't approve a study that had nowhere to happen.

"A partner site," Dr. Reyes said. "That's the one I can't give you. My hospital competes with half the people who'd want this. You'd get six months of committee meetings."

"I know. I'm working on it."

I hadn't known I was working on it until I said it. But the shop had been working on it for me since seven that morning.

---

The mobile clinic van had been in bay two since seven, and the man standing beside it had been on his phone since seven-oh-five.

"Alternator?" he asked, when I came out. He was in his late forties, gray at the temples, in a good coat with a lanyard that read TRI-COUNTY COMMUNITY HEALTH NETWORK. "That's what the last garage said."

"Let me check before I agree with them."

It took thirty minutes. The van died intermittently when the vaccine refrigeration unit cycled on, which pointed at a power problem under load, and a corroded ground strap between the body and the chassis turned out to be the whole story. I cleaned the contact, replaced the strap, and ran the van with every accessory on for fifteen minutes. The fridge cycled, the lights held, the van kept running.

"A strap?" He looked as if he wanted to be annoyed and couldn't find the reason.

"A strap and a bolt. I'll charge you for the strap."

"Mr. Okafor said you'd find it fast. He also said you'd charge me too little." He paid, and lingered at the bay door. "Raymond Teague. I run operations for the network. Nine clinics, two of these vans, one county, and not enough of anything."

"What's short?" I asked, and he walked through the door I'd opened.

Most of the county, he told me, was forty minutes or more from an imaging suite. An ultrasound technician visited the biggest clinic on Thursdays. Anything that might need imaging the other six days went by ambulance to the county hospital, and many of those trips came back with nothing wrong. "A hundred and forty last year," he said. "At about eleven hundred dollars each, before anyone counts the patient's day."

"What if a nurse at the clinic could scan the patient, and a clinician decided whether the transfer was needed?"

He was quiet a moment. "Is that a pitch?"

"It's a question. I'm building something that might do part of that. It's early and it isn't approved for anything. I'd like you to look at it and tell me whether your clinics would use it."

"Honestly?" He glanced up at the sign. "I've been pitched imaging devices by people with sales teams. You're the first to tell me up front it isn't approved."

"It wouldn't be much of a pitch if you found out later."

He came upstairs that afternoon after he'd moved the van. He watched the demonstration twice and asked three questions, studying the machine as if pricing a chair he wasn't sure he could afford. I told him what Adeyemi had told me and what the machine couldn't do. He said "the scanner" twice, took a copy of the protocol outline, and promised to call by the end of the week.

He called Wednesday.

---

The network's headquarters was a converted bank branch with the vault door still in the wall, and the conference table stood where the tellers used to be. Teague had brought his attorney, a brisk woman named Ms. Odom with a folder tabbed in four colors. I brought Gloria, who had read the draft three times on the drive.

"Our board approved forty-five thousand dollars from the rural innovation fund," Teague said. "In three payments. It has to be committed by the thirty-first or it goes back. I assume you've guessed my deadline."

"Walter guessed it."

"Then you know I have leverage problems." He smiled thinly. "I should tell you the board also has two other proposals on the table, from companies with sales teams and a finished product. I'd rather work with you. I'd prefer not to be talked into it."

"I'd rather you weren't."

Odom slid the draft across. "Five years of statewide exclusivity in exchange for the full forty-five."

"No," I said. "Not for forty-five thousand and not for a prototype. I'll give you a right of first negotiation on a commercial license for your service area, for twelve months after the bench verification report. If you like the numbers, you negotiate first. If you don't, or we can't agree, I'm free."

"That's thin," Odom said.

"It's a prototype. It's what it's worth." I kept my voice level. "I'm not refusing your money. I'm refusing to sell the future of the technology with the first payment."

Teague looked at his attorney, then at the draft. "Twelve months. Fine. What else?"

"Section six. Improvements arising from your clinical feedback belong to the network."

Gloria spoke for the first time. "Your clinicians evaluate the device. They don't develop it. Akatsuki owns the invention and everything built on it. In return, the network receives a no-cost license to use pilot units during the study, and a clause stating that clinician comments can't ground an ownership claim."

Odom conferred with Teague in a whisper. "Acceptable."

"Then there's the grant," Odom said. "Your application to the state. If it comes through, does the network's money get absorbed into your budget? The board won't want to learn that its forty-five thousand became a rounding error in a hundred and fifty."

"The two are separate," I said. "The grant is for the evaluation protocol and a rented bench, and it's not approved. Your money is for the bench verification and the study site. If the state says no, your deliverables don't change. If it says yes, they don't change either. I'll put it in the contract that neither funds the other."

"Put it in the contract," Odom said, and wrote it down.

"Now section nine," I said.

Teague's face shifted. I'd known it was coming. Section nine required a working wound-closure unit for pilot use at two clinics by June.

"That's what the board cares about most," he said. "A scanner is helpful. Closure is what lets my nurse practitioners see more patients. And I'll be direct. Our other two proposals offer it."

"Then take them, if they'll sign it."

Silence.

"I can't promise it," I said. "The head has never touched a human being. The surgeon who reviewed it told me why it shouldn't yet, and he was right. If I sign a deliverable I know I can't meet, you're buying a date, not a device. In December you'd have a missed June and a broken contract, and so would I."

"That's a hard thing to tell a board."

"Tell them imaging is the part that works." I leaned forward. "Here's what I can offer instead. A feasibility report on closure, written by us and reviewed by Dr. Adeyemi, covering what a clinician-gated workflow would take. No delivery date. You'd learn what a clinic would need and what it would cost, before anyone else."

Teague looked at Odom. She shrugged. "It's more than a promise."

"It's more than a promise," he said slowly. "It's less than I wanted." He slid a page across. "Price. The board will ask what a unit costs."

"I can't tell you."

"You must have an idea."

"I know what the prototype cost. That isn't a product's cost. If I quote a ceiling now, I either lose money or break the promise, and neither helps you. After verification, when I know what it takes to build one reliably, I'll give you a real estimate. You'll see it first."

"My board won't like that."

"They'd like it much less in a year."

He almost laughed. "I wish I could argue with that."

We spent another hour on the smaller things. Payments in three installments of fifteen thousand: at signing, at delivery of the bench verification report, and when an ethics board approved the first volunteer study. The network's clinics as study sites, subject to that approval, with staff trained and compensated for their time. Confidentiality that covered the machine's internals. A termination right for either side with thirty days' notice and payment for completed work.

"One more thing," Teague said, as Odom squared the pages. "If the verification fails. If the numbers come back and the machine doesn't do what you say."

"Then the report says so, in plain words."

"In writing?"

"That's what the report is for."

He studied me for a long moment. "I've been doing this a long time, Mr. Himura. I don't think I've ever signed a contract where the other side promised to report its own failure."

"You haven't signed it yet."

"No." He picked up a pen. "But I think I will."

---

Teague signed on the twenty-ninth, two days before his budget closed, in the loft, with Dolores watching from the top of the stairs with a clipboard against her chest.

"That's the deal?" she said when it was over. "Forty-five thousand?"

"In three parts, and a place to run the study."

"Your mother ran this shop for twenty years on less."

"My mother wasn't buying isolated power supplies."

She considered that and nodded. "Fair."

That night I sat at the bench with the signed agreement and the numbers Pruitt had called in that afternoon. The first payment bought about two months of runway. If the others came on schedule, it bought a third. It was no fortune, and the state grant was still a letter I might not get. But it was money from someone who wasn't me, for work that had to happen anyway, with a clinic network that had agreed to be the place where it would.

I made the list that had to come next.

_1. Isolated medical-grade supply. Marcus. Order this week._

_2. Disinfectant testing on shell materials. Heat path from pump bracket into head mount._

_3. Clinician gate on treatment mode: examination, irrigation, attestation, unresolved flags resolved on record. Hardware enable on the pump. Design with Adeyemi._

_4. Reliability campaign: one thousand scans._

_5. Fusion comparison. Raw data to Dr. Zhao._

_6. Shadow phantoms._

_7. Quality system with Priya._

_8. Technician interviews._

_9. Reference ultrasound. Ask Zhao._

_10. Space._

I looked at the tenth item. Marcus had left a printout on the bench that afternoon, with a yellow note in his block capitals. _Unit 14, industrial park. 2,400 sq ft. Vacant since spring. Landlord flexible?_ The listing showed a concrete floor, a roll-up door, and one window someone had painted shut.

I didn't call that night. I called in the morning, and the landlord's agent, a man named Pell who sounded as if he'd been waiting since spring, offered to meet us Saturday.

---

Pell let us in at two, handed me the key on a loop of wire, said he'd be across the lot with another prospect and to bring it over when we were done, and left, which I appreciated more than I let on.

The door stuck, then gave. Inside, the air was cold and smelled of dust and old concrete. The roof was high enough to hang a crane from. Our footsteps went out across the floor, hit the far wall, and came back a half second late, as though the room were answering.

Marcus walked the length of it once without speaking and stopped under the painted-over window. "Power's three-phase," he said. "I checked the panel. Loading dock on the east side. It floods in the northwest corner, you can see the stain. There's no cleanroom and no HVAC to speak of." He turned around. "It's perfect."

"It's an empty box."

"It's an empty box that doesn't have a lathe in it."

I'd brought my mother's steel tape, the twenty-five-footer with the dented hook, and a stick of chalk from the shop. Pell had said chalk was fine, since the floor had seen worse. I handed Marcus the end. We walked it out across the floor, and where the tape ended I chalked a line, then turned and chalked another, until there was a rectangle on the concrete about the size of the clean bench area I'd drawn on my pad, and then, because Marcus kept pointing, a second one next to it, and a third.

"Reliability bay," he said, tapping the first. "Clean area, controlled access. Storage here. Dr. Reyes gets an office."

"Dr. Reyes gets a stool."

"Dr. Reyes gets a door that shuts." He looked at me. "Are you signing?"

"Not today."

"Why?"

"Because the first payment hasn't cleared, the grant is a letter I haven't gotten, and Pruitt hasn't run these numbers. Two months of runway isn't a lease." I looked at the chalk lines. "If I sign this and the grant fails, you and Ines and Dr. Reyes find out before I do. I'd rather know what it costs before I know what it feels like."

"That's a good answer." He sounded disappointed in it. "But you want it."

"Yes."

I stood inside the largest rectangle. It was bigger than anything the company had ever owned, or ever would, unless I signed something. The loft held a mill, a bench, and a cluster of old servers, and one man could cross it in six steps. Here there were forty feet in every direction and nothing in them yet. I said "Hello," not very loudly, and the room said it back.

"Chalk comes off," Marcus said.

"A lease doesn't."

"No." He reeled in the tape for me, and the dented hook clicked against the case. "But somebody's going to need the space."

I looked at the lines at my feet, gray against the concrete, already smudged where we'd walked over them. By Monday someone would have swept them away. Tonight, in the cold light of a window nobody could open, they were the only plan the room had.

We locked up and crossed the lot to where Pell stood beside a gray sedan, talking to a woman in a safety vest who was plainly not interested in a building with a flooded corner. He saw us coming and excused himself.

"Well?" he asked.

I held out the key on its loop of wire. "Thank you for the time. I'll call you once my accountant has seen the numbers."

He took it, and his hopeful look didn't quite go away. "It won't be vacant forever."

"I know."

"That's what they all say." He pocketed the key. "Call me."

Marcus and I walked back to the truck. I didn't look over my shoulder at the building until we'd reached it, and when I did, the roll-up door was already down, and nothing about it showed that anyone had stood inside and said hello. But my hands remembered the weight of the key on its wire, and I knew exactly what I'd do first. I went home to call Walter Pruitt.