# tomiDAO specifications: DAO Requirements for tDNS release

## Contents

Contents.......................................0

Introduction...................................4

    Challenges....................................4
    The structures................................4
    Pioneer control...............................5
    Representation of the Netizens................5
    Limitations of token-based voting.............5
    Goals.........................................5
    Success Metrics (2024)........................5
    Assumptions and dependencies..................6
    Dependencies.................................6
    User Stories...................................6
    Requirements...................................7
    UX Mocks.......................................7
    Questions......................................7
    Out of Scope...................................7
    
Top-level DAO	8

    Strategy	10
    Finance and budgeting	12
    
        Main tomiDAO	13
        Current procedure	13
        User stories	13
        Requirements: Immediate functionality	13
        UX mocks	14
        Questions	14
        Out of scope	14
    Stewardship and council elections	15
        Council Elections Procedure	16
        Requirements	16
        Responsibilities of the first DAO Stewardship council	17
        Approval of the council	18
        Application	18
        Voting	19
        Establishment	19
    Calls for proposals (Grants Program)	20
        Problem definition	20
        Participation compensation	21
        Proposal propositions: Pre-proposal phase	22
        Discussions and proposal improvement	22
        Collaboration compensation	23
        Team building for proposal execution	23
        Proposal submission	23
        Ranked voting and consensus for proposals	24
    Metagovernance: oversight and governance changes	24
    The tomiDAO approach to identity and reputation	24
        The challenge of identity: rationale for a reputation system	25
        Separation of reputation issuance and interpretation	25
        Decentralization of reputation	28
        Negative reputation	30
        Reputation system flow / architecture	31
    Credential issuance (NFT and VC)	31
        Goals	31
        Success Metrics	31
        Assumptions and Dependencies	32
        User Stories	32
        Requirements	33
            The DAO top-level credentialing guild	33
                Credential issuing for top-level credentials:	33
                Compensation for the credentialing guild:	34
            Creation of a guild	34
            Certificate definition for guilds	34
            Negs: Certificates of bad reputation	36
            Certificate issuance for guilds	38
            Automatic credential issuance	38
            DAO execution credentials	38
            Credential pick-up hub	39
        Reputation Interpretation Engine	41
            Issuer Reputation	42
            tomi Reputation Score	43
        Warrants Authorities	44
            tomi Warrants Authority	45
            Warrants Authority Standards	45
            Warrants Expiration	45
        UX Mocks	45
        Questions	45
        Out of scope	45
    Credential recognition	46
    Membership and recruitment	46


tDNS DAO	46

    Goals	46
    User Stories	47
    Technical decisions	47
    Initial stewardship	48
    Budgeting and finance (within tDNS-DAO)	48
        Income sources: tDNS DAO	48
        Annual budgeting	49
        Payment for DAO participation	49
        Financial council	49
        Monthly Retainer smart contract	49
        Revenue streams	49
    Domain Management	49
        Registry-Registrar relations	49
        Domain release and pricing	52
        Branding and art	52
        Domain registry management and privacy	52
    Content moderation and community guidelines	52
            Goals	52
            Success Metrics	52
            Assumptions and dependencies	53
            User Stories	53
            Requirements	53
            UX Mocks	53
            Questions	53
            Out of Scope	54
            Design considerations and vulnerabilities for content moderation:	54
        Content guidelines	55
        Default URL banning and default moderation policy	55
            Design considerations and vulnerabilities for content moderation:	55
            Initial Misidentification Process for Content Moderation by the DAO	56
            Appeals process	57
        Standards and pricing for third-party moderation plug-ins	59
    Dispute resolution	59
    
Out of Scope: Marketing DAO (Future)	59

Out of Scope: DevelopmentDAO (Future)	60

# Introduction

The tomiDAO has two main operational requirements to date. One is to manage the budget that has been allocated to the DAO, and the second is to manage the DNS and content moderation functions such that tomi can accomplish its goal of creating an alternative WWW governed by the people who use it.

Currently, the tomiDAO budget is governed by the initial investors, the Pioneers. However, this is not a long-term sustainable structure because these individuals cannot take the time to govern an entire WWW, nor do the tomi founders intend for the tomiNet to become a plutocracy or oligarchy. In order to maintain the interests of the Pioneers and their function as an oversight group for tomiNet, this proposal seeks to separate the Pioneer-managed budget from the ongoing operational budget of the DAO, and to create all of the sub-functionalities required for the management of the tDNS. 

### Challenges

To date, much of DAO tooling has focused on how to co-manage a budget, and even that has been limited.
* Centralized control of strategy setting and annual/quarterly budget.
* Competitive winner-takes all compensation.
* Lack of information on DAO participant qualifications (reliance on political campaigning).
* Lack of organizational history.
* Accountability gap: Once DAO funds are released, there is little accountability or tracking of what has been delivered.
* Expectation of a tremendous amount of “free work” to enter DAOs, participate in discussions, make proposals, campaign, etc.
* Competitive rather than cooperative rewards systems.

### The Structures

Typically, a centralized foundation or core team has been making the decisions about the strategy of how to spend the budget and how much of the DAO treasury should be spent. This typifies the problems of today’s democracies: while the citizens do get to vote on a list of candidates or on a referendum, the candidates are chosen and the referendum text is written by centralized entities in a corrupt process that excludes the citizens. SImilarly, in the DAO, while the token holders get to vote yes or no on proposals, the process by which the proposals get to the ballot is complicated and politicized.

Another problem in DAOs is that although 

### Pioneer control 

The current tomiDAO provides a secure voting system for the Pioneer holders

### Representation of the Netizens

