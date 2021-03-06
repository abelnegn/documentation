## DA meetings: Overview
The Design Authority meets every week for a weekly update and has ad-hoc or detailed sessions for Specific topics

The meetings are open for the public to participate, though discussions are usually limited to the Board members. However, attendees will be promoted to panelists in meetings if they have designs to be reviewed or proposals for changes.

More details can be found [here](https://github.com/mojaloop/design-authority/issues/42#workspaces/da-issue-log-5cdd507422733779191866e9/board?notFullScreen=false&repos=186592307)

# DA Meeting - 5 August 2020
The topic for discussion was: https://github.com/mojaloop/project/issues/852
The "HSM Integration Approach" was touched on a few times, and the workgroup taking care of the design and implementation, tabled this for discussion at this week's DA meeting to answer a few questions arising from the last PI-Planning session where progress on this was again presented.

As we have not completed the discussion, an ad-hoc DA meeting has been arranged for this Friday with a sub-section of the DA Members. The reason for that was because there were a few specific questions we did not have time to go into detail for, which will be clarified with the individuals who raised those questions. Please drop me a note if you would like to participate in that meeting.

# DA Meeting - 29 July 2020
Issue discussed: https://github.com/mojaloop/design-authority/issues/60
Claudio noted three observations regarding usage of best practices in the Mojaloop Core codebase. One of the issues has an active issue and will be used for tracking it; the other two will be followed up as separate stories/bugs as well (standards). Claudio will provide examples and in some cases sample snippets that can be used.

Istvan and Michael discussed the usage of a unique ID for lookup requests and proposed to have a follow-up meeting the upcoming week for those interested. The current trace headers (optional) usage for traceability (APM) was brought up as a solution, which after the DA review can be proposed to the CCB (if accepted by the DA).

# DA Meeting - 22 July 2020
Canceled as a result of the PI-11 Mojaloop Convening taking place

# DA Meeting - 15 July 2020
Sam walked through some of the high-level changes being introduced with Helm v10.4.0 release and various sections from the release notes: https://github.com/mojaloop/helm/releases/tag/v10.4.0
Please have a look on the DA Topic board: https://github.com/mojaloop/design-authority/issues/56

Neal and Michael discussed the issue of shared DB, code between central-settlement and central-ledger; they’re going to continue with the current work on Continuous Gross Settlement but after the convening will get the inputs from the Perf/Arch PoC (Event sourcing / CQRS) and then align. https://github.com/mojaloop/design-authority/issues/58

# DA Meeting - 8 July 2020
The TIPS team did a presentation of the design and implementation of a **Rules Engine** satisfying their requirements of interpretation in the **Settlements Portion**, to extend fees levied as part of a transfer. The implementation allows for rules to be interpreted at any stage during a transaction. A formal presentation will be made at the convening during the week of the 20th July 2020 after which more informed decisions as to the adaption of this implementation into the Core OSS codebase can be considered as a generic approach to implementation of a rules engine.
Please see the link on the Design Authority Board here: https://github.com/mojaloop/design-authority/issues/53 for a detailed problem statement, progression on meetings in the notes and remarks and also, if completed, the subsequent decision.

# DA Meeting - 1 July 2020
As part of the "Versioning" workstream, a "zero down-time deployment proposal" PoC is being conducted and feedback from that project has been presented in the form of a problem statement, solution and a demo. The team currently working on that is Lewis Daly, Mat de Haast and Sam Kummary. The feedback was well received and as this work is ongoing, the DA will follow up with any action items to come out of the upcoming presentation for this workstream at the PI 11 Meeting.
Please see the link on the Design Authority Board here: https://github.com/mojaloop/design-authority/issues/54 for a detailed problem statement, progression on meetings in the notes and remarks and also, if completed, the subsequent decision.

# DA Meeting (Ad-Hoc) - 29 June 2020
KNEX Discussion - continued. The KNEX discussion extended into talking about the possible use of third-party tools to assist in the generation of queries to help migration efforts. This has no direct bearing on the use of KNEX itself and after exploring a bit deeper, it was decided that there was no compelling reason to continue further investigation into the use of KNEX itself, but to keep an open mind and look out for alternative solutions out there as and when they are introduced. Those libraries will be measured against the current implementation to ensure we deploy the right tools for the right purpose. This issue is now closed.
Please see the link on the Design Authority Board here: https://github.com/mojaloop/design-authority/issues/27 for a detailed problem statement, progression on meetings in the notes and remarks and also, if completed, the subsequent decision.

# DA Meeting (Ad-Hoc) - 25 June 2020
KNEX Discussion - initiated
Conversations have been started, highlighting the problem statement of difficulty in generating or creating migration scripts when database changes occur, as well as the scenario of having to perform these upgrades on a database which is online at the time.
With this context in place, continued design sessions have been scheduled to determine if KNEX would be capable of handling the above scenario and if there are alternate libraries or tools out there to replace or supplement the current implementation, which may help alleviate this difficult task.
Please see the link on the Design Authority Board here: https://github.com/mojaloop/design-authority/issues/27 for a detailed problem statement, progression on meetings in the notes and remarks and also, if completed, the subsequent decision.


# DA Meeting - 24 June 2020
Discussion today started with: Deprecation of Helm2 support - Issue #52, where it was agreed that migration to Helm3 should continue. Documentation to assist in the use of tools available to help in the migration should be provided. Find the link to this document at https://github.com/mojaloop/design-authority/issues/52

The topic of having a design approach of implementing a generic rules-based system was discussed with some specific reference first, to a requirement of having the capability to interrogate completed or in-flight transactions (either in the transfer stage or even as early in the quoting stage) in order to apply "interchange fees" for that transaction, depending on the transaction type, as interpreted by certain rules.
Various design decisions are going to be discussed around this topic as the requirement is the facility to attach rules at various points of the transaction path.
The current implementation of a Rules Engine in the TIPS project was discussed and a request to demonstrate the capabilities of that solution in order for the DA to see if it was generic anough to incorporate into the core Switch will be made in a follow-up discussion.
Please track the progression of the design decisions surrounding this issue on the board at https://github.com/mojaloop/design-authority/issues/53


# DA Meeting - 17 June 2020
Topic under discussion was: Understand and Define Mojaloop Roles for PISP, x-network, etc. use cases
The DA is happy for workstreams to go ahead and split out new APIs and Role definitions (e.g. Thirdparty API, CNP API etc.)
Please see the link on the Design Authority Board here: https://github.com/mojaloop/design-authority/issues/44 for a detailed problem statement and subsequent decision.

# DA Meeting - 10 June 2020
This week, the DA discussed: Discuss the PISP Simulator: https://github.com/mojaloop/design-authority/issues/46
The decision was made that for the time being, the PISP workstream will work on it's own branch in the sdk-scheme-adapter, and such a division/abstraction of the sdk-scheme-adapter will be revisited at a later date (see #51)

# DA Meeting - 3 June 2020
We continued the discussion started last week regarding the separate API for PISP and decided to go with option 4: maximum API Separation, with common swagger/open api files for definition and data model reuse:
Please see the link on the Design Authority Board here: https://github.com/mojaloop/design-authority/issues/47 for a detailed problem statement and subsequent decision.

# DA Meeting - 27 May 2020
Consensus relating to the issue raised and discussed some time ago, as queried by Adrian, was reached amongst the attendees. The outcome is that the Switch development will not be restrictive and prescriptive but as far as recommendation for new contributions and modules are concerned, it will be preferred if those could be done in TypeScript.

A new discussion topic was tabled: https://github.com/mojaloop/design-authority/issues/47 seeking to answer the question of whether to have a separate API for PISP, or simply extend the existing Open API. A position statement was prepared and added as a comment. All attendees were brought up to speed with the decision to be made and Issue-#47 will be the topic for the next DA meeting.

Another, PISP related topic was tabled and will be scheduled for another DA meeting: https://github.com/mojaloop/design-authority/issues/48 - Answer the question of how to manage notifications so that a PISP can be registered as an interested party for notification of the success of a transfer

