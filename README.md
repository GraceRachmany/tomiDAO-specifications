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

## Introduction

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

  