### Limitations of token-based voting

Note to write in the introduction the failures of token-based voting and the general approach tomi is taking to democracy and democratic process.

### Goals

The tomiDAO has the following overarching goals:
* Utilize the budget of the tomiDAO for maintaining the tomiNet
* Become self-sustaining financially by 2027
* Create structures for self-governance of the tomi Domain Management System (tDNS) that allow it to be fully governed by the users (tomiZens)
* Ultimately take over all of the management of tomi, including the development and marketing of the tomiNet
* Allow the separation of the tomi corporate interests from the public good interests of maintaining an alternative WWW

### Success Metrics (2024)
* Functioning DAO with at least 60 active members
* Stewardship team of 5-7 core people being compensated at competitive rates for their work on the DAO
* Functioning milestone system for proposals
* 2 funding rounds completed for specific “calls to proposal” for the DAO
* tDNS management
* Basic moderation mechanism in place
* Ranked voting mechanism integrated with tomiWallet for weighted voting
* Voting system that does not require high gas fees (up to $1/vote maximum)
* Integration with Guild.xyz for committees and reputation system
* Operational Verifiable Credential (VC) certifying DAO for implementation of reputation
* Strategy setting event set for 2025

### Assumptions and dependencies
1. All DAOs to date suffer from voter fatigue because voting is not the primary means that organizations naturally make decisions. In order to have a proper decision-making and management process, DAOs need to implement normative and natural management processes, and create professional governance teams.
2. Many DAOs run out of money without accomplishing their goals because of the ability for people to drain money out of the DAO with no accountability, and conflicts of interest between those who invested and those who want to use the money for their own purposes.
3. All participants in the tomi ecosystem (tomiZens) should have some level of influence in the decisions that affect them. Decision-making power is provided based on people’s participation and reputation in the tomi ecosystem. 
4. Voting systems are inadequate for the complexity of issues that tomiDAO, and particularly tDNS, are facing today. tomi needs to establish proper process for each of the different needs of the DAO decision-making team.
5. A “normative” decision making process for organizations includes:
   
    a. Strategy setting and prioritization (annual/quarterly)
   
    b. Budgeting allocation based on strategy and prioritization
   
    c. Problem / Opportunity identification
   
    d. Problem definition (and success metrics)
   
    e. Bids / proposals that address the problem, or bounties that allow people to do work and have the work accepted.
   
    f. Choice (possibly by voting) of the best proposal(s)
   
    g. Execution of the proposals, and reporting to the DAO of progress.
   
    h. Oversight and milestone review of those who are conducting the work, or review of bounty execution (automated or human).
   
    i. Reputation/validation issuance for those who execute (and those who fail to execute) the proposals.
   
    j. Dispute resolution in case of disputes.
   
7. Much more power lies in the creation of the proposals than the voting. 
  
#### Dependencies

* Self-sovereign identity wallet creation
* Having a large enough community of DAO participants for the committees and votes.
* Time of the development team to work in collaboration with the DAO committees

### User Stories

User stories will be based on each section of the DAO, detailed below.

### Requirements 

Detailed in each section below.

### UX Mocks

To be worked on together with the R&D team.

### Questions

* What is the minimum functionality required for the tDNS launch?
* How is tomi dealing with security, spam, and DDOS type attacks?
* What are the most immediate security and attack vectors we need to manage?
* What is the right balance of AI vs human intervention in content moderation (censorship)?
  
### Out of Scope

* DAO for marketing and R&D

# Top-level DAO

Overview

The tomi DAO has multiple functionalities. The top-level DAO is responsible for top-level requirements across all sub-DAOs. The main DAO provides overall strategy setting, calls for proposals, finance and budgeting, membership, and credential issuance.

** INSERT IMAGE HERE **

## Strategy
The tomiDAO Stewards will hold strategy meetings twice per year: June and January. The January strategy meeting will be in-person and funded by the DAO. Depending on the funding from the DAO, the tomiDAO stewards may opt to sponsor accommodations or travel. Sponsorship of participants should be used primarily in order to balance the representation of the different interest groups in the tomi ecosystem.

The strategy meetings will include representative participants from the following groups: 

* tomi team
* tomiDAO (stewards, proposal winners, etc.)
* tomi Pioneers
* tomi token holders
* tomi community members, including tomiArmy and tDNS domain holders 
* projects under the tomi umbrella (tomiChain, Gems, etc.)

** INSERT IMAGE HERE **


Each of the above entities will have decision-making power in the strategy discussions. Rather than individuals having power, each of the entities above will have equal decision-making power in prioritizing the strategy if there is a vote or proposal that needs to be passed by consensus. Each of the 6 entities can have their own internal decision-making process which is not dictated by the DAO. For example, the tomi team may be governed by a CEO or executive team, whereas the tomi Pioneers may use voting to determine their stand or to elect a representative.

Strategy discussions should start online and then be completed in an in-person format whenever possible.

The suggested process for strategy discussions: 

** INSERT IMAGE HERE **

## Finance and budgeting

As of May 15, 2023, the finances will be split between the main DAO and the tDNS DAO:
* The tDNS DAO will receive all funding based on sale of DNS domain names.
* The main tomiDAO will receive all other funding.

## Main tomiDAO

The current tomiDAO has an initial budget set out by the Whitepaper and based on contributions towards the DAO functioning ongoingly. The following sources of income are identified for the top-level DAO:
* Initial grant money from the tomi Launch
* Airdrops (including Pepe coins)
* Partnerships (such as DOP partnership)
* Content partnerships and memberships (Gems)
* Nodes and hardware (future)

## Current procedure

