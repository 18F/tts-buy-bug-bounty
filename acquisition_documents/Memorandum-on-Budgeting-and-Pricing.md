# Memorandum on Budgeting and Pricing

# TTS Bug Bounty

This memo expands on the TTS Bug Bounty budget proposed in the ICGE. It covers how the budget was projected, why the model is structured the way it is, and some background on pricing bug bounties.

## Summary
Projecting costs for a bug bounty is difficult, particularly since we are paying for discovery of unknown issues. To mitigate this uncertainty, we have estimated a per-quarter “bounty pool” based on industry averages, and am asking the vendor to work with us to effectively manage that pool. This converts an unknown into a Not-To-Exceed (“NTE”) cost, and gives us flexibility to modify our program within that cost to spend money most effectively.

There are a variety of ways vendors might structure their platform fees. In the ICGE we have chosen a structure that I believe is most advantageous to TTS. The per-app structure matches how TTS plans to use the bounty, keeps our costs fixed, and gives us maximum flexibility to add or remove apps over the life of the contract. 

## Background: costs associated with bug bounties
The idea seems simple enough: pay for discovered security issues. However, successful programs have costs far beyond just the rewards paid out:

* Promotion: there are thousands of bounty programs available now; you need a way of getting your bounty in front of researchers, ideally good ones. 
* Tracking and workflow: how will you receive submissions, track and manage them throughout their lifecycle? You may be able to re-use existing ticketing or workflow software, but bounty programs have several important details that mean they are much easier to manage with purpose-built software.
* Triage: successful programs receive dozens of reports per month, but the signal-to-noise ratio is low. On average, only about 10% of submissions turn out to be valid (FN1). But all submissions need responses, or else you risk alienating researchers. The workload of filtering submissions and communicating with researchers can be quite heavy.
* Payouts: successful bounty programs result in many small payouts to researchers. Payouts average around $300(FN2), with dozens or even hundreds of payouts over the life of a program. Most accounts payable departments struggle to manage these small payouts.

These costs add up, and quickly: it’s common for the total cost of a bounty program to be many times the actual rewards paid out, especially if you factor in the personnel costs associated with all the manual steps here (tracking, triage, managing payouts, etc) or the costs of developing custom workflow tracking software.

That’s where platforms like the one we seek to procure come in. These platforms have their own costs, but they are spread out over all of the platforms’ customer base. They provide all the services listed above (and a few more) in a single place, and tend to do so at a lower total cost(FN3). 

Platforms typically provide triage services as a separate option, so this mean that the budget for a bug bounty on a platform will have 3 components:

1. The “bounty pool” -- the actual funds paid out to researchers as bounty rewards.
2. The cost of access to the network and use of the platform’s SaaS workflow tracking software.
3. The cost of first-line triage and communication services.

## The structure of the TTS Bug Bounty Pool
The IGCE shows a single line-item for a bounty pool (about $50,000 per quarter). What is this number, how did we estimate it, and how will that line-item be spent?

Ultimately, estimating what we will pay out for vulnerabilities is an impossible task. we are paying to discover *unknown* issues in our software. We can assume that we have some vulnerabilities -- all software has vulnerabilities -- but if we knew more about them, we wouldn’t have to pay to have them found!

Our response to this uncertainty was to do two things:

First, estimate what we might expect to spend based on data from industry averages (FN4). This assumes that our apps are “average” for the industry, which may or may not be a valid assumption, but we have no proof that we are not average, so that was a starting point. Applying industry averages, along with industry average pricing for vulnerabilities(FN5) gave us a monthly estimate of $15,600. We estimated an even split between reports against login.gov and the remaining 4 apps in our portfolio. Login.gov is a larger surface than any of the other apps we are considering, so we can expect it to have more issues. It’s also a far more compelling target, so we can expect more researchers to be interested in it than other apps, which equates to more bounty payout.

Second, since it would be a mistake to assume the actual bugs found will perfectly match our estimates, we structured the procurement such that we give ourselves maximum flexibility to spend our budget in the most appropriate way. The procurement does this by establishing a “bounty pool”: an NTE pool of funds to be spent directly on bounties. we will work with the vendor to establish a fee structure -- that is, the different rewards for vulnerabilities of different severities (low, medium, and high). we will have flexibility to change this structure as the program progresses. For example, if we discover over the period of the program that we are seeing fewer high-severity bugs than expected, we could increase the reward to incentivise reporters to look a little harder.

