# tomiDAO specifications: DAO Requirements for tDNS release


# Table of Contents
=================

  * [Introduction](#Introduction)
    * [Challenges](#Challenges)
    * [The Structures](#The-Structures)
    * [Pioneer control](#Pioneer-control)
    * [Representation of the Netizens](#Representation-of-the-Netizens)
    * [Limitations of token-based voting](#Limitations-of-token-based-voting)
    * [Goals](#Goals)
    * [Success Metrics (2024)](#Success-Metrics-(2024))
    * [Assumptions and dependencies](#Assumptions-and-dependencies)
       * [Dependencies](#Dependencies)
    * [User Stories](#User-Stories)
    * [Requirements](#Requirements)
    * [UX Mocks](#UX-Mocks)
    * [Questions](#Questions)
    * [Out of Scope](#Out-of-Scope)
  * [Top-level DAO](#Top-level-DAO)
    * [Strategy](#Strategy)
    * [Finance and Budgeting](#Finance-and-Budgeting)
      * [Main tomiDAO](#Main-tomiDAO)
      * [Current Procedure](#Current-Procedure)
      * [User Stories](#User-Stories-1)
      * [Requirements: Immediate Functionality](#Requirements-Immediate-Functionality)
      * [UX Mocks](#UX-Mocks-1)
      * [Questions](#Questions-1)
      * [Out of Scope](#Out-of-Scope-1)
    * [Stewardship and Council Elections](#Stewardship-and-Council-Elections)
      * [Council Elections Procedure](#Council-Elections-Procedure)
      * [Requirements](#Requirements-1)
      * [Responsibilities of the First DAO Stewardship Council](#Responsibilities-of-the-First-DAO-Stewardship-Council)
      * [Approval of the Council](#Approval-of-the-Council)
      * [Application](#Application)
      * [Voting](#Voting)
      * [Establishment](#Establishment)
    * [Calls for Proposals (Grants Program)](#Calls-for-Proposals-Grants-Program)
      * [Problem Definition](#Problem-Definition)
      * [Participation Compensation](#Participation-Compensation)
      * [Proposal Propositions: Pre-proposal Phase](#Proposal-Propositions-Pre-proposal-Phase)
      * [Discussions and Proposal Improvement](#Discussions-and-Proposal-Improvement)
      * [Collaboration Compensation](#Collaboration-Compensation)
      * [Team Building for Proposal Execution](#Team-Building-for-Proposal-Execution)
      * [Proposal Submission](#Proposal-Submission)
      * [Ranked Voting and Consensus for Proposals](#Ranked-Voting-and-Consensus-for-Proposals)
    * [Metagovernance: Oversight and Governance Changes](#Metagovernance-Oversight-and-Governance-Changes)
    * [The tomiDAO Approach to Identity and Reputation](#The-tomiDAO-Approach-to-Identity-and-Reputation)
      * [The Challenge of Identity: Rationale for a Reputation System](#The-Challenge-of-Identity-Rationale-for-a-Reputation-System)
      * [Separation of Reputation Issuance and Interpretation](#Separation-of-Reputation-Issuance-and-Interpretation)
      * [Decentralization of Reputation](#Decentralization-of-Reputation)
      * [Negative Reputation](#Negative-Reputation)
      * [Reputation System Flow / Architecture](#Reputation-System-Flow-Architecture)
    * [Credential Issuance (NFT and VC)](#Credential-Issuance-NFT-and-VC)
      * [Goals](#Goals-1)
      * [Success Metrics](#Success-Metrics-1)
      * [Assumptions and Dependencies](#Assumptions-and-Dependencies-1)
      * [User Stories](#User-Stories-1)
      * [Requirements](#Requirements-2)
        * [The DAO Top-level Credentialing Guild](#The-DAO-Top-level-Credentialing-Guild)
          * [Credential Issuing for Top-level Credentials](#Credential-Issuing-for-Top-level-Credentials)
          * [Compensation for the Credentialing Guild](#Compensation-for-the-Credentialing-Guild)
        * [Creation of a Guild](#Creation-of-a-Guild)
        * [Certificate Definition for Guilds](#Certificate-Definition-for-Guilds)
        * [Negs: Certificates of Bad Reputation](#Negs-Certificates-of-Bad-Reputation)
        * [Certificate Issuance for Guilds](#Certificate-Issuance-for-Guilds)
        * [Automatic Credential Issuance](#Automatic-Credential-Issuance)
        * [DAO Execution Credentials](#DAO-Execution-Credentials)
        * [Credential Pick-up Hub](#Credential-Pick-up-Hub)
      * [Reputation Interpretation Engine](#Reputation-Interpretation-Engine)
        * [Issuer Reputation](#Issuer-Reputation)
        * [tomi Reputation Score](#tomi-Reputation-Score)
        * [Warrants Authorities](#Warrants-Authorities)
        * [tomi Warrants Authority](#tomi-Warrants-Authority)
        * [Warrants Authority Standards](#Warrants-Authority-Standards)
        * [Warrants Expiration](#Warrants-Expiration)
        * [UX Mocks](#UX-Mocks-2)
        * [Questions](#Questions-2)
        * [Out of Scope](#Out-of-Scope-2)
    * [Credential Recognition](#Credential-Recognition)
    * [Membership and Recruitment](#Membership-and-Recruitment)
  * [tDNS DAO](#tDNS-DAO)
      * [Goals](#Goals-2)
      * [User Stories](#User-Stories-2)
      * [Technical Decisions](#Technical-Decisions)
      * [Initial Stewardship](#Initial-Stewardship)
      * [Budgeting and Finance (within tDNS-DAO)](#Budgeting-and-Finance-within-tDNS-DAO)
        * [Income Sources: tDNS DAO](#Income-Sources-tDNS-DAO)
        * [Annual Budgeting](#Annual-Budgeting)
        * [Payment for DAO Participation](#Payment-for-DAO-Participation)
        * [Financial Council](#Financial-Council)
        * [Monthly Retainer Smart Contract](#Monthly-Retainer-Smart-Contract)
        * [Revenue Streams](#Revenue-Streams)
      * [Domain Management](#Domain-Management)
        * [Registry-Registrar Relations](#Registry-Registrar-Relations)
        * [Domain Release and Pricing](#Domain-Release-and-Pricing)
        * [Branding and Art](#Branding-and-Art)
        * [Domain Registry Management and Privacy](#Domain-Registry-Management-and-Privacy)
      * [Content Moderation and Community Guidelines](#Content-Moderation-and-Community-Guidelines)
        * [Goals](#Goals-3)
        * [Success Metrics](#Success-Metrics-3)
        * [Assumptions and Dependencies](#Assumptions-and-Dependencies-2)
        * [User Stories](#User-Stories-3)
        * [Requirements](#Requirements-3)
        * [UX Mocks](#UX-Mocks-3)
        * [Questions](#Questions-3)
        * [Out of Scope](#Out-of-Scope-3)
        * [Design Considerations and Vulnerabilities for Content Moderation](#Design-Considerations-and-Vulnerabilities-for-Content-Moderation)
      * [Content Guidelines](#Content-Guidelines)
      * [Default URL Banning and Default Moderation Policy](#Default-URL-Banning-and-Default-Moderation-Policy)
        * [Design Considerations and Vulnerabilities for Content Moderation](#Design-Considerations-and-Vulnerabilities-for-Content-Moderation) 
        * [Initial Misidentification Process for Content Moderation by the DAO](#Initial-Misidentification-Process-for-Content-Moderation-by-the-DAO)
        * [Appeals Process](#Appeals-Process)
      * [Standards and Pricing for Third-party Moderation Plug-ins](#Standards-and-Pricing-for-Third-party-Moderation-Plug-ins)
     * [Dispute Resolution](#Dispute-Resolution)
  * [Out of Scope: Marketing DAO (Future)](#Out-of-Scope-Marketing-DAO-Future)
  * [Out of Scope: DevelopmentDAO (Future)](#Out-of-Scope-DevelopmentDAO-Future)
  

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

![Sketch 1](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/e161ad09-508e-4d8f-be66-af11c0261898)

## Strategy
The tomiDAO Stewards will hold strategy meetings twice per year: June and January. The January strategy meeting will be in-person and funded by the DAO. Depending on the funding from the DAO, the tomiDAO stewards may opt to sponsor accommodations or travel. Sponsorship of participants should be used primarily in order to balance the representation of the different interest groups in the tomi ecosystem.

The strategy meetings will include representative participants from the following groups: 

* tomi team
* tomiDAO (stewards, proposal winners, etc.)
* tomi Pioneers
* tomi token holders
* tomi community members, including tomiArmy and tDNS domain holders 
* projects under the tomi umbrella (tomiChain, Gems, etc.)

![image](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/7ece7289-0974-46eb-861c-2920beadb577)

Each of the above entities will have decision-making power in the strategy discussions. Rather than individuals having power, each of the entities above will have equal decision-making power in prioritizing the strategy if there is a vote or proposal that needs to be passed by consensus. Each of the 6 entities can have their own internal decision-making process which is not dictated by the DAO. For example, the tomi team may be governed by a CEO or executive team, whereas the tomi Pioneers may use voting to determine their stand or to elect a representative.

Strategy discussions should start online and then be completed in an in-person format whenever possible.

The suggested process for strategy discussions: 

![Workflow 1](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/04f1ad69-47d2-4c7d-a704-c94393c0faf1)

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

![Workflow 2](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/b5abea16-fb02-4ef5-9918-0ca250cb20e0)

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

![Sketch 2](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/ad635a37-dd83-4702-a0e7-5ccbb296c6de)

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

![Workflow 3](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/f80c2c5a-b71a-443f-9018-7bc0b22bc9ed)

1. A person performs work and the guild responsible for oversight of that work issues a credential to the tomi Credentials Portal. The guild may keep a database of certificates issued, or they may discard all data once the certificate is issued.
2. The person logs in with their wallet to the Credentials Portal. The Portal displays all credentials that have been issued and not yet collected for that wallet address / login.
3. The person can collect or reject the issued credentials. If they accept their credential, it is sent to their wallet and deleted from the Portal. If they reject a credential, it is deleted forever from the Portal. The Portal does not store a database of credentials issued. (The individual is responsible for wallet backup.)  
4. The person holds their issued credentials in their personal wallet. They have full autonomy to hold, expose, and delete credentials. 

A completely separate flow is used for reputation interpretation, as shown below:

![Workflow 4](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/1295a4f1-8a68-42ed-bde0-691827439a80)

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

Credential issuing for top-level credentials:
* At least 2 members of the guild must approve the issuance of VCs.
* The guild may retract VCs within 7 days with a majority of 5/7.
* The guild may expel any member with a majority of 5/6 of the other members. Grounds for expulsion include violation of community guidelines, false issuance of credentials, and failure to do the fair share of work.
* If there are disputes among members, the guild applies for conflict resolution to the conflict resolution team. The conflict resolution team should try to resolve the conflict in conversation. If that is not possible, the conflict resolution team may recommend expulsion of a guild member, or a re-election of all members if it is clear that the guild is no longer functioning well.

Compensation for the credentialing guild: 
* The initial commitment is projected 3-5 hours/week.
* Initial compensation will be the equivalent of $1000/month in $TOMI tokens.
* After a 6 month trial period, the credentialing guild will report on its actual time spent and the work done, and suggest an appropriate ongoing payment.

Creation of a guild
Additional certification Guilds can be created in one of two ways:
* The DAO can declare the need for a guild and either nominate initial members or run an election.
* A guild can self-declare and apply for approval from the top-level credentialing guild.

Guilds are responsible for:
* Issuance of approved VCs.
* Their own integrity and self-governance. They may or may not choose to change members, have general elections, etc.
* Maintaining their reputation. If a guild is not performing, they may lose their approval as an official tomiDAO issuer of VCs.
* Suggesting members of their guild for election to the top-level guild when elections come around.
* Guilds can also operate “unofficially”. If a guild wants to use the tomiDAO VC issuance system, they can do so. The Top-level Credentialing Guild may charge a fee for the service.

Certificate definition for guilds
Guilds can define the following parameters for their Verifiable Credentials:
* Name
* Description
* Image / artwork
* (optional) Up to 8 attributes
* Quality rating for each attribute (1-10)
  
Guilds can create simplified VCs that don’t have quality ratings. For example, they can create certificates of participation, awards for accomplishment, etc. 

![image](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/8dadc70c-88b0-48db-bfab-cca05f14dd74)

Guilds should issue participation certificates that include the following:
* Type of participation (member / senior member / manager / etc.)
* Length of participation (months/years)
* (optional) Level of participation (excellence, standard membership, other levels they want to note)
  
Participation certificates can serve as a way for DAO members to create a “resumé” of their experience with proof of participation under any guild they belong to.

![image](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/23546cb4-4501-459f-95e2-9ac244b3e531)

Guilds can submit a table describing their certificates and their meanings to the DAO Reputation Engine, or make it public to all. Using the certificate table, the tomiDAO, other guilds, and other ecosystems can interpret the participation level and quality of all members of the tomi Guilds system. Because of the complexity of reputation interpretation, it is recommended that Guilds limit themselves to a few types of certificates. Too many certificate types will make it difficult to interpret for outsiders (which is the whole purpose of the certificates). While the system will not limit the number of certificates, the interpretation engines initially will be limited in their capabilities. It is expected that AI will be able to be implemented to interpret reputation and certificates, but it is unlikely to happen within the first 2 years of the system’s implementation. 

If possible, the system should be architected for cross-platform compatibility so it can be used by anyone in the EVM ecosystem.

Negs: Certificates of bad reputation

In an SSI system where people have discretion over what credentials to display (selective disclosure), it is difficult to report negative behavior, because participants can reject the credential or simply not display the credential. At the same time, if someone behaves poorly, rugs a treasury, or delivers poor quality services, the community wants to know that information. In the current environment, cheating often happens because people are anonymous and their reputations are not recorded anywhere. Furthermore, people’s reputations are a multitude of attributes. Some people might be amazing workers but have difficulty getting along in a team. It’s up to each team to decide whether they want someone friendly who does slower work or someone who is a recluse but gets more work done.

As a community, Web3 needs better signals of bad actors, or of people who simply are lacking in a particular skill that is needed for success in a particular context. Therefore, we need to have a system of recording negative activities and failures. (We also need a system of Reputation Rehabilitation, because people do take reparative actions and improve their skills based on feedback. That is out of scope for this document but should be developed based on actual use cases in the first year of implementation of the reputation scores.)

In order to ensure that guilds and the DAO can record people’s negative performance, the initial specifications include DAO execution credentials as well as a tomi Warnings Authority, where any negative certificates are registered. The guilds can issue one of the standard Negs and must include evidence (such as on-chain transactions) or a written explanation of the testimony. People can remain anonymous (for example, in the case of sexual harassment), in which case a single Neg may not be considered adequate to have a major negative impact on someone’s reputation. 

Initial proposal of available Negs:
* Financial negligence or malfeasance
* Poor work performance
* Social misconduct (online / IRL)
* Harassment or stalking (online / IRL)
* Physical violence
* Lies / dishonesty (verbal / financial)
* Obnoxious overshilling
* Poor treatment of employees / team members

We recognize that there are brilliant people who are not nice and that there are people who are socially awkward. It is each community’s decision regarding what behavior they tolerate and what Negs they recognize as significant. This is an experiment which we feel is important to the industry for identifying malfeasance and poor behavior, and we expect the system to evolve over time.

We recognize that people can create new identities and get a clean slate at any time. That feels appropriate for the purpose of the DAO. National enforcement authorities should deal with more serious violations. 

Workflow for Negs:
1. A guild or individual issues a Neg credential. Guilds must expose their identities, but individuals do not need to in circumstances of harassment or violence. Issuers are highly encouraged to offer a course of action to make up for the negative consequences.
2. The credential is issued to the person’s wallet, and to the appropriate Warrants Authority.
3. The individual can appeal or take appropriate compensation action (which may be as simple as an apology). 
4. If the rehabilitation is satisfactory, the original issuer issues the proof-of-rehab or proof-of-apology. They may also issue additional credentials (sometimes the compensation might be above and beyond the request).
5. The Negs are stored with the Warrants Authority, but they are secret and nobody has access to them without the permission of the recipient.
6. If an individual or guild wants to check someone’s Neg record (for example, for hiring, DAO applications, etc.), they make a request for the exposure of that person’s Warrant ratings. They can ask for a full report or just the highlights (number and dates of the Negs).
7. The person must approve the request for exposure of their Neg Record. 
8. The Warrants Authority will expose the data requested only to the authorized recipient and only for a specific use and period of time.
9. Deliberate or accidental exposure of other people’s Negs will result in a guild or individual being banned from asking for reports in the future.

Warning: Everyone has enemies, everyone makes mistakes, and sometimes people complain because they are in a bad mood that day. Having a few Negs should not exclude people from participation, particularly if they have taken reparative actions. On the contrary, someone with absolutely no negative reports may be gaming the system or using multiple identities. In other words, a totally clean record over time could be considered more suspicious than one with a few Negs.

Certificate issuance for guilds

Guilds will establish the requirements within the guild for issuance of the credentials. Some guilds might let any member issue a credential, others might require a majority vote, etc. 

The Guilds will submit its requirements to the Credential Pick-up Hub (temporary name). To issue credentials, one guild member will create the credential issuance on the hub. If it requires more than one signature, those signatories will log into the hub and confirm the issuance as required.


Automatic credential issuance 

* All guild membership will come with a VC automatically issued based on the amount of time served and the name of the guild that the person served in. 

DAO execution credentials

The DAO will issue a credential to everyone who has performed work or received funding from the DAO, including retroactive issuance. This will be done by the DAO Stewards or by the individual/group/committee who commissioned the work to be done by the DAO. For example, this specification was commissioned by DAO Owl and Camel, so they will issue a credential to the wallet addresses who have performed work under these specifications.
The purpose of the DAO credential is to let the community know the quality and completion of DAO-approved proposals. At each milestone and at the completion of a proposal, the responsible party will issue one of the following credentials to the wallets involved in delivering the work:

* Outstanding: Completion of the proposal that went beyond the requirements.
* Excellent: High-quality delivery 
* Good: Satisfactory delivery of the expected work.
* Incomplete: The work was not delivered in full.
* Unacceptable: The work was delivered but the results did not meet the minimum criteria that was expected based on the amount budgeted and the time to deliver.

In addition to quality certificates, the DAO can also issue one of the following indicators of the group’s adherence to timelines:
* Early delivery
* On-time delivery
* Late delivery

It’s important to note that these are self-sovereign Verifiable Credentials, meaning that the proposal-maker does not need to accept the credential and they have complete sovereignty to display or not display the credential when asked. However, the winning of the proposal in the DAO is an on-chain activity, so if someone receives funding from the DAO but does not show a credential that the work was completed, the lack of a completion credential serves as a negative reputation signal. 

Credential pick-up hub 

Credentials are issued from the guilds, but a person must accept the credential to their wallet. The Credential pick-up hub will be a website created and stewarded by the tomiDAO. Participants log into the hub and see the list of credentials they have been issued. Participants can accept or reject the credentials that they are issued. The portal can display the credentials in the person’s wallet plus any unclaimed credentials. Credentials are stored in the wallet and displayed when the wallet is connected to the portal.

By default, credentials will not be held by the issuing guild or by tomi, nor will they be stored in the credentials issuing platform. When someone rejects or deletes a credential, it disappears forever. When someone accepts a credential it is stored in the person’s wallet and each person can determine how they want to back up the credentials. Tomi can serve as a credential storage if that is what the user wants, however the default is for the user to make their own choices in storing credentials. 

![image](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/a5d420cb-ea4a-42f4-8547-3c37d9b14ca8)

The tomi Wallet will allow people to export credentials to a physical storage device, to store them in IPFS or in Google Drive as an encrypted file. Self-custodianship is key to creating a system that gives people full sovereignty over their reputation and credentials. Over time, other third parties may offer services to store credentials. This is not a base functionality of the system, but it is feasible to imagine a third-party business model in creating safe storage for people’s credentials. 

IMPORTANT NOTE: Unlike blockchain-based NFTs, the credentials are OFF-CHAIN and cannot be restored in case of loss. The credentials are stored on the DEVICE where the person chooses to store them. In the case of loss or damage to the device, the person cannot restore the credentials if they do not specify more than one storage location.

![image](https://github.com/GraceRachmany/tomiDAO-specifications/assets/46278307/3b871a69-9da1-4d92-9391-c9f0fb9d2329)

Once a credential is accepted to the wallet, it is stored in the wallet and disappears from the portal. The portal does not store credentials. Each issuer can decide whether to store the issued credentials, but the primary responsibility for storing credentials is with the recipient. The recipient can also permanently delete credentials. Tomi does not store credentials unless that service is requested by the user. The tomi wallet can be configured for local storage, storage on an external or cloud drive, or potentially on IPFS or other storage chosen for integration by the tomi team. 

### Reputation Interpretation Engine

As explained above, there are different circumstances under which someone might want to understand someone’s reputation or trust score. The trust needed for someone to be on a Stewardship council is different than the trust needed for someone to be allocated funds for a marketing proposal. Therefore, the tomiDAO intends to create a generic reputation interpretation engine. A generic Reputation Interpretation Engine could become generic DAO tooling both for tomi and for other DAOs. 

The reputation engine will allow anyone to create their own interpretation graphs with output that gives them up to 5 ratings scores for grouped information. The builder of the interpretation creates their categories and then includes input that makes up the score on each of the ratings. 

The reputation engine can input any of the information that is included in the tomi SSI Wallet, including Web3 credentials, Web2 proofs, verifiable credentials, on-chain activity, and any other credentials that the individual wallet has accumulated.

When creating a reputation score, the assumption is that each of the 5 ratings will be listed from 1-100 (positive ratings) and there will also be a warning score from 0 to -100, which indicates the types of warrants and negative ratings accumulated by the wallet, as well as a rehabilitation score which shows the actions the person has done to remediate any damage they have caused in the past.

The cumulative score will allow people to understand the capabilities of the person they are assessing. For example, if someone is applying for funding from the DAO, the reputation interpretation score might include financial responsibility, technical capabilities, and communications skills. For this particular proposal, it might not be important to know if the person has good social skills, because it’s a development contract. In that case, the person setting up the report would look at someone’s Github, participation in other DAO proposals, delivery of technical work, and the documentation for the projects. They wouldn’t need to look at PoAPs for conferences, because they don’t care about social or marketing skills for this particular contract.

To create a full specification for the reputation engine, the DAO should allocate funding in late 2024 or early 2025 for the specifications writing and then solicit proposals for the development tasks. 

Issuer Reputation

Reputation credentials are issued by different guilds as described above. In order to determine which guilds are trusted verifiers, tomi will issue a registry of issuers and certificates that tomi considers to be valid. The tomiDAO Stewards or a committee elected by the tomiDAO will be responsible for establishing and maintaining the Tomi Trusted Verifiers registry.

The registry is a list that validates that the certificates issued are what the guild claims them to be. The tomi registry does not judge the quality of the certificates, but just that they are what they say they are. In other words, if a Guild issues a “Certificate of Participation”, and that Guild is on the tomi verified guild registry, it means that tomi has checked that the certificate is issued to participants in the guild. If the Guild issues a qualitative certificate, for example, that someone has accomplished outstanding work, a listing on the registry would mean that the quality of those certificates really does signify outstanding work. 

The Stewards will devote 8 hours each month to updating the registry. The DAO will create a capability for users to issue complaints about certificate issuance so that the Stewards can be made aware if there are issuers that need to be removed from the registry.

The Registry system will offer other authorities to publish their own registry of recommended validators. For example, a known entity such as “Vitalik” or “BanklessDAO” could issue a registry of Guilds that offer valid certificates. This mechanism provides reputation interpreters to choose the authority that they feel is most relevant for validating the validators. If tomi were to become opaque or corrupt, or have a low quality standard, reputation interpreters could use other registries as an alternative or a supplement to the tomi list of valid issuers. In this way, the certificate issuance is fully decentralized, because any third party can perform its own audit of certificates. If the quality of that registry is superior to tomi’s registry, then others will natural prefer other certificate issuer registries. Eventually, it may be unnecessary for tomi to maintain the registry if there are enough alternative registries of high quality. 

The intention is that the registry may be replaced by a more distributed system in the future where the DAO participants and users of reputation can assign reputation to the certificate issuers. For example, there may be a way to review validators in the future. Qualitative reviews may eventually replace the need for a registry of verified validators. The DAO will consider such solutions in the future.

### tomi Reputation Score

The tomi reputation score will be implemented after 3 months of operation of the Credential Issuance Engine. The reputation score is designed to identify the reputation of the person who is taking an action within the tomiDAO and determine their capabilities as they relate to the action they want to take. Examples:
* Anastasia is running for the stewardship council of the DAO
* Breno is submitting a proposal to the DAO
* Chinera applies for a job as community manager

In each of these cases, the DAO can ask for the applicants to submit their information for a reputation assessment. Initially, there will be only positive assessments until a Warrants Authority is implemented.

The initial reputation engine will simply allow a permissioned way for applicants to show any of their credentials they want to show. They might show NFTs or PoAPS, certificates from their accomplishments in the DAO, the amount of time they have held or staked $TOMI, evidence of participation on the Discord channels, etc. Any evidence they wish to open up in their wallet will be presented to the authorized receiving party. 

The portal will allow for the DAO to display that information to anyone in a particular guild, or to just the individuals who are making the assessment.
Furthermore the DAO Stewards may create a “tomi Reputation Score” which represents someone’s trust level. The stewards will determine whether such a score is necessary and submit a proposal to the DAO on how the engine will work for the reputation score. The DAO can then solicit proposals for the development of the reputation score creator.


### Warrants Authorities
One of the main obstacles to identifying bad actors and improving people’s behavior is that only positive certificates can be issued. Organizations issue Proofs of Participation, but not Proofs of non-participation, proofs of chronic tardiness, or proof of overstepping one’s bounds. Furthermore, it is a basic human right to have selective disclosure. In other words, if someone has made a mistake in the past, they do not have to let others know about it unless they want to.

In the above configuration or reputation issuance, it is possible to know some things by omission. If someone is awarded DAO funding but does not show a certificate of completion, the assumption can be made that they did not complete the task or did a poor job. But if someone has spammed the Discord, failed to pull their weight in a tomiArmy team, etc., there is no on-chain record and therefore it is impossible to find repeat offenders. Furthermore, when people are not punished, they can continue the behavior rather than learning their lesson and improving themselves and the community as a whole.

The Warrants Authority is an experiment that replicates something like a “criminal records check”, where there is a repository of negative ratings (Negs). Just like a criminal record check, the individual needs to give authorization to the party who requests the check. 

The Warrants Authority will run for a period of 6 months and then it will need to issue a report of how the experiment is going and make recommendations for upgrades.

Whenever a guild issues a Neg, they also issue it to the Warrants Authority, which keeps a record of all negative reports to all wallet addresses in the tomi system. When individuals apply for participation as a steward or allocation of funds from the DAO, they will be asked to reveal a summary report of their Negs for review. They have the right to refuse to show their report, and still apply for these positions. 

Likewise, people will have the right to appeal and ask for rehabilitation. The complainant could ask for any type of compensation, from an apology to a repair of damage, etc. The Warrants Authority will encourage all parties to issue rehabilitation requirements for all Negs, to attempt to always improve the community. Usually a wrong can be easily rectified, but the Neg records will allow the community to understand whether apologies are sincere based on repeat behavior.

A report with fewer than 3 Negs is considered completely clean and will be issued as such, unless there is proof of a serious offense such as rugging a large amount of funds, physical violence, etc. For serious complaints, the Warrants Authority expects the complainant to take legal action in the appropriate jurisdiction. The WA does not serve as an enforcement authority, but as a reputation repository only.


tomi Warrants Authority

Warrants Authority Standards

After 6 months of operation, the tomi Warrants Authority will create a recommendation document that will 

Warrants Expiration 

A person’s past should not be held against them indefinitely. The following standards are recommended but will be updated after 6 months of operation of the Warrants Authority (see above):
* Verbal / text offense: 3 months if there are no other complaints in that time, or if the person undergoes communications training/personal development. 1 year if this is a common occurrence.
* Physical assault or harassment: as per local jurisdiction laws, maximum 5 years
* Rug, failure to pay invoices, or financial cheating: 1 year after the refund of the full amount rugged or if forgiven by those wronged.
* Poor work performance: 3 years
* Tardiness, lack of professional conduct: 6 months
* Late payments: 6 months if no repeat, 3 years for other occurrences

UX Mocks

Questions

* How should we think about issuance of a “score” or reputation interpretation engine?
* Assuming most of the Warrants Authority is done through automation, how big should the stewardship committee be? What should be the responsibilities of the stewards? 
* Can we make this into a team strengthening activity rather than give it a feeling of punishment and shame?

Out of scope

* Ratings of the guilds themselves. Over time, guilds will get a reputation of their own (for example, one guild may give out certificates easily, and another guild might be very strict and only give out certificates of high quality). Initially tomiDAO just has officially validated guilds and ones that are not validated. The intention is to create a guild reputation system so that it is not necessary to have a central authority (tomiDAO) to validate the guilds.
* Reputation Rehabilitation. A team or individual may be in a situation where they under-perform, receive warrants, or otherwise establish a poor reputation. These teams and individuals may take actions to make up for their past poor performance, and they can apply for certification that they have repaired damage, improved their social skills, etc. We recognize the need for a rehabilitation authority and we recommend the Stewards create a reputation rehabilitation procedure over the course of the first 2 years, based on actual instances.


### Credential recognition

Functionality for recognizing people’s participation records and reputation when submitting proposals, voting, or participating as stewards.

### Membership and recruitment
* Identification of TomiZens
* Basic membership requirements and tiers of membership as TomiZens
* Connectivity with the tomi SSI Wallet
* Recognition NFTs and POAPs
* Recognition of certificate issuance
* Whitelist of acceptable guilds



# tDNS DAO

### Goals

Success Metrics

* Issuance and adherence to budget for 2024
* Sufficient stewardship for the first 1000 websites launched on the tomiNet
* Domain management of the .com and .tomi domain names for year 2024-2025
* Launching of AI for identification and blocking of content that violates community guidelines
* Enabling the implementation of APIs for content moderation from third parties
* Enabling discovery tools (search/crawlers) from third parties
* Implementation of appeals committee for content that is caught by AI but should not be banned
* Launch of a dispute resolution mechanism/team

Assumptions and dependencies

* The DAO assumes that the tomi development team will have launched the tomiNet in a usable format.
* The tDNS and DAO need to be linked properly by the R&D team at tomi for the functionalities described.
* To have a WWW to manage, there must be websites launched using the tDNS. All of the appropriate infrastructure (domain hosting, SSH equivalent, DDOS prevention, etc.) needs to be in place for the tDNS DAO to be required.
* Stewards and other people spending time managing the DAO need to be paid. The tDNS DAO will be dependent in its first year on the tomiDAO. The assumption is that the tomiDAO will allocate appropriate funding, including the issuance of the promised annual $TOMI 10,000,000 to the DAO.

### User Stories

* Dana holds multiple partner tDNS names and auctions them to people who want to create their websites in tDNS
* Estelle runs an open source company and creates an ad-free search engine that can be used on the tDNS network. She buys searchme.com, and includes a “tip jar” for tomiZens who want to make sure her team has the funds to keep searchme up and running.
* Fajar runs an ecommerce business and builds a website at the tomi domains BuyStuff.com and BuyStuff.tomi . His website accepts ERC20 compatible tokens as well as fiat currency in his local country.
* Gloria develops APIs for content moderation. She uses LLM APIs for basic moderation as well as user feedback to provide a variety of filters. Her website, www.protection.com, allows people to pay for software licenses to use a suite of content filters such as “Parental Protection”, “Safe for Work”, and “Uncensored Adult”.
* Hester is a political activist and runs an exposé site where they publish information exposing government corruptions, scandals, and conspiracy theory opinion pieces.

Requirements 

UX Mocks

Questions

Out of Scope

### Technical decisions

The tomi development team is currently in charge of the following technical decisions:
* Name formats
* Technical specifications
* Security and managing malicious traffic
* Abuse prevention
* Scaling and robustness
* Failover and backup
* Underlying infrastructure
* Node development and rewards

### Initial stewardship
The tomi development team will continue to manage the technical aspects of the tomiNet for the first year of operations. After the first 6 months of operations of the tomiNet parallel WWW, the tomiDAO Stewards will set up a series of conversations with the tomi team to understand more deeply the technical operations. After this conversation, the Stewards will make a proposal for how to decentralize the technical aspects of management of the tomiDNS.

### Budgeting and finance (within tDNS-DAO)

#### Income sources: tDNS DAO

The tDNS sources of income will be as follows:
* Sale of initial tDNS names (50%)
* Percentage of sales from partner tDNS (50%)

The initial tDNS DAO launch will be as follows:
1. Budgeting from main DAO for stewardship committee: February 2024
2. Election of a stewardship committee: March 2024.
3. Creation of DAO and multisig functionality for tDNS: April 2024
4. Full accounting and reporting of funds owed to the DAO from tDNS sales and partner sales: April 2023
5. Deposit of management funds into the tDNS DAO: May 15, 2024
6. Establishment of working annual and quarterly budget by steering committee: June 2024.

The tomi tDNS marketplace will provide a full accounting of all tDNS domain names sold on May 1, 2024 and at that time deposit the funds in the tDNS DAO. The tDNS DAO will be described in the tDNS section below. tDNS DAO will be managed by a steering committee of 7 people using a multisig and a Tally, Snapshot, Commonwealth, or similar ERC20-compatible DAO management technology. 

#### Annual budgeting

#### Payment for DAO participation

#### Financial council
* The DAO will have a steward council of 7 stewards with a multisig requiring 3 of 7 signatures for milestone approval. 
* The council will hold money for different proposals based on milestones accomplished, committee

#### Monthly Retainer smart contract
The Monthly Retainer smart contract will be created for the payment of council members, stewards, and other monthly salary requirements. Functionality of the Monthly Retainer smart contract:
* Hold in escrow budgets allocated from the DAO to specific councils and committees such that each amount is held for that specific group.
* Integrate with the DAO such that when people are elected to a committee, their wallets are connected to the smart contract for regular payment.
* Pay the monthly retainers/salaries as agreed upon by the election process.
* Provide a “stop” mechanism where a majority of the qualified voters (qualifications for that particular council) can take a person off the council and 

#### Revenue streams
The main revenue model is the tDNS registration. However, other revenue models may come into place, such as third-party add-ons for security, safety, and other types of services to the tomiNet members. 

### Domain Management

## Registry-Registrar relations

In Web2, registrars and web hosting companies serve important functions. Registrars help create a competitive market for domain names. Web hosts sell both domain names and other services to end users. While a discussion of hosting services is out of scope, because any domain hosting service can be used for tomiNet, it is expected that some of the functions of the registrars will need to be managed by the DAO after the first year of operations.

Registrars in the tomiNet are the same as domain owners. In Web2, there is some controversy about the value of “domain squatting”, which means the purchase of valuable domains with the intention to speculate on the price of those domains. tomiNet actively encourages the collection of valuable domain names in order to establish a fair market price, but the current system does not provide a way for people to contact a domain owner and make a purchase of a domain name. We expect the development of third-party marketplaces, and potentially the DAO may wish to implement policies regarding the sale and trade of domain names.

In January-February 2025, the DAO stewards will create a series of 3 online discussions of domain name management with the holders of tDNS names and tDNS partner NFTs and make it open to the public. They will discuss the relationship between the tDNS holders and those who want to create websites on those domains. Following these meetings, the Stewards will make recommendations of policies regarding the tDNS domain holders (registrars) and their place in the ecosystem. This will be an annual process that will involve all stakeholders in the health of the ecosystem.

At the time of writing, tomi is assuming there is a reason for this distributed role management in Web2 (registrars, hosts, domain holders) but the network does not yet have the volume to need to separate the different responsibilities. This specification assumes that as the network evolves, it will become obvious that additional decentralization of roles is necessary and that the community can come together to determine the appropriate steps and governance needed to ensure the health of the system.

#### Domain release and pricing
The initial tomiNet has released the Top Level Domains (TLD) at the price of $100 in $TOMI tokens, with an open auction for 48 hours. (Details of the Partner program can be found on the tdns.network website.)
After the first year of operation, additional TLDs can be released, based on decisions from the DAO. The considerations for releasing domain names should include:

* Demand for a certain TLD, for example, gaining a large number of participants in a country that wants to release the domains for their country, or teachers wanting to have a .edu domain name.
 	
* Demand for .com addresses and the need to offer additional addresses.
 	
* Requests from existing users.
 	
* Financial considerations for the viability of the tomiNet.

The process for releasing TLDs should include the following steps:

1. Public discussion and consideration of the release timing, 	costs of the domains, and the structure for auctioning and owning TLDs with that ending. In some countries, $100 up front might be prohibitive, and the DAO could create any structure it would like to in the future for specific domain names.
 	
2. Presentation of proposals for the release of the TLDs in question. If there is general consensus in the public discussion, it may be that only one proposal is necessary. Where there are differences of opinions, up to 8 proposals may be available in a 	voting round. If more than 8 proposals are presented, there will be signaling based on asessment of the discussion using LLMs to determine the 8 proposals most agreeable to the largest numbers of voters, and a validation of those 8 proposals by the stewards to make sure none of them violate the basic values of tomiNet.
 	
3. Ranked voting or yes/no voting for the proposals. In ranked voting, the winning proposal must have at least 40% consensus. Where there is less than 40% consensus on the top proposal, a runoff will be held between the top 2 proposals in the ranked voting round.

Voting in the ranked voting will be similar to the voting rights in steward elections:

The ranked voting recommendation for the candidates will be weighted for different levels of community participation:


* $TOMI holders: 100 votes
 	
* Pioneers: 500 votes
 	
* TomiArmy members with certification of participation: 200 votes (List to be 	provided by TomiArmy Stewards)
 	
* Active 	Discord and community members with proof of participation: 200 votes


* DAO experts based on list from DAO Owl: 200 votes


#### Branding and art

#### Domain registry management and privacy

### Content moderation and community guidelines

#### Goals
* To create a content-moderation system that bans the most egregious content from the tomiNet.
* To create a content-moderation system whereby users can choose their level of moderation by choosing the third-party content filters that suit them.
* To create and maintain standards that allow and encourage third-party content moderation filters as plug-ins to the tomi Browser/app.

#### Success Metrics
By May 2024, tomi has a default content filter and a content moderation DAO that allows people to flag sites, have sites go through a content moderation committee, and ban sites.
By May 2024, tomiBrowser publishes standards by which any third party can create a content moderation filter to plug in. 
By June 2024, tomi will have a content appeals court that will handle content moderation appeals.
By July 2024, tDNS DAO will have a stewardship team for the filters and for bringing in additional developers to create their third-party filters.
By December 2024, several third-party content filters will have joined the tomi ecosystem.

#### Assumptions and dependencies
Without a large number of people doing content moderation, the tomiDAO will not be capable of taking on the task of moderation.

#### User Stories
* End-user: Dana works for an ecommerce company in a location where ecommerce is restricted. Her company uses the tomiBrowser to manage their websites. She uses the Default tomiNet basic moderation browser capabilities when at work, with an additional Corporate Plus filter by a third party that her company has approved. For her children, she has installed a Content filter in their native language which is child-safe. It also gives them sites in English, but through the same child-safe Content filter system. When Dana gets home, she loves to hear about conspiracy theories and freedom fighter movements. She uses an Adult Basic filter to allow her to see content that might be banned in the Corporate filter. 
* Third party: Magic Mods is a company providing third-party content filters. They offer a variety of filter plug-ins as add-ons to the tomi Browser. Their packages include family-filters, “Adult Entertainment” permission filters, and a variety of content moderation modules based on people’s preferences for particular ideologies and religious beliefs. 
* ??? Not sure how to think about tea

#### Requirements

#### UX Mocks

#### Questions

* What mechanism does the Google Safe List use for website screening? Is it a browser plug-in? How does it update? Is that something we can integrate for third-party integrations?
* Are there open-source filtering engines we can use for initial “censorship”?
* How did the Brave team approach censorship/browser filtering? Is there a potential partnership for the minimum viable filter?
* What is tomi’s responsibility for the initial censorship capabilities?
* Should banned URLs be allowed in more lenient censorship filters?
* To what degree can tomi use AI to identify content that is offensive or repetitive?
* How can we deal with content attacks? Bots? Other types of offenders?
* Should wallets become banned if they are too frequently associated with malicious behavior?
* Should AI-generated content have some limitations or labels on it?

#### Out of Scope

* Bots, scams, malicious code on websites, malicious code in images. The main purpose of the Google Safe Browsing List is to identify those sites that are actually malicious, phishing, or malware sites. This is obviously banned content and the tomi development team is tasked with managing security and threats.
* This document does not go into the community guidelines themselves. That could be done at the stewardship/metagovernance level, or the stewards or community could create a council to make changes to the community guidelines. Theoretically, anyone from the community could suggest changes and have it up for a vote in the DAO.

#### Design considerations and vulnerabilities for content moderation:
* Determining the right policies for a free speech but non-violent web is a difficult balance. tomiNet exists to encourage resistance to immoral regimes, while at the same time not wanting to support violent activity. The DAO exists to ban only the most egregious content, allowing people to use their judgment. tomiNet envisions toolsets (like parental filters) which will allow people to determine their own levels of comfort in browsing the web. The content moderation DAO may evolve over time to create ratings that enable such tools rather than outright censorship of borderline activities.
* Reporting itself is part of the content moderation. If only one person flags a site, it isn’t doing much harm (because people aren’t visiting the site). If hundreds of people are flagging a site, it is reaching many people so it is either offensive, or those people are creating a coordinated attack on certain kinds of content. In the case of collusion to attack certain types of content, it may be useful to down-regulate people who collude to censor (future feature).
* Reviewing websites with extreme content is an emotionally taxing activity, and seeing objectionable images can cause psychological damage. It’s important to ensure that people are not harmed by overexposure to this type of content.
* Technological solutions, for example, filters that blur pictures or AI identification of images, could be part of the solution in the future in order to avoid harm to people and streamline the censorship of the most obvious violations. A reviewer can always remove the filter, but the system could protect them from the initial impacts.
* The censorship mechanism could become an attack vector. The DAO could be flooded with spurious reports or someone could flood tomiNet with sites that violate the terms in order to intentionally flood the DAO with work.
* Artificial Intelligence has reached a level at which it can be trained to identify offensive content, but the current models have been overzealous in over-censorship, so some training will be required up front to allow adult content while outlawing the worst types of content. AI can also be used for repeat offenses using similar content, bots, or other types of non-human generated content. 
* For the initial iterations of censorship, the AI will be used as the first filter. We expect the automated moderation to be improved by the human process for misidentification. Rather than having all reported content go to DAO moderation, website owners will need to make an appeal that their content was mis-identified by the AI.

#### Content guidelines 
tomi wants to eliminate censorship, but there are some types of content that are so egregious that nobody should see them. We have several ideas on how to implement content moderation, and the DAO will make decisions on how to do so and provide the capabilities for automating the process as well as including participants in the moderation process.

#### Default URL banning and default moderation policy
This moderation will be the top-level moderation for tomi DNS, to ban URLs that are demonstrably violations of the content policies.

tomiNet bans highly inappropriate and unethical content. The initial guidelines for banning of content are:
* Child pornography and pedophilia.
* Extreme and gratuitous violence (does not include most forms of games)
* Illegal arms trading and human trafficking.

tomiNet starts with the most lenient possible policies, with the potential for implementing additional restrictions only when there is a wide consensus that an activity is universally immoral.


#### Design considerations and vulnerabilities for content moderation:

* Determining the right policies for a free speech but non-violent web is a difficult balance. tomiNet exists to encourage resistance to immoral regimes, while at the same time not wanting to support violent activity. The DAO exists to ban only the most egregious content, allowing people to use their judgment. tomiNet envisions toolsets (like parental filters) which will allow people to determine their own levels of comfort in browsing the web. The content moderation DAO may evolve over time to create ratings that enable such tools rather than outright censorship of borderline activities.
* Reporting itself is part of the content moderation. If only one person flags a site, it isn’t doing much harm (because people aren’t visiting the site). If hundreds of people are flagging a site, it is reaching many people so it is either offensive, or those people are creating a coordinated attack on certain kinds of content. In the case of collusion to attack certain types of content, it may be useful to down-regulate people who collude to censor (future feature).
* Reviewing websites with extreme content is an emotionally taxing activity, and seeing objectionable images can cause psychological damage. It’s important to ensure that people are not harmed by overexposure to this type of content.
* Artificial Intelligence has reached a level at which it can be trained to identify offensive content, but the current models have been overzealous in over-censorship, so some training will be required up front to allow adult content while outlawing the worst types of content. AI can also be used for repeat offenses using similar content, bots, or other types of non-human generated content. 
* The censorship mechanism could become an attack vector. The DAO could be flooded with spurious reports or someone could flood tomiNet with sites that violate the terms in order to intentionally flood the DAO with work. Again, AI can be used to manage repeat attacks.
* For the initial iterations of censorship, the AI will be used as the first filter. We expect the automated moderation to be improved by the human process for misidentification. Rather than having all reported content go to DAO moderation, website owners will need to make an appeal that their content was mis-identified by the AI.

#### Initial Misidentification Process for Content Moderation by the DAO

Content that is filtered by AI may not actually violate the guidelines. Any website owner can appeal to have their content reviewed by the content moderation DAO.

TOMI tokenholders and Pioneer holders participate in the DAO. Content moderation votes are 1-wallet-1-vote. Initially, changes to the content moderation policies will go through a process similar to Technical Proposals (until the DAO decides otherwise). 

A website is banned only if 9/10 viewers say it should be banned. Otherwise, it is considered permissible content. In other words, it must be clear to pretty much anyone that the site violates the content requirements for it to be banned.
1. Any website owner can appeal that their content was mis-identified. They must bring two vouchers who say that their content should not have been flagged. Vouchers can be any members of the tomiNet. People can vouch for a maximum of 50 sites per month, unless they ask for special permission. (For example, if they work in a profession, such as art curator, where they may be exposed to art expressions that could be mistaken for violence or pornography.)
2. Each day, the DAO creates a daily list of sites for appeal
3. The DAO chooses 500 tokenholders per every 60 sites flagged, and requests that they review the content that has been flagged. The DAO uses a round-robin algorithm that ensures that every token holder is summoned at least once per year, and that no tokenholder is called to moderate more than 5X more than the person called the least.
4. When a voter logs in, they are shown sites from the list in a mixed order which prioritizes the sites that have the most complaints but still provides a semi-random order so that not everyone sees the list in the same order.
5. For each site, the voter indicates yes if they agree it violates the guidelines or no if not. The voter can stop at any time or when they have voted on all the sites presented. After 1 hour, the DAO stops showing them sites, even if there are more sites on the list.
6. Voting on a site ends when:
        * There is 100% agreement (ban) from the first 9 voters.
        * At least 2 voters say it should not be banned.
        * There is 90% agreement from the first 10 voters.
        * 10 votes are collected. To ban a site, 9/10 must vote that it violates community standards.
7. If the site is to be banned according to the DAO vote, the site NFT is blocked. The owner receives the information on the reason it was reported.
8. If they want, voters receive a POAP indicating their participation in the DAO vote for having been part of the “good governance” team. In the future the system may use Verified Credentials for asserting their participation.

Note on Social Networks and Messaging Platforms: tomiDAO will not moderate content on social networking sites and other discussion sites. A networking site could be censored by tomi, but not parts of the speech. It is the responsibility of such sites to provide closed members-only areas for speech that could have them censored from the open web areas of tomiNet.

#### Appeals process

Banned sites may be reinstated under one of the following situations:
* Incorrect assessment of the site (formal appeal) or request for recommendations.
* Changes made to an existing site based on the site owner’s understanding of the violation.
* Purchase of an NFT URL that was previously banned and reinstatement by a new site owner.

In order to enter into the Appeals process, the owner must stake $100 in TOMI for the first appeal, $1,000 for 2nd appeal, $10,000 for 3rd appeal, etc. The staked amount vouches for the goodwill of the site owner. If the site still has highly unethical content, the staked amount is awarded to the people who had to view the offensive content.

Appeals will be handled by DAO members who:
* Volunteered for the council and provided their credentials to be on the Appeals Council.
* Were approved by at least 45/50 DAO voters that they can be trusted on the council.
* The council may include hundreds or even thousands of members.

When an appeal is accepted:
1. The DAO algorithmically chooses 3 people to handle the appeal.
2. The 3 must agree unanimously that the site has made the appropriate changes to be reinstated.
3. If the site is not to be reinstated, the council members must provide specific changes that would need to be made to reinstate the site.
4. If the site passes the reinstatement process, it goes through the full content moderation voting process by the DAO before the URL is reinstated.

#### Banning of tDNS URLs and wallets

The existing tomiDAO includes capabilities for blocking URLs and wallets for those who violate the moderation policies. However, this requires the Pioneers to vote on each and every address that needs to be banned. Not only is it unrealistic to expect them to spend time on voting, it’s unethical to ask the Pioneers to have to look at multiple offensive sites every day. Therefore, the functionality of banning wallets and tDNS addresses must be removed from the existing Pioneer-controlled tomiDAO and automated into the system described above.
Requirements for this functionality:

* AI banning is automatically implemented. If there is a contact address or email on the website, the AI will send a notification to the webmaster that the URL has been banned.
* Appeals committee selection and automated rewards system, as described above. Includes staking of tokens for those seeking repeated appeals.
* When voting is completed on an appeal, the website owner receives notification of the results of the appeal and the website is:
        * If approved, automatically reinstated (tDNS restored).
        * If declined, a record is established so the next time it is appealed, the cost will be higher. 
        * If the site is declined for a second or third time, half the amount staked goes to the appeals committee members who had the task of reviewing the site and the other half goes back to the DAO.
* When a wallet holds more than 5 tDNS names that have been banned and it launches a 6th banned sites within 1 month of having the last one banned, that wallet is banned.

The wallet owner may request an appeals process at a cost of $4800 in $TOMI tokens, with a $500 processing fee. If the stewards take the case, it is up to them to determine who will review the case. In either situation, the stewards receive the $500 processing fee. 

#### Standards and pricing for third-party moderation plug-ins

### Dispute resolution

The Dispute Resolution team should be elected and ready to start work on the day of the tomiNet launch. The DAO Stewards will put out a call for applicants for a team of 7 people to staff the initial Dispute Resolution team. Elections are expected to take place in the first 2 weeks of May 2024, based on the deployment plan for the tomiNet.

It is unclear what disputes will emerge, but the following are potential issues that could arise in the course of management of the tomiNet:
* tDNS disputes
* Monetary disputes
* Verification disputes
* Threat resolution 
* Damage due to technical problems

The initial scope of the Dispute Resolution team will be to handle any issues that emerge, and to investigate dispute resolution tooling for DAOs. The dispute resolution stewards will agree on a fair hourly rate, because it is unknown how much work will be needed initially. Every quarter, the Dispute Resolution team will submit a report to the DAO Stewards with budget and structural recommendations for advancing the dispute resolution capabilities of the team.

# Out of Scope: Marketing DAO (Future)

Currently, marketing is done by the tomi team and the tomi Army. The tomi Army was approved with the DAO budget and has become a separate entity. It is expected that if the tomi Army wishes to have additional funds, they would submit a full report of their use of funds and accomplishments to the DAO before additional funding. At that time, other marketing organizations would be eligible to compete with the Army for marketing funds, or the DAO may decide to create a marketingDAO as many other organizations have done.

# Out of Scope: DevelopmentDAO (Future)

Right now, all the development is done by the tomi team. The work will eventually be decentralized, as outlined in the original tomi Whitepaper, with a time trajectory of approximately 5 years.

With the proposal on an SSI wallet, we are for the first time making progress towards a decentralized development team. If the specifications document and prototyping are successful, we will be on our way to hiring an outside development team for a significant part of the tomiNet! But that’s still a far cry from having a research and development team managed on a DAO. Tools like WonderVerse and HyphaDAO have been some of the first to provide management tools like those in Jira to the DAO world. This article won’t dive into those sub-DAOs because we aren’t yet starting work there.




























































  


