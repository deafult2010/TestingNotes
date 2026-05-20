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