## Pricing structures for bounty platforms and the best choice for TTS
With the bounty pool and its management in mind, let’s look at the other two line-items in the IGCE: the program access and per-app fees. Why structure the IGCE that way?

There are a variety of ways that a platform provider might structure a managed bug bounty, but they usually fall into one of two categories: percentage-based, or fixed-fee.

In a percentage-based fee structure, we pay the platform vendor an “overhead” on each bounty paid. For example, if our fee was 50% and we awarded a $5,000 bounty, we would actually pay the vendor $7,500: $5,000 to the researcher, and $2,500 (50% of the bounty) to the vendor.

In a fixed-fee structure, we pay the vendor a fixed fee (monthly, quarterly, or yearly) regardless of bounties paid. Fixed-fee structures could be a single fee for the entire program, or a per-app fee.

We prefer fixed fees and per-app fees --  over percentage-based fees -- for a few reasons:

* Predictability: As we have previously discussed, we cannot perfectly predict how many issues we will see, so it will be hard to predict what we will pay the vendor. Fixed fees are perfectly predictable: we know exactly what we will pay.
* Incentives: Since the vendor sees a percentage, they are incentivized to assume that issues are valid, and to reward more (and higher) bounties. we will be asking the vendor to make the ultimate decision about an issue’s reward, and we want their incentives to be aligned with ours. 
* Flexibility: TTS is not a typical product company with just a single product; we have a portfolio of products and services. With a per-app structure, we are free to add or remove apps from our portfolio as we see fit. In a percentage-based fee structure, the vendor might be reluctant to add new apps that might not see the same volume of payouts.

This format is maximally advantageous to TTS: We have a fixed vendor fee, with no perverse incentives. And we have a NTE bounty pool that we can manage effectively and flexibly throughout the program. This means high budget predictability with maximal flexibility to spend that budget effectively.

And, finally, looking to the future: this structure will serve us well if/when we expand the program to more apps and services. It’s the right structure for a multi-project, multi-service organization like TTS.

## Notes on sources
In coming up with this budget, we relied on a number of sources:

* Two whitepapers on the bug bounty industry published by Bugcrowd: [The State of Bug Bounty](https://pages.bugcrowd.com/hubfs/PDFs/state-of-bug-bounty-2016.pdf) and [What’s a Bug Worth?](https://pages.bugcrowd.com/hubfs/PDFs/Whats_a_Bug_Worth.pdf). Though these papers are published by a potential vendor, they are fairly free of vendor bias: they contain data sourced from across the industry (not just the one platform), and they mesh with data we have been able to independently verify through our own experience and through that of colleagues in the security community.
* [An Empirical Study of Vulnerability Rewards Programs](http://devd.me/papers/vrp-paper.pdf), by Matthew Finifter, Devdatta Akhawe, and David Wagner of UC Berkeley.
* Market Research gathered from Bugcrowd, HackerOne, and Synack (notes on these meetings are with the rest of the procurement documents).
* An interview with [Katie Moussouris](https://en.wikipedia.org/wiki/Katie_Moussouris), an acknowledged world-wide expert on bug bounty programs. She created one of the earliest bug bounty programs at Microsoft, founded HackerOne, and was directly involved in creating Hack the Pentagon.
* Our first-hand knowledge from one of our team-member’s direct experience in bug bounty programs: Jacob Kaplan-Moss led the team that launched [Heroku’s bug bounty program](https://bugcrowd.com/heroku) and operated it for two years. Jacob later helped the Salesforce security team launch their parallel bounty (Heroku is a Salesforce business unit). Jacob has a broad network within the security community, and has discussed bug bounties with colleagues who operate them at many companies (Microsoft, Mozilla, Google, Apple, Facebook, Tesla, among others).

## Footnotes

FN1. Bugcrowd, The State of Bug Bounty (2016), 13.

FN2. The State of Bug Bounty, 16.

FN3. Some rough math on just a couple of the costs of we would face running a program completely internally:

* Workflow software: to build even some rudimentary tracking software in-house would take at least 2-3 person-months (and, likely, substantially longer). At TTS’s current billing rates, that’s around $100,000.
* Triage: we would need to hire an additional 3-4 FTEs, at at least a GS-12 level, to manage triage of incoming issues. That’s over than $200,000 per year.

So that’s on the order of $300,000, and we haven’t even accounted for the actual bounty pool yet.

FN4. The State of Bug Bounty, 14-16.

FN5. Bugcrowd, What’s a Bug Worth? (2016), 4-7. https://pages.bugcrowd.com/hubfs/PDFs/Whats_a_Bug_Worth.pdf 
