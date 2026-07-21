# The Parent's Key — One-Page Summary

## The Problem

The average age of first exposure to hardcore pornography in the United States is 11. One in ten children sees it before age 9. Anxiety disorders among adolescents have risen 60% in 15 years. Depression, self-harm, and suicide track upward in lockstep with the smartphone.

## Why Everything Has Failed

- **25 US states** have passed age verification laws. All are defeated by a free VPN in seconds. Multiple academic studies show no measurable reduction in youth access.
- **UK, France, EU, Australia** — each deployed a different system. Each was publicly demonstrated as bypassable within days or weeks. VPN downloads spike 400-700% when these laws take effect; consumption does not change.
- **The structural problem**: You cannot regulate a website in another jurisdiction. The domain moves. The server moves. The CEO has no bank account in your country.

## The One Architecture That Cannot Be Bypassed

A single new requirement: **adult content access requires a renewable credential attached to the device's hardware, activated in person by a verified adult after viewing a brief informed-consent acknowledgment. The credential is free.**

### How it works

1. **The credential is in the hardware, not the browser.** The check happens at the operating system level, before any connection reaches the network. A VPN changes where traffic appears to originate — it does not change the attestation on the device's motherboard.

2. **The technology already exists.** Apple's Secure Enclave (every iPhone since the 5s, 2013), Android's Trusted Execution Environment (every modern Android phone), and TPM 2.0 (every Windows PC since 2016) already perform hardware-level attestation for disk encryption, Apple Pay, and corporate security. This is the same capability, turned toward a new question.

3. **The credential is free** — activated in person at any county clerk, DMV, or licensed retailer (same places that sell fishing licenses). Annual in-person renewal forces a yearly conscious choice.

4. **The central database contains zero names.** It stores only device public keys — random values that cannot be reversed or linked to any person. Your name stays at the county office where you activated. Connecting a device to a person requires two warrants: one to identify the issuing county, then a separate warrant to that county.

5. **A child's device is locked by default from the factory.** No adult has activated a credential, so no adult content domain responds. This is true whether the child uses Safari, Chrome, a third-party browser, or an in-app web view — the check is in the kernel, before any application code runs.

6. **Five enforcement layers reinforce the device check:** payment processors (Visa/Mastercard), ad networks, CDNs (Cloudflare, Akamai), ISPs for legacy devices, and mobile app stores (Apple App Store, Google Play).

### What this proposal is NOT

- Not a ban on adult content — adults with a credential access the same content they access today
- Not a database of what anyone watches — the central system returns yes/no, nothing else
- Not a surveillance system — the website never learns who the user is
- Not a new technology — it uses hardware security modules already in 5+ billion devices worldwide

### What NYC could do

The architecture is designed for federal legislation. But cities can start the conversation. Mayor Mamdani could:
- Commission a feasibility study from NYC's CTO office or an independent research body
- Convene child safety advocates, privacy experts, and hardware security engineers for a roundtable
- Be the first elected official to publicly lay out a technically honest path where others have offered theater

## The Full Proposal

Full legislative proposal with constitutional analysis, enforcement layers, privacy architecture, stress-tested holes, and pilot program design:
**https://github.com/RayGilliardGitHub/the-parents-key/blob/main/PROPOSAL.md**

Technical research and international survey of age verification approaches:
**https://github.com/RayGilliardGitHub/the-parents-key/blob/main/docs/research.md**

Stress-test of the model — 12 identified holes, 5 critical, with proposed fixes:
**https://github.com/RayGilliardGitHub/the-parents-key/blob/main/docs/holes.md**
