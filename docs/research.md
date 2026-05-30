# Deep Research: Protecting Children from Pornography — Approaches Worldwide

## 1. The Regulatory Landscape (as of May 2026)

### European Union — DSA + Age Verification App
- **Digital Services Act** Article 28 requires platforms to assess/minimize risk to minors
- **April 2026**: EU launched a free, open-source age verification app built on the EU Digital Identity Wallet foundation
- President von der Leyen: "Self-declaration is dead" — tick-box age confirmations are no longer sufficient
- App is "completely anonymous," "works on any device," fully open-source, made available to partner countries globally
- Built by Scytáles (Sweden) + T-Systems (Germany); pilot in Denmark, France, Greece, Italy, Spain
- A Special Panel on child safety online formed in March 2026 is exploring a harmonized EU-wide minimum age for social media

### France — ARCOM "Double Anonymity" (strictest enforcement model)
- **SREN Law** (May 2024): porn sites must deploy age verification meeting ARCOM's technical standard
- **"Double anonymity"**: the site never learns WHO the user is; the age verifier never learns WHICH site is visited
- November 2024 technical standard published; transitional period ended **April 11, 2025**
- Bank card verification no longer sufficient — must use privacy-preserving, data-minimizing systems
- Facial age estimation must be free from ethnic bias
- Independent third-party verifiers required (legally and technically separate from the porn platform)
- **August 2025**: ARCOM verified 6+ major porn sites are now compliant
- Also attempting a **minimum age of 15 for social media** (legislatively stalled due to EU law conflict)
- France also introduced mandatory sex education covering consent, online porn risks, gender identity (Jan 2025)

### UK — Online Safety Act (OSA)
- **Ofcom** mandates "highly effective" age assurance for:
  - Part 5 services (pornography sites): enforced from **July 25, 2025**
  - Part 3 services (user-generated content): live age assurance from July 25, 2025
- Acceptable methods: AI facial age estimation, government-issued ID, mobile carrier verification, bank-verified age
- Fines up to £18M or **10% of global annual turnover**
- Children's Commissioner: average age of first exposure to explicit content is **13**, 1 in 10 by age 9
- **Critical weakness**: VPN bypass is trivial — users simply appear to be in another country
- UK consulting on potential minimum age for social media, change to age of digital consent (currently 13)
- Pornhub has threatened to geo-block the UK entirely

### Germany — Dual System (JuSchG + JMStV)
- Federal **JuSchG** (Youth Protection Act) + state-level **JMStV** (Interstate Treaty on Youth Media Protection)
- Pornographic content providers must use age verification systems evaluated by the **KJM** (Commission for Youth Media Protection)
- **April 2025**: German courts upheld blocking orders against Pornhub and YouPorn for missing age verification
- Industry push for device/app-store-level age verification to shift implementation burden from individual websites
- Criticized for complexity and "overblocking" — December 2024 draft amendment caused business concern about excessive filtering

### United States — State-Level Patchwork (25 states + pending federal)
- **Supreme Court (June 2025)**: ruled age verification gates for adult content do not facially violate the First Amendment
- **25 states** now have active age verification laws for adult content sites (threshold: typically 33.3% "substantial portion")
- Methods: government ID, facial age estimation, credit card checks, digital ID wallets
- **Pornhub has blocked access in 23 states** rather than comply — users trivially bypass via VPN
- **EFF evidence**: VPN app downloads spike immediately when these laws take effect; actual porn consumption does not drop
- Federal: **KOSA** (Kids Online Safety Act, introduced May 2025); **Parents Decide Act** (April 2026, OS-level age verification at setup)
- Enforcement varies: $5,000–$10,000 per day fines; private lawsuits also permitted in some states
- First Amendment challenges ongoing in lower courts despite SCOTUS ruling