For the functionality of the DAO, in 2023, funds were allocated to specific groups to execute on the needs of the DAO. This structure works for trusted suppliers, and reduces the overhead for voting on the DAO. The following major budget allocations were made:

* $TOMI 100,000 to the tomiArmy, which is using the funds for marketing efforts, led by Superbullish, and recently shared responsibility among several stewards. The army does not provide transparent reporting to the DAO. The majority of the funds continue to be held in $TOMI and allocated in the same. As of this writing, the activities of the tomiArmy are within a dedicated portal of the tomiArmy.
* $TOMI 16,000 to walt.id for creation of the SSI wallet specifications. The walt.id team immediately converted the money to USDT. Walt.id continues to report regularly to the tomi team, including Camel and DAOowl. 
* $TOMI 30,000 to the tomiDAO specifications team, managed with a multisig with 3 signatories from the tomi team (Camel, Owl, and NowhereMan). The multisig is transparent and a team led by Grace Rachmany has been providing regular reports and updates, and Owl has been maintaining a payments table of all payments.

## User stories
* Pioneer
* Steward
* Proposer to DAO

## Requirements: Immediate functionality 
Over the first 9 months of functionality, the following missing functions have disabled the DAO from providing the intended basic functionality 
* Ability to convert treasury into other tokens. ($PEPE to $TOMI, for example)
* Ability to get rid of sh*tcoins and NFTs dropped to the wallet address.
* Ability to award money through milestones instead of all in one tranche. (Requires stewards/representatives to approve milestones.)
* Possibility to pay for work in tokens other than $TOMI tokens.
* Full reporting on all income sources to the DAO, and auto-deposit of money from tDNS and token issuance.
* Notification to DAO stewards of incoming funding.
* Removal of the DAO forum (Inadequate design)
* Nice to have: Improvements to the functionality of the proposal submission (compatibility with Markdown language or HTML to preserve format, support for budget tables)

Additional requirements are described in the sections below:
* Basic stewardship
* Calls for proposals
* Metagovernance: Ability to change governance
* Credential issuance (NFT and VC)
* Membership and recruitment

## UX mocks

## Questions
* What are the main goals and objectives of the tomiDAO for 2024?
* How much (maximum percentage) of the DAO funds should be allocated for disbursal each year/quarter?
* To accomplish these goals, what are the structures we need to put in place?
* What is the right relationship between the team, the community, and the DAO?

## Out of scope
* Self-Sovereign Identity. The self-sovereign identity wallet is part of the tomi roadmap and is being developed as a separate project from the DAO. The DAO will leverage the SSI Wallet / tomiWallet capabilities in the reputation system described in this document.
* Evolving the DAO from a Pioneer-only driven DAO to a community-driven DAO is out of scope for 2023 and at least the first half of 2024. The intention is to make the transition in collaboration with the existing Pioneers.
* Discussion forums built into the DAO. The current discussion forum is inadequate, but creating discussion forums is now a major focus of several organizations such as FactoryDAO and RnDAO, who are looking into AI and LLMs for integration of DAO discussions and DAO decisions. During 2024 it will be worth further investigation by the DAO stewards.

## Stewardship and council elections
Many of the functionalities required by the tomiDAO over time will require stewards and/or committees either for the purpose of temporary management of a new functionality, or as part of the needs of the DAO. For example, budgetary oversight might always be done by a committee, but if the DAO decides on an automated jury-based content management scheme, it might require a temporary group of stewards for the first 6 months until the automation is fully functioning and tested to work.
Note: The platform Guild.xyz can be used to maintain the groups. Using guild.xyz will ease the ability of the tomiDAO to manage the groups and sub-groups operating as councils. Stewardship elections could be done through something like tally or jokerace so that tomi does not need to develop proprietary technology for everything.

** INSERT IMAGE HERE **

The following table describes the general election process for the creation of a stewardship council. Details on each step are described in the following sections of this document.

### Requirements

The requirements for the council can be created by any of the following entities:
* tomi team or DAO Owl 
* Stewards or councils of the DAO
* Proposal by the community or Pioneer

Requirements must include:
* Purpose of the council
* Number of people to be elected
* Qualifications desired
* Time frame both for the election terms and how long the council will exist (temporary or long-term)
* Expected time commitment for council members
* Outcomes the council is responsible for (measures of success)
* Reporting needs: how the council will report to the community
* Authorities and responsibilities for the council
* Budget, payment to council members if relevant, wallet for storing the funds, and oversight/milestone approval process
* Type of reputation, credential, and ratings that will be awarded for council participation

If a budget is required for the council, the requirements must be ratified by the DAO with the budget which is requested, as per the current requirements for budget approval. (10% quorum of Pioneers with 51% positive.) The budget should be put in a multisig wallet managed by the financial council committee of the DAO, or put in the Monthly Retainer smart contract that automatically will pay the winners of the council elections. 

Simultaneously with the creation of the requirements for the applicants, the team responsible for elections will publish the requirements necessary for voting in the election. Depending on they type of council needed, the voters should represent the $TOMI community, DAO participants, Pioneers, users of the tomiNet system, and potentially the partner projects.

#### Responsibilities of the first DAO Stewardship council

The first DAO stewardship council will be responsible for the implementation of the specifications in this document, including updates and changes as needed. Responsibilities:
* Updating of the DAO specifications
* Communication with the R&D and product teams doing the development
* Calls for proposals and budgeting for the development of the DAO (anything not done by the tomi core team)
* Strategy meetings including the community to determine annual and quarterly strategy for the DAO
* Creation of additional stewardship councils as needed (calls for elections and responsibility definitions)
* Oversight of the content moderation capabilities of the DAO
* Coordination among the teams that operate the DAO
* Working with all DAO and community members to set and monitor KPIs, including budgeting for people and elections for people who are responsible for specific KPIs or activities of the DAO
* Ongoing communication with the community as well as outward facing communications and transparency into the DAO. This includes creating a website, wiki or other online tool where all of the decisions and information about the DAO and DAO decisions can be easily filed and found.

