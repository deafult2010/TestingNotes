Meeting Minutes – Material Parameters & Reporting Harmonisation

Date: Not specified
Attendees: Dale, Shelley, Mamun, Wei, Dan, Tom, Sotirios, Asushi, Nishant, Fernando, Rachel, Joey, others referenced during discussion

Purpose of Meeting

To discuss:

Harmonisation of material parameter methodologies and monitoring/reporting processes
Reducing duplication of reporting and calculations
Increasing automation and objectivity in material parameter selection
Alignment between first and second line teams on governance and tooling
Key Discussion Points
1. Principle of a “Golden Source” for Reporting

Dale reiterated the strategic objective that all teams should operate from:

A single golden source of data
Common QA/UAT-approved reports and tooling
Shared dashboards and monitoring outputs

The aim is to:

Avoid maintaining duplicate reports or methodologies
Eliminate disputes over “correct” data during governance forums
Focus discussions on risks/issues rather than data reconciliation
Exceptions

Independent calculations may still be appropriate for:

Risk appetite metrics
Board/ERC reporting
Areas with heightened regulatory concern or historical issues
2. Data Harmonisation Programme

Dale summarised ongoing harmonisation work already underway, including:

Automation of PRC packs
Alignment of ERC/MMG/PRC reporting data sources
Improvements to APC, micro, and backtesting reports
Collaboration between CRD, ROD, and technology teams

Material parameters were identified as part of this broader reporting ecosystem.

3. Governance of Material Parameter Calculations

Background provided:

A few years ago it was agreed that ROD/second line should calculate material parameters
This approach was viewed favourably by regulators because:
methodology was jointly agreed
execution was controlled independently by second line

Sotirios previously led enhancements to the methodology, but:

the process still contained significant subjectivity
manual justification was repeatedly required
spreadsheets/manual intervention remained involved
4. Objective & Automated Methodology

The current proposal aims to:

Create a more objective and automated methodology
Refresh automatically on a quarterly or periodic basis
Remove repeated manual justification exercises
Provide a defendable baseline selection framework

Key design goals:

Automated threshold-based selection
Consistent methodology
Coverage of ~80% of IM
Reduction of ad hoc representative selections
5. Agreement on Harmonisation Philosophy

Shelley acknowledged:

prior lack of awareness regarding the historical harmonisation efforts
that work had previously been progressed independently

General agreement was reached that:

teams should move toward a unified methodology
duplication and “reinventing the wheel” should be avoided
relevant stakeholders should be involved earlier in future work

Dale stressed:

existing solutions/work should always be reviewed before creating new approaches
collaboration between teams should occur earlier in project cycles
6. Discussion on Reporting Platforms & Tableau

Discussion covered:

Tableau vs newer GUI tooling
Need for both flexibility and controlled production reporting

Dale explained the distinction between:

Production Tableau Reports
Locked down
QA/UAT controlled
Migrated through formal governance
Non-Production Reports
Flexible
Quickly editable
Used for urgent fixes or exploratory work

Dan noted:

flexibility is still needed for edge cases and data corrections
some current issues stem from underlying source systems rather than Tableau itself

Consensus:

underlying data quality/governance is the primary issue
tooling choice is secondary once data is properly controlled
Material Parameter Methodology Discussion
Existing vs Proposed Methodology
Existing (Sotirios / Previous Approach)
More subjective
Representative selections manually justified
Less scalable over time
Proposed Methodology

More systematic and automated.

Proposed Logic – Outright Parameters
PCC Level
IM apportioned to PCCs
Material PCCs selected if:
largest in asset class, or
contribute >0.1% of OIM

Thresholds remain adjustable.

Proposed Logic – Tenor Level
IM Allocation

Discussion on:

allocating IM using:
Open Interest (OI), or
Notional-based allocation

The proposed version currently uses notional-based allocation.

Material Tenor Selection

Process:

Rank all tenors by IM contribution
Select largest tenors cumulatively contributing to:
80% of total IM

This differs from prior approaches that focused on product-specific percentages.

Inter-Month Spread Logic

Approach:

Generate inter-month combinations between selected material tenors
Apply tighter thresholding (~50–60%) to avoid combinatorial explosion

Counts discussed:

Previous methodology: ~177 parameters
Proposed methodology: ~227 parameters
IRM2 & Spread Risk Concerns

Mamun highlighted:

Need for clearer spread parameter definitions
Current methodology ambiguity affecting spread risk analysis
Particular urgency due to recent Iran-war-related spread movements

The proposed automated methodology was viewed positively as a potential resolution.

Issues Identified

Examples raised:

UK emissions contract (~774m IM) missing from current implementation
Potential implementation bugs in some parameter selections
Need for validation of generated outputs and lists
Agreed Next Steps
Action Items
Action	Owner
Circulate methodology comparison spreadsheet and parameter lists	ROD / Team
Review generated material parameter outputs	Mamun / Shelley / Teams
Validate missing parameter examples and implementation bugs	Wei / Team
Continue discussions on threshold calibration (0.1%, 80%, etc.)	All
Align IRM2 implementation with agreed harmonised methodology	Relevant teams
Engage ROD/CRD earlier in future monitoring/report development	All teams
Continue evaluating Tableau vs future GUI solutions	Management / Tech teams
Overall Outcome