### Australia — New Industry Codes (Dec 2025–Mar 2026)
- eSafety Commissioner enforcing age verification for porn sites
- Acceptable: facial age estimation, digital wallets, photo ID
- VPN app downloads surged from 40th to 7th in iPhone app charts within days of enforcement
- Fines up to **$49.5M per breach**
- Also covers AI companions/chatbots — must block content inciting suicide/self-harm to minors
- Academic criticism: restrictions may drive traffic to illegal sites

### Canada — Bill S-209
- Introduced April 2026 by Senator Miville-Dechêne
- Targets commercial porn providers; requires effective age verification or estimation
- Still in legislative process

### South Korea — Most Comprehensive Identity-Linked System
- National **resident registration number** used across all online services for age verification
- Mobile carrier integration for age verification
- **Youth Protection Act** + **Information and Communications Network Act** empowered the KCC to monitor/restrict harmful content
- "Cinderella Law" (minors under 16 barred from online gaming midnight–6AM) was **lifted in 2021** but age verification remains
- Pornography is **largely illegal domestically**; foreign sites blocked
- Approach raises significant surveillance and privacy concerns

### China — Strictest System
- Mandatory **real-name registration** for virtually all online services
- Government ID + facial recognition at login for gaming
- Minors limited to small number of gaming hours per week
- Facial recognition used to detect children using parents' accounts
- Enforced via social credit system penalties

### Japan — Cooperative Industry-Driven Model
- No single age-verification law
- **Mobile Carrier Age ID system**: carriers share age attribute when users register with phone number
- Sector-specific regulations for adult content (manga, videos)
- Minimal government enforcement

### Other Notable Approaches
- **Norway**: announced law to prohibit social media for under-16s; platform providers responsible for age verification
- **Spain**: Draft Organic Law raising digital consent age from 14 to 16; OS manufacturers must provide risk information
- **Italy**: AGCOM resolution (2025) requiring two-step (identification + authentication) age verification for porn/gambling/alcohol/tobacco
- **Austria**: committed to draft law by June 2026 establishing minimum age of 14 for social media
- **Singapore**: mandatory parental controls + AI/ML detection of age-restricted content via ISP-level blocking

---

## 2. The Fundamental Flaw: VPN Bypass

**Every jurisdiction mandating website-level age verification faces the same unsolved problem:**