The council will work with the tomi team and the tomi community to get feedback on how these DAO structures are working, and to improve on them based on the actual deployment. If budgeted by the DAO, the stewards may have oversight on an external R&D team that is developing the DAO alongside the tomi team.

#### Approval of the council
Approval of any type of council, team, or guild needs to be done at two levels: budgeting and responsibilities. The budget needs to be approved by the people giving the budget. If the council is self-budgeting, this step can be skipped. The responsibilities need to be approved by those currently holding that responsibility, those who need to honor their decisions, and potentially the community being impacted by the decisions of that council or guild. 

The approval of responsibilities and budget may be two separate processes or one process, depending on who needs to approve each element of the proposal.

* Budget: The budget for a new council or committee must be approved through the normal budgeting mechanism for that entity. For example, if the tomi Team wanted to budget a new committee, they would do that through their management team. If the tomiDAO is required to approve the budget, the Pioneers would have to approve the allocation.

* Responsibilities: The authority and responsibilities of the council need to be approved or ratified by the individuals or entities that currently hold that authority, or those who will need to honor the decision. For example, if a council were to be proposed to take on marketing responsibilities, the tomi internal marketing team and the tomiArmy would need to approve the delegation of that authority to the new council. If the DAO proposed a council to oversee finances, the approval would need to come from the DAO Stewards, the tomi team finance department, and the tomi Pioneers, because those three authorities are responsible for managing finances today. Optionally, all $TOMI token holders could be given a vote in that as well, since they are impacted (but it is not their responsibility.)

### Application 

For Stewardship and council elections, the initiators of the call will release an application form. We would ideally like to formulate something similar to the recent SNET Supervisory Council elections on the Swae platform. The DAO will allocate funds to determine the best existing platform. The questions will be discussed among the community and will be tailored for the tomi mission and vision. 

The applications and call for applications for the initial Steward council will be open for 30 days, but other councils may determine other application deadlines.

Candidates will be able to campaign on the tomi Discord and Telegram channels. The team initiating the election will provide 10-minute interviews for all candidates to present themselves to the community and field questions in a live video format. Those who do not want to use video can use voice-only for pseudonymous participation. Pseudonymous participants must hold the tomiPay wallet with SSI capabilities so that they can be identified and accumulate reputation.

During the discussion period, if any of the candidates do not meet the minimum requirements, or if they have a history of corruption or rugging behaviors, the Stewardship council may remove them from the list of candidates.   

### Voting

Voting for the initial stewardship council will take place on the Jokerace.xyz or similar platform that allows credentialed voting. The tomiDAO development team will develop the means for people who are qualified to vote to receive their voting tokens. Voting tokens are useful only for the one-time vote (and new tokens are issued for every vote). 

The ranked voting recommendation for the candidates will be weighted for different levels of community participation:
* $TOMI holders: 100 votes
* Pioneers: 500 votes
* TomiArmy members with certification of participation: 200 votes (List to be provided by TomiArmy Stewards)
* Active Discord and community members with proof of participation: 200 votes
* DAO experts based on list from DAO Owl: 200 votes

Tokens are not cumulative. Each wallet can choose its top level of participation. 

For any other councils, the initiators of the call can determine other voting configurations.

The voters can distribute their tokens among the candidates as they see fit.

Voting will be open for 10 days. 


### Establishment 

The call for council will also include the compensation and establishment of the council. Following is relevant to the initial tomiDAO Stewardship council
6 stewards will be elected to the council

* Council decisions will be by unanimous agreement / consent
* The council will elect its own full-time council chair. The council chair is expected to work full time on the implementation of this document
* The additional 5 seats will be expected to work 10-15 hours/week on different aspects of the DAO
* Salary for the full-time head of the Stewardship Council, full-time 45 hours/week: $7000/ month
* Salary for additional seats (10-15 hours/week): $2300
* Payment will be in $TOMI tokens and will be updated according to dollar rates for the first year. 
* The Stewardship will be for 18 months, at which time a new election will be run. No more than 2 of the existing stewards can be re-elected (the top 2 that are voted for).
* Within the first month of their stewardship, the team will create a budget to propose to the DAO. Budgeted funds will be placed in a multisig wallet managed by the Stewards with a 3/6 signature release of funds and full transparency into where the funds are going. 
* The stewards will be paid through the Monthly Retainer Smart Contract
* If any of the stewards is not performing their duties, they can be removed by 5 of 5 of the remaining stewards.


## Calls for proposals (Grants Program)

On a quarterly basis, the stewards will allocate funds for the top priorities of the DAOs, based on the priorities set in the strategy sessions and by the financial stewards who determine the appropriate spending levels.

The tomiDAO intends to create a grants program that is primarily designed to expand the reach and long-term sustainability of the tomiNet. 

For 2024, this document sets out the main strategic goals of the tomiDAO: 
* Maintaining and improving the functionality of the Credential Issuance tools, including the SSI wallet.
* Supporting tomi and the $TOMI price
* Supporting websites that are established in the tomiDAO ecosystem. 
* Supporting third-party essential tooling for tomiNet (for example: search engines, SSH tools, content filters, social networks).
* Increasing participation in the DAO and stewardship.
* DAO improvement (metagovernance).