Broad agreement was reached on:

the importance of harmonisation
reducing duplication
moving toward a single automated methodology
maintaining controlled and auditable reporting processes

Further technical review is required before finalising implementation details and thresholds.



Gustav Stenfalt: He's going to send a note to the Bank of England just as courtesy to say.

Gustav Stenfalt: We don't want to keep sending you registry-specific types of contracts in transit, so it cuts down on your regulatory oversight of multiple products.

Gustav Stenfalt: Updated PGL, so as I found out yesterday, Hester has agreed that for these initial auctions, given that they're quite small, I think the one coming up on 17th of November is notional about $1.35 million and it's Corsair eligible.

Gustav Stenfalt: If in the event of the—which is why the backstop was put in place—is in the event that a buying clearing member goes into default in between the auction and the end of day when we're expecting to get paid for the credits, if that happens.

Gustav Stenfalt: Happens the next day.

Gustav Stenfalt: We're left with a bunch of credits. We can't do anything with them and no money.

Gustav Stenfalt: So that's really why the backstop was put in place, given the fact that there is now OIM volume trading in the core C and monthly contracts at CP1 and CP2.

Gustav Stenfalt: The argument is that OK, if we're left with these credits that are Corsi and compliant, we can sell futures on CP1/CP2 and then when they come to expiry, we're delivering the credits that we were leftover from the auction.

Gustav Stenfalt: So that's been agreed by Hester.

Gustav Stenfalt: So I am going to update also the PGLs to include the removal of that. I think there was some KYC initial elements there that belong in the exchange, not the clearinghouse.

Gustav Stenfalt: So I'm going to put all that in an ERC memo and send that around. So some of you may get view of that. Others of you may not if you don't need to be.

Gustav Stenfalt: And we're working on that end towards that. By the end of the week, to submit to the ERC, we'll send to.

Gustav Stenfalt: The CFTC on next Monday?

Gustav Stenfalt: So Phil, our speech here, once we've got the drafting in place, we can give AOS a shout and line them up because at the moment I've kind of worked out, we should be able to certify those by the 9th of November. But obviously AOS needs to know.

Gustav Stenfalt: That this is a fast track and then they need to know what to do with the filing.

Gustav Stenfalt: So if you could put them on standby as soon as Cornea is finished with the DP that she's already got a cut-off that EJ has suggested, we can send over there.

Gustav Stenfalt: So once we go to the ERC, come out the other side, we can file.

Gustav Stenfalt: Anybody any questions for me on that?

Abhishek Hule: Yes, Gus, quick question.

Abhishek Hule: The auctions are all going to be 100% core C eligible units, right?

Gustav Stenfalt: No, at the moment the next couple are.

Gustav Stenfalt: The next two are, but the changing to the contract allows for auctions of non-Corsa-compliant auction credits.

Abhishek Hule: OK. And we are still keeping the backstop arrangement.

Gustav Stenfalt: No. Hester's agreed that we don't need the backstop arrangement for these contracts.

Gustav Stenfalt: The initial contracts because they call CA compliant and B.

Gustav Stenfalt: They're quite small, however, when we get to the stage where they're non-Corsair compliant and they increase substantially in size.

Gustav Stenfalt: The discussion will be whether we introduce the backstop back again for those or whether Mamun is comfortable being able to find an off-ramp either through OTC contracts that exist already or not.

Gustav Stenfalt: So that's a separate discussion going on. So for the time being, the PGLs will not be a backstop has to be in place and then going forward, I think EJ's talking about—I think there's 100,000 credits equals 1.35 million for the next two auctions.

Gustav Stenfalt: Next two auctions, there is talk of auctions being as high as a million credits, which would be thirteen and a half $1,000,000. And I think at that point when we get the early sight of that.

Gustav Stenfalt: Memory. We'll have a discussion with Gordon.

Gustav Stenfalt: And then say, OK, is there scope to be able to trade some OTC contracts to get out of this or do we reintroduce the backstop? And that's a takeaway for them?

Abhishek Hule: OK.

Abhishek Hule: So the first two right now are 100% cores here, no backstop.

Gustav Stenfalt: That's right.

Gustav Stenfalt: Yeah. And then the third one.

Gustav Stenfalt: I don't know, but obviously in time, you know, we're six months, nine months down the road, whatever it might be, that there will be non-Corsair-compliant credits in potentially a bit of size.

Gustav Stenfalt: And then the question would have to be asked and answered about what we do, you know, is the OTC offering good enough outlet to get rid of the residual risk of having those credits or do we have to go back to the backstop idea, but that's further down the road.

Abhishek Hule: OK.

Abhishek Hule: Thanks. Thanks a lot.

Gustav Stenfalt: Alright.

Gustav Stenfalt: Any other questions for me on?

Gustav Stenfalt: That, I'd imagine, Eva, you'll get wind of the ARC papers and ERC papers and probably would have to send something to the FSA. Don't know about the updated contract spec, but—

Cornelia Lowe: Yeah. No, it will.

Cornelia Lowe: I mean, sorry to step in there as well. Just for the exchange side, we're going to need changes to the exchange, to the contract rules and procedures.