- Users simply use a VPN to appear to be in an unregulated jurisdiction
- VPN usage is **legal** in essentially all democratic countries
- One-click in most VPN apps; free options widely available
- VPN app downloads spike measurably when age verification laws take effect (Australia: #40→#7 in days; UK: similar pattern)
- Pornhub has chosen to geo-block entire states/countries rather than implement verification — users bypass via VPN

**Evidence from studies:**
- EFF: "Users didn't stop accessing adult content after the laws went into effect, they just changed how they got to it."
- Phoenix Center research: no measurable reduction in youth access from state age verification laws
- "The internet always routes around censorship"

**Technical impossibility**: You cannot simultaneously (a) let a user browse the open web, (b) determine their real location, and (c) preserve privacy — without fundamentally breaking how the internet works. Blocking VPNs requires mass deep-packet inspection, which is incompatible with privacy rights and encrypted traffic (which is now the vast majority of web traffic).

---

## 3. The Cigarette & Alcohol Model — Distribution-Interface Responsibility

Your intuition about the cigarette/alcohol regulatory model is sharp. Let me lay out how it actually works:

### Tobacco Regulation (US model)
- **FDA regulates at the RETAIL level** — the seller (store clerk, cashier) must check ID for anyone under 27
- **Three-tier liability**: Manufacturer → Distributor → Retailer. Each link has licensing requirements, inspections, and penalties.
- **Enforcement**: undercover stings, compliance checks, fines, license suspension/revocation
- **Key insight**: The BURDEN is on the distribution interface (the store), not the manufacturer, not the consumer. The store has a physical location, employees, a license — there's an accountable entity you can actually regulate.
- **Result**: Before Tobacco 21 (raising age to 21), retail compliance rates were already above 90% in most states.

### Alcohol Regulation (US three-tier system)
- Post-Prohibition framework: **Producer → Distributor → Retailer** must remain separate
- States use either **Control model** (gov runs liquor stores — 17 states) or **License model** (licensed private retailers)
- The **retailer** bears the legal burden of checking IDs
- Enforcement: sting operations, license revocation, criminal penalties for selling to minors
- **Critical detail**: The law doesn't require the *customer* to prove their age — it requires the *seller* to verify it. The burden is entirely on the distribution interface.

### Application to Digital Porn

The question is: **Who is the digital equivalent of "the retailer"?**

| Physical World | Digital Equivalent | Accountable? | Enforceable? |
|---|---|---|---|
| Store clerk | Website operator | Yes, but globally distributed | Weak — jurisdiction gaps, easy to move |
| Store license | Domain registrar/DNS | Possibly | Weak — many countries, ICANN limitations |
| Distributor | ISP | Yes | Strong — ISPs are regulated utilities |
| Manufacturer | OS maker (Apple, Google, MS) | Yes | **Strongest option** — single points of leverage |
| Retail location | App Store | Yes | Strong — Apple/Google control these |
| Cash register | Browser/OS API | Yes | Emerging approach |

**The OS/device level is the closest digital equivalent to the "store clerk" in the tobacco model:**
- Apple, Google, Microsoft, and (for desktops) OS vendors are identifiable, accountable entities with a physical presence in every jurisdiction
- They already control what runs on devices and have existing age-gating infrastructure (Apple's Screen Time, Google's Family Link, Microsoft Family Safety)
- They already have payment relationships with users (Apple ID, Google Account, Microsoft Account) that could anchor age verification

**This is what Colorado SB25-104 tried to do**, and the open-source community correctly pointed out that it breaks for:
- Linux distributions (no single accountable entity)
- Self-built/compiled software
- Code repositories distributing source code
- Container systems like Docker

The Colorado amendment effectively created exemptions for open-source. The **Parents Decide Act** (US federal, April 2026) tries a different tack: require age verification at OS setup, give parents control, and require OSes to make user age data accessible to app developers (via a privacy-preserving API).

---

## 4. The "Adult Responsibility" Framing

Your observation — "the adult who brought the electronic equipment is responsible for how it is used" — maps to how we handle many physical-world goods:
- A parent who buys a TV is responsible for what their child watches (but broadcast TV also has watershed rules)
- A parent who buys a car is responsible for who drives it (but there are also licensing laws)
- A parent who buys a smartphone is responsible for what the child does on it

**Strengths of this approach:**
- Clean legal framework: parental duty of care already exists in law
- No privacy/First Amendment issues
- No technical infrastructure required
- No VPN bypass problem
- Empowers parental choice rather than imposing one-size-fits-all

**Weaknesses:**
- Doesn't address children accessing porn on devices they own, on friends' devices, or on school/library devices
- Effectively says "the problem is solved if parents are good enough" — but many parents lack digital literacy
- Doesn't help in abusive/neglectful households (where the risk is often highest)
- Doesn't address production of CSAM or sextortion
- Ignores that the online environment is *designed* to maximize engagement, including for children
- Places 100% of the burden on the individual consumer, 0% on the industry that designs addictive/directed products

**The real answer is probably both**: parental/responsible-adult accountability AND systemic regulation. These are not alternatives — they're complements.

---

## 5. What the Evidence Says Actually Works

### What IS Supported by Evidence

**1. Comprehensive sexuality and digital literacy education — strongest evidence**
- Costello (2025, University of Bath) critical review: "Child-focused educational interventions are proposed as the **superior strategy**, addressing gaps in digital literacy and sex education whilst empowering children to independently navigate online risks."
- This is supported by both psychosociological theory and empirical research
- UNESCO/WHO: CSE delays sexual initiation, reduces risk-taking, does NOT increase sexual activity
- France's model (Jan 2025): primary school (emotions, consent, body awareness) → middle school (puberty, online porn risks, gender stereotypes) → high school (consent, gender identity, sexual violence)

**2. Active parental mediation (educational, not restrictive)**
- More effective than simply blocking/filtering
- Requires high parental digital literacy — which is unevenly distributed
- Parents discussing content critically with children works better than installing blockers

**3. Multi-layered approach**
- No single intervention achieves full protection
- The most effective systems combine: education + parental involvement + technical guardrails

### What Is NOT Supported by Evidence

**1. Restrictive parental mediation alone** — "largely ineffective" at reducing online risks
**2. Website-level age verification alone** — trivially bypassed via VPN, no measurable reduction in youth access
**3. Filtering/blocking alone** — "These controls don't work well" (multiple academic sources); "no filter is 100% effective"

---

## 6. Synthesis: The Best Way Forward

### The Unstated Goal
The user's framing is precise: keep children from **seeing, receiving, OR producing** porn or porn-equivalent content. These are three distinct problems:
1. **Seeing** (accidental/curiosity-driven exposure) — education + device-level controls
2. **Receiving** (peer sharing, grooming, sextortion) — education + platform accountability for CSAM
3. **Producing** (self-generated content, coercion) — education + law enforcement + platform safety design

### The Best Approach (from the evidence)

**Layer 1 — Education (foundation, most evidence-based)**
Mandate comprehensive, age-appropriate digital literacy + sexuality education in all schools. Model: France 2025 curriculum. This is the ONLY intervention that demonstrably reduces harm at population scale regardless of technical bypasses. It works even when children access content despite all other controls.

**Layer 2 — Choke-point regulation at OS/device level**
The tobacco/alcohol model applied correctly: hold the distribution interface accountable.
- OS vendors (Apple, Google, Microsoft) must provide age-verification at device setup
- Parents verify children's ages — OS provides privacy-preserving age signals to apps
- Open-source exception (the Colorado lesson) — code repositories, container systems, and modifiable software distributions are exempt
- This creates a "retailer-equivalent" that actually exists, has assets, and can be regulated

**Layer 3 — Platform-level "double anonymity" verification (France model)**
For commercial adult content platforms, require independent third-party age verification where:
- The site doesn't learn the user's identity
- The verifier doesn't learn which site is visited
- No data retained after verification
- This is the most privacy-preserving implementation available

**Layer 4 — Active parental tools (not passive filters)**
Device-level tools (Screen Time, Family Link, etc.) that support active parenting rather than replace it. Combined with educational resources for parents to develop digital literacy.

**Layer 5 — Supply-side enforcement**
Target the production and distribution of CSAM specifically (not general adult content):
- Hash databases (IWF Image Intercept tool, Project Arachnid, NCMEC CyberTipline)
- AI detection of CSAM in cloud/encrypted contexts (ongoing technical and privacy debate)
- International law enforcement cooperation
- Financial pressure on payment processors

### What Would NOT Be the Best Approach

- **Pure website-level age verification alone** (US states model) — VPN bypass makes it theater
- **Total real-name registration / surveillance** (China/South Korea model) — incompatible with democratic values and privacy rights
- **Absolute parental responsibility alone** — abandons children in abusive/neglectful homes and doesn't address systemic design issues
- **Blanket OS-level without open-source carveouts** — kills innovation and violates software freedom principles
- **Criminalizing VPNs** — would require mass surveillance that democratic societies reject

### The Honest Bottom Line

100% prevention is impossible in an open, encrypted, global internet. The goal should be **harm reduction**, not perfect enforcement. Just as we don't eliminate underage drinking but reduce it through licensing, education, and retail enforcement, the digital equivalent must combine:

**Education (best evidence) + OS-level accountability (best leverage) + Platform-age verification (best privacy-preserving tech) + Active parenting (best individual strategy)**

These layers are additive. Each catches what the others miss. None alone is sufficient.