The DAO team should aim to set out calls for proposals along those lines.

## Problem definition
The report from the Strategy meetings will define the main areas where the DAO wishes to focus. The DAO stewards will then be tasked with creating problem definitions for each of the strategy areas. Depending on their workload, the DAO stewards may decide to write the specifications themselves, appoint consultants, or hold elections for a short-term committee to set any number of the problem definition statements.

ANTI CORRUPTION CLAUSE: People involved in creating the problem definition and their associated organizations may not later submit a proposal to the DAO for that particular problem. A number of DAOs (and companies) have suffered from poor proposals because the person writing the requirements is the same as the person applying for funding to meet those requirements. 

Problem definitions for strategic objectives and large funding initiatives should include:
* General description or overview of the problem.
* Approximate timeline for addressing the issue.
* Conditions of satisfaction or Key Performance Indicators.
* Milestones for approval.
* Consequences if the conditions or milestones are not met. Generally, the DAO should strive to always pay for work performed, but a contract may be stopped if the conditions or milestones are not met.
* Guild, team, or individual who will assess the work, provide Credentials of the performance, and provide feedback to the performers of the work. This also includes the compensation for the assessment they are doing.
* Budget available, priority or percentage of budget available. 
* Number of projects that can be accepted.
* Eligibility requirements for proposal submission.
* Decision-making method (voting or other).
* Time frame for submissions, discussions, proposal collaboration, and voting or voting alternative.
* Collaboration rewards.
* Eligibility for voting.
* Any differences between this and standard participation rewards/compensation in the DAO.
* Format and adjustments to the Proposal Template designed to help teams assess the proposals.

## Participation compensation
One of the drawbacks of most DAOs is that teams need to invest a tremendous amount of time creating and discussing proposals and campaigning for their proposals. All of this work is expected to be done for free as part of the way the DAO functions. This disincentivizes the best teams from getting involved, because the best people are usually too busy to spend their time campaigning. It also creates a system that is heavily weighted towards teams that are good at marketing and campaigning rather than teams that are great at execution. 

tomiDAO believes that people should be financially compensated for their contributions, and that proper compensation encourages each person to collaborate in the way that is best for them. In fact, it may be that some people are excellent at writing proposals but not at execution. For example, this specifications document was not written by a smart contract programmer. All of the smart contracts for execution of this specification need to be written by a team that specializes in software development, not one that specializes in specification writing. It should be possible for people who are creative to submit proposals that can be executed by others. Furthermore, contributions are made along the way by the community by commenting on a proposal. 

The budget for participation compensation should be 10%-15% of the overall budget for the project. While this may seem like a lot, it’s aligned with the costs of market research and procurement for regular companies. 

The Participation Compensation Fund will be allocated on a week-by-week basis over the course of the proposal submission and discussion phases, up until the date of final submission of the shortlist/final proposals. 

Each week, anyone who has been involved in the proposal making process over the previous 90 days will be dropped 100 Coordinape Tokens that they can allocate to whoever they think deserves compensation for their participation this week. The compensation phase will be for 48 hours at the end of each week. At the close of each round, the funds will be allocated proportionally based on the Coordinape votes that week. This system allows the community to decide what is valuable to them.

## Proposal propositions: Pre-proposal phase

The Grants program will issue a generalized proposal template that can be adopted for any proposal in the grants program. Individuals, guilds and teams that want to apply for the grants program should submit pre-proposals which will eventually make it into the final round.

During the pre-proposal phase, guilds, teams, and individuals can submit proposals. A proposal can be as elaborate as a full proposal based on the proposal submission template, or as simple as a few sentences outlining an idea, or even an offer to join an existing team. 

The DAO will establish a submission form that allows the community to find all proposals in one place. It will be up to the DAO stewards to determine whether this will be a Git repository, shared online docs (Google Docs), Snapshot or other DAO tooling, Discourse, or other forum tool. The tomiDAO will ensure that the proposal discussion is properly managed and archived after each vote for transparency and auditability. 

The initial proposal phase is designed to collect all viable ideas and teams that want to address the issue. Submitters of proposals can retire or withdraw proposals, or indicate that they have joined a collaboration with another team. 

## Discussions and proposal improvement

During the discussions and proposal improvement phase, the different proposals can be reviewed against one another and improved. Proposals that are similar can be merged, or teams can provide explanations of why they would not collaborate. It is true that teams may “steal” the ideas of other teams--but this is part of the ethos of the open source community. The tomiNet is designed as a public good to serve everyone. As such, a healthy combination of collaboration and cooperation is required. The community can also be the judges of the collaborative energy. If a team is seen to be stealing others’ ideas, the community is the judge of which team or individual gets compensated for their time participating in this phase (as described in Collaboration compensation). The community can also appeal to the stewards to eliminate a proposal, from qualifying, or they can simply not vote for the proposal if they feel there is a team acting in bad faith.

During this phase, the community can use upvotes to indicate the proposals that are the most popular, helping to form a shortlist of proposals with the best chances of success.

## Collaboration compensation

During the proposal proposition phase, the community can indicate which proposals are similar to one another, and encourage groups to join forces. Furthermore, development teams and product management teams can take advantage of this time to find one another. The DAO will provide a system for teams to signify that they have decided to collaborate rather than compete, and describe the areas where the collaboration provides an improved proposal. Teams can be rewarded by the community for joining forces. The DAO, tomi team, and stewards will keep their eyes open for such collaborations and give special NFTs and publicity to those who are leveraging the opportunity to collaborate.
No collaborations will be forced. People are always allowed to work with the people they want to.


