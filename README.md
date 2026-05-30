# The Parent's Key: A Challenge Paper

**The Problem**

The average age of first exposure to commercial hardcore pornography in the US is 11. A growing body of research suggests correlations between early and frequent exposure and adverse developmental and mental-health outcomes — elevated rates of adolescent anxiety, depression, and distorted expectations of sex and relationships — though causality and magnitude remain debated. The problem is real enough that the UK, France, and the EU have all passed legislation attempting to address it.

**Why Current Approaches Fall Short**

Website-level age verification is structurally vulnerable because the client (the device) can represent itself as being anywhere. Every existing system — the UK's Online Safety Act, France's double-anonymity framework, the EU's age verification app — has been publicly demonstrated as bypassable within days of deployment. The enforcement target (a website in another jurisdiction) cannot be reliably regulated by the jurisdiction where the child lives.

**The Proposal: One Architectural Idea Worth Examining**

> Adult content access requires a renewable credential attached to the device's hardware, activated in person by a verified adult after viewing a brief informed-consent acknowledgment. The credential is free.

The credential check happens at the device level — the operating system queries the hardware attestation module (TPM/Secure Enclave) at every resource boundary. If no valid credential exists, the connection is refused before it reaches the network. The website never knows the device exists.

**The Privacy Architecture**

The central registry stores only device public keys — random high-entropy values generated at activation that link to no device identifier, no serial number, no person. The adult's name stays at the county counter where they activated. Connecting a device to a name requires two independent warrants: one to identify the issuing counter from the registry, then a second warrant served on that specific county. The central system cannot produce a name because it does not contain one.

**The Pilot Gate**

Before any nationwide hardware requirement takes effect, Congress must authorize a pilot: 10,000 devices across three diverse counties, 18 months, full infrastructure. The pilot automatically terminates if false positives exceed 0.01% of sampled legitimate domains or if any vulnerable subgroup (rural, disabled, non-English-speaking) experiences a denial rate above 5%. The trust-root problem must be demonstrated working — either an open trust root with extraction-proof key storage or a published path for independent OS vendors to obtain signing authority. Nationwide deployment requires a three-fifths supermajority vote in both chambers. If Congress does not approve, the pilot devices are recalled and the program ends.

**Additional Features**

- **Device resale**: credential must be revoked before transfer; factory reset wipes the private key
- **International visitors**: 90-day exemption with age-gate fallback for non-US devices
- **Annual renewal**: in-person, free, forces yearly conscious reconfirmation
- **Remote activation**: live video notarization for rural, disabled, homebound adults
- **Sunset**: five years; reauthorization requires three-fifths supermajority

**Constitutional Questions and Possible Doctrinal Paths**

The hardest questions are constitutional. This note does not claim to have resolved them.

The strongest doctrinal path may be Renton v. Playtime Theatres (1986), which treated adult-theater zoning as a content-neutral regulation of secondary effects (crime, property values) — not a speech restriction. The credential could be analogized as device-level zoning: it does not ban or judge any content category, but regulates the environment in which speech is received based on harms to children. This analogy is contestable — courts may see compelled hardware architecture as categorically different from municipal zoning — and the Renton path is offered for examination, not as a settled defense.

Separately, Ginsberg v. New York (1968) establishes that minors may be restricted from accessing material that adults have a constitutional right to see. And McIntyre v. Ohio (1995) protects anonymous speech — which the credential preserves, since the website never learns the user's identity.

The under-inclusivity problem (the proposal excludes social media and encrypted messaging, where much teen exposure occurs) is acknowledged. The defense is incrementalism: the government may address the most structurally tractable vector first. Whether that defense survives strict scrutiny is an open question.

**What This Paper Is Not**

This is not a finished legislative proposal. It is not a lobbying document. It is a challenge paper: an architecture worth adversarial examination by people who know more than the author about the specific domains involved.

**What I Am Asking**

- Constitutional scholars: does the Renton secondary-effects path have a better or worse chance than the Ginsberg variable-obscenity path? Is the under-inclusivity defense viable?
- Privacy and civil liberties: where does the local-only records architecture still leak?
- Firmware/TPM engineers: is the trust-root problem structurally intractable, or is there a path I have not seen?

I am not asking for endorsement. I am asking for the holes I still cannot see.

---

## Repository Contents

- **[PROPOSAL.md](PROPOSAL.md)** — Full legislative proposal with constitutional analysis, enforcement layers, privacy architecture, and pilot program design
- **[docs/research.md](docs/research.md)** — Worldwide survey of age verification approaches (EU, UK, France, US states, Australia, Korea, China, Japan) and why VPNs structurally defeat website-level enforcement
- **[docs/holes.md](docs/holes.md)** — Stress-test of the model: 12 identified holes, 5 critical, with proposed fixes and honest assessment of what remains unsolved
- **[docs/colorado-sb25.md](docs/colorado-sb25.md)** — Summary of the Colorado SB25-104 amendment that triggered this project (OS-level age verification, open-source backlash, the exemption)