## Team building for proposal execution

Before the final submission of proposals, the different teams submitting proposals will have an opportunity to collaborate with others. The DAO should encourage such collaborations through incentivization of teams who merge their proposals. Similarly the DAO should create ways that teams can acquire missing skillsets from among those who have submitted the proposals. The writers of this specification (the one you are reading now), for example, do not have programing skills. Similarly, the best proposal may not come from someone with the best ideas and writing skills–not necessarily the best development team. 

To date, no DAOs have implemented any processes that would optimize for the best teams. Currently, this phase is envisioned as something the stewards and community would do manually. tomiDAO intends to run trials and experiments in order to fulfill this need. While we don’t yet have a structure that could be explicitly described in this document, it is clear that lack of collaboration has been a huge source of loss of value in the community, and we did not want to step over the need even if we don’t yet have a specific process in mind.

## Proposal submission

The Grants program will issue a generalized proposal template that can be adopted for any proposal in the grants program. The basic template will include the following sections. For each grant problem definition, a customized template can be created, or the team can simply use the following format.

1. Title
2. Summary /TLDR
3. Description
4. Team and Credentials
5. Qualifications Based on Problem Definition Criteria
6. Milestones
7. Budget 
8. Revenue and Revenue Share (if relevant)
9. Requests from tomi Core Team
10. Requests from the DAO
11. Other Specific Requests
12. Outcomes / ROI / Alignment with Conditions of Satisfaction
13. Milestones / Timeline
14. Risks / WCPGW 
15. Out of Scope

### Ranked voting and consensus for proposals   

## Metagovernance: oversight and governance changes

DAO Owl and the DAO stewards will have monthly meetings to discuss the DAO functionality. On a quarterly or bi-annual basis, the DAO stewards and DAO Owl will submit governance change proposals to the tomi team or the DAO. This is under the responsibility of the Stewards to govern the DAO.

By the end of 2024, the DAO Stewards will propose improvements to the stewardship structure, so that the DAO can further decentralize all of the DAO functions described in this document. The stewards will also assess and comment on proposals from each of the sub-DAOs for improvement of their own meta-governance structures.

The stewards will also have responsibility for collecting input from the community on the DAO, and for managing the functioning of the DAO. As such, the stewards will be able to make proposals for funding for functions such as dispute resolution, proposal assessment, etc.

## The tomiDAO approach to identity and reputation

The tomiDAO takes the approach that identity is about the reputation someone carries vis-a-vis the DAO itself. The DAO is a governance entity that grants certain rights to its members: the right to vote, the right to submit proposals and receive funding for projects, the right to participate in stewardship councils, and the right to discuss and critique the proposals and candidates that are running in the DAO. For any of these rights to be valid, it’s necessary to identify an individual based on past behavior.

### The challenge of identity: rationale for a reputation system
While the initial DAO is based on NFT-gated voting by the Pioneers, the medium to long-term goal is to distribute power among all of the relevant tomiZens. For different types of decisions, different membership levels may be relevant. 

For example:
* Pioneers and token holders have an interest in the long-term value of the $TOMI token.
* tDNS NFT holders have an interest in the business case and technical viability of building websites on tomNet
* Website creators have an interest in the moderation and safety policies of the tDNS
* Buidlers have an interest in the fairness of the proposal process of the DAO
* All users of tomiNet have an interest in the success of projects that are funded by the DAO and the accountability of those receiving funds

While it’s not important to know the “real name” of someone, it is important to know that someone is qualified to carry out a proposal when they request money, that someone is a long-time contributor or expert when they run for a position of responsibility, etc. Token-based voting has its place in decisions about the money that is controlled by the token-holders, but it falls short in several ways which have been well-documented in Web3. For that reason, tomi is pioneering a self-sovereign identity based approach. 

For a practical review of self-sovereign identity, please see [The Ultimate Guide to Self Sovereign Identity] (https://www.identity.com/self-sovereign-identity/). While much of the Web3 community remains dependent on NFT and token-based identity, there is clear movement towards technologies that offer privacy and selective disclosure. tomi will be using a wallet with SSI technology to preserve people’s rights over their personal data. This wallet allows the tomiNet to develop a sophisticated general-purpose reputation system that will serve the tomiDAO as well as all of the tomi ecosystem and the tomiZens as a whole.

### Separation of reputation issuance and interpretation

Recognizing the complexity of reputation means that there will never be one reputation measure or one “reputation token” that can provide an adequate reputation score. Reputation includes understanding different levels and types of contribution as well as different competencies. Similarly, reputation issuance and reputation acceptance are two separate mechanisms, often practiced by separate entities. For example, a university issues degrees, but the degrees are accepted by employers or clients. Each employer can interpret a degree differently, depending on their assessment of the quality of the issuing university. 

Within Web3, separation of issuance and interpretation is demonstrated by the Gitcoin Passport, which provides an affirmation of someone’s “personhood” based on connecting to multiple other profiles: Twitter, Discord, LinkedIn, Google, etc., as well as their Ethereum wallet. Based on the amount of activity of that identity, GitCoin provides a single score which represents the likelihood that this is a real human individual, not a dummy wallet or bot. For quadratic funding, that’s an adequate measure. 

In all of these systems, one of the main shortcomings is how to manage undesirable behavior in DAOs. tomi has taken into consideration the problems of people who win DAO contracts and do not deliver, or who apply for multiple DAO contracts for the same work, getting paid multiple times for the same work. Similarly, a DAO might want to identify people who make a lot of noise in the community channels but don’t really contribute any useful information or useful work.

** INSERT IMAGE HERE **

Following these models and considerations, tomi is creating a distributed identity and reputation tracking system  system that has several components:

* tomi Wallet: The tomi wallet will support Verifiable Credentials (VCs) in addition to blockchain credentials (NFTs and tokens).
* Standards setting and modification: Overarching responsibility for making sure that the standards and interoperability protocols are maintained and published for all of the components of the identity, certification, registries, guilds and reputation interpretation engines. 
* Guild / team implementation: Groups of certificate issuers will be teams of people who issue certificates. The initial release of the reputation engine intends to use guild.xyz as the team-management component. On top of that structure, the tomi wallet and portal will provide interfaces for setting up and managing a guild that can be recognized by the system. 
* Certificate issuance: Verifiable Credentials can be issued by any group that wants to issue them. tomiDAO is planning to use guild.xyz for the initial system that will allow people to prove they are part of a team, and those teams/guilds will be able to issue certificates. Initially, tomiDAO will be the only official certificate issuer, but the protocol will allow anyone to sign on and issue credentials that can be recognized by the tomi Wallet.
* Certificate collection: The collection portal allows people to log in with their wallets and collect the certificates they have earned.
* Issuer registry: tomiDAO will publish a list of the guilds and certificates that tomi considers legitimate. Others can also publish their own registries, so that the reputation system is fully decentralized. Anyone interpreting a certificate can choose the Issuer Registry that they consider most reliable at assessing the validity of the guilds.
* Reputation interpretation engine: tomi will create its own reputation score for the purposes of the DAO. Over time, tomi will create a reputation interpretation engine where other entities can determine how they want to interpret the different certificates that are issued.
* Warrants authority: Centralized entity (similar to a credit rating agency) that will collect negative reports on community participants. This is expected to happen at a later stage (1-2 years following the certificate issuance system) following smaller experiments and community discussions. While tomi sees this as an essential part of reputation, the potential for harm is great, so it’s important to proceed with caution and try a number of pilot projects before implementation over the whole DAO. Similar to the other components, tomi intends to publish interoperability standards so that third parties can also create warrants authorities and people can choose the authorities that they find most relevant or reliable.

### Decentralization of reputation

The reputation system components allow for a fully decentralized reputation, allowing anyone to issue credentials, anyone to verify the issuers, and anyone to select the certificates they want to trust. The certificates are intended for issuance based on actual first-hand participation but could be used in other ways as well.
The following shows the system flow for certificates.

** INSERT IMAGE HERE **

1. A person performs work and the guild responsible for oversight of that work issues a credential to the tomi Credentials Portal. The guild may keep a database of certificates issued, or they may discard all data once the certificate is issued.
2. The person logs in with their wallet to the Credentials Portal. The Portal displays all credentials that have been issued and not yet collected for that wallet address / login.
3. The person can collect or reject the issued credentials. If they accept their credential, it is sent to their wallet and deleted from the Portal. If they reject a credential, it is deleted forever from the Portal. The Portal does not store a database of credentials issued. (The individual is responsible for wallet backup.)  
4. The person holds their issued credentials in their personal wallet. They have full autonomy to hold, expose, and delete credentials. 

A completely separate flow is used for reputation interpretation, as shown below:

** INSERT IMAGE HERE **

1. The DAO or entity that wants to check the reputation of someone refers to an Issuer Registry to determine what guilds are relevant and reliable. tomiDAO will have a public Issuer Registry, but others can create third-party registries and a reputation interpretation engine can refer to whatever source it chooses.
2. The DAO requests credentials from the individual who wants to participate. The DAO could choose to ask for any set or subset of credentials it wants to request. The requesting entity should provide clear information about how the credentials will be used (for internal use, public to participants in the DAO, etc.)
3. The participant exposes (or declines to expose) the relevant credentials from their wallet. The user can choose to expose all of the credentials requested or any selective credentials they want to expose.
4. The DAO or reputation engine calculates a reputation score or provides a dashboard for the community to assess the reputation of the individual. The reputation engine can also use other inputs such as social network participation, public online activity, and on-chain information about the wallet holder.

This approach allows decentralization at several levels:
* Anyone can form a guild to issue verifiable credentials.
* Any entity can issue a Registry list of trusted guilds.
* Any entity can use one or more registry to determine the guilds they want to trust.
* Any entity can choose which guilds to trust, whether or not they are on a registry.
* Any entity can combine verifiable credentials from the tomiNet DAO and also use public data such as online data, NFTs and other on-chain holdings, social media information, etc. 
* Any entity issuing a reputation score can weight the data however they feel it is relevant to the particular decision being made or rights being given to the person.
* Every person with a wallet can determine which credentials they want to expose to entities.

All of these different layers of configuration allow for a highly decentralized system that allows multiple ways of interpreting “reputation” based on a person’s history and accomplishments.

### Negative reputation

A major challenge in Web3 is how to prevent destructive behaviors. Within a closed system or strictly financial system, completely trustless solutions are possible. However, in a larger ecosystem where people can move from one blockchain to another and change public key addresses, people can repeat bad behaviors with no negative consequences. Rug pulls, aggressive behavior, and failure to complete funded projects are just some of the ways that people have exploited the trustless nature of blockchain. The tomi approach is to create a reputation system that also includes the ability to display someone’s negative reputation.

At the same time, everyone has bad days, everyone has enemies, and people do make reparations for their behaviors. Therefore, the system needs a way for people to contest accusations made against them, and to be forgiven if they have made up for the damage, apologized, or madea appropriate changes to their behaviors.

Negative reputation does require centralized authorities (eg, credit ratings agencies), because people will not want to collect and display any negative feedback or credentials they receive. This document outlines one potential approach to creating negative reputation with the ability for reconciliation built in.

Because of the delicacy of the issue of negative reputation, it will be implemented only after the credentials system is in place and working well, and only after smaller trials show the viability of these approaches. While this document offers one potential solution on “Negs” or negative reputation issuance, this approach may be the one implemented ultimately. The DAO should work collectively to experiment with multiple approaches to preventing bad behavior and always be flexible in upgrading the system. 

### Reputation system flow / architecture

## Credential issuance (NFT and VC)
The Credential Issuance DAO will be responsible for issuing credentials. Credentials can be issued either automatically (for example, verifying a wallet address received approval for a DAO approval), or by a group of people (Guild) in the DAO. 

## Goals
The Credential Issuance function of the DAO will provide the ability to issue Verifiable Credentials and non-transferrable NFTs that can operate as proof of reputation. The Credential Issuance function is separate from the Credential Recognition ability, which can be built into different areas of the DAO depending on the needs for recognition of different types of reputation.

The Credential Issuance, Reputation Interpretation Engine, and the Self-Sovereign Identity Wallet (out of scope) are primitives of DAO tooling that are currently missing in the Web3 industry in general. These specifications may help guide other DAOs towards appropriate technologies, and tomiDAO may offer these services to other DAOs as a service. tomi is the first project to undertake a crypto wallet with built-in support of standard W3C DIDs and W3C VCs within the wallet, providing control in the hands of the users for selective disclosure of their personal data. The tomiDAO will leverage this technology for an advanced application of reputation and credentialing that is sorely missing in the DAO space. 

## Success Metrics
Ability to perform all of the following:
* Issuance of Verifiable credentials for participation, issuance to tomi wallet
* Integration with guild.xyz or creation of a similar functionality in terms of the ability to recognize an authorized committee in the DAO
* Automated DAO functionality to recognize submission of proposals, voting, allocation of funds
* Steward and team implementations for issuing certification of work performed
* Ability of teams to define their VCs
* Ability to issue non-transferrable NFTs in cases where someone does not have the tomi wallet
* Export of all VC types with descriptions to a public database
* Maintenance of reporting (export or dashboard of activity) on all VC issuance guilds approved by the DAO
* Advanced: Offering of DAO tooling services to other DAOs for cross-DAO credentialing and reputation recognition

## Assumptions and Dependencies
Dependency: Completion of the SSI components of the tomi wallet to receive VCs.
Dependency: Definition of standards for the VC, performed in the SSI wallet definition phase.
Assumption: Even when a credential is issued, it requires consent. Therefore, the receiving wallet needs to validate its acceptance of the credential.
Assumption: Some people who will want credentials will not have tomi wallets. In those cases, they will be issued NFTs, with minting costs on the recipient. The tomiDAO will accept the NFTs as a slightly inferior proof of reputation. NFTs issued outside the tomi wallet cannot assure any type of privacy.

## User Stories
* Jan serves on the Problem Definition Guild in the DAO and is the lead writer for the call for proposals for an upgrade for the tomi Wallet. The PD committee issues 2 VCs to Jan: One for writing ability and One for project coordination.
* Once the call for proposals is up on the DAO, Walt, Xak, Yap-ID, and ZkID all submit proposals. The DAO automatically issues VCs to all 4 of the applicants acknowledging that they have submitted proposals that qualify for the call.
* Walt wins the proposal and receives the funding for the first milestone of the upgrade. The DAO issues a VC showing they are the winner and how much the proposal was for.
* Walt submits the wallet addresses of all members of the team who are writing the code for the feature.
* Walt submits the code for the feature. It’s late and is missing some of the features. The Awards Guild does not accept the submission and issues a “Nice try” VC to Walt as well as to each of the individuals on the team.
* Walt re-submits 2 weeks later, and the work is excellent. The Awards Guild submits a VC to Walt and each of its coders for excellence in code, but a poor mark in punctuality, and releases the funding for the work’s completion. The DAO automatically issues Walt a VC identifying it as a DAO participant who has submitted and completed execution of a successful DAO proposal.

### Requirements

### The DAO top-level credentialing guild

The top-level Credentialing Guild will consist of the DAO stewards or a committee of 7 nominated by the stewards for the first year of the DAO (depending on the needs in terms of time). After 1 year of operation, an election will be held for the Guild. The credentialing guild elections will be every year with half (alternative 3 or 4) of the guild being replaced each year. The term of service will be 2 years. The replacement of half of the guild is to ensure that there are always members with experience. Elections will be done according to the DAO election protocol.
The tomiDAO will have a top-level DAO Credentialing Guild responsible for:
* Giving itself a better name.
* Issuance of VCs related to the DAO. Initially, this guild will issue all VCs, but as new Guilds emerge, they will take on specific certification authority.
* Authority over formats of VCs and updates to the protocol for VC issuance.
* Maintenance of the code and upgrades to the Credentialing protocol (in collaboration with the tomi core team).
* Approval of other Guilds that will receive permission from the DAO to issue VCs that are official tomiDAO credentials.
* Maintenance of a public list of all approved Guilds and the types of VCs they are approved to issue.
* Maintenance of a database of VCs that have been issued (identifiers and meaning of the VCs).
* Making requests for changes to the term and size of the guild (self-governance). Proposals for changes will go to the meta-Governance DAO or to the full DAO for a referendum. (Depending on the maturity of the DAO at the time of decision.)
* Determining the costs and income model for issuance of DAO VCs. The credentialing services can be used by DAOs within tomi or those who are using it independently. This service has the potential to generate income for tomi. 
























  


