---
title: "Team Topologies: Reading Notes"
categories: [reading]
layout: post
---
**Book:** [Team Topologies](https://teamtopologies.com/book) by Matthew Skelton & Manuel Pais 

* this unordered seed list will be replaced by toc as unordered list
{:toc}

# Highlighted Passages
## Chapter 1: Teams as the Means of Delivery
**pg 11:** ...[S]print planning for the now eight-person-strong team was a mix and match of requests across their stack of responsibilities. Prioritization was hard, and the frequent context switching even throughout a single sprint led to a dip in people's motivation. _This is not surprising if we consider Dan Pink's three elements of intrinsic motivation: **autonomy** (quashed by constant juggling of requests and priorities from multiple teams), **mastery** ("jack of all trades, master of none"), and **purpose** (too many domains of responsibility)._

**pg 13:** The goal of _Team Topologies_ is to give you the approach and mental tools to enable your organization to adapt and dynamically find the places and timing when collaboration is needed, as well as when it is best to focus on execution and reduce communication overhead. 

## Chapter 2: Conway's Law and Why It Matters
**pg 24:** One key implication of Conway's law is that not all communication and collaboration is good. Thus it is important to define "team interfaces" to set expectations around what kind of work requires strong collaboration and what doesn't. Many organizations assume that more communication is always better, but this is not really the case.

What we need is _focused_ communication between specific teams. _**We need to look for unexpected communication and address the cause**. (emphasis mine)_ 

**pg 29:** Team collaboration is important for gray areas of development, where discovery and expertise is needed to make progress. But in areas where execution prevails -- not discovery -- communication becomes an unnecessary overhead.

## Chapter 3
**pg 32:** In this book, "team" has a very specific meaning... a stable grouping of 5 to 9 people who work towared a shared goal as a unit. _**We consider the team to be the smallest entity of delivery within the organization**_. Therefore, an organization should never assign work to individuals; only to teams.

**pg 40:** _Analysis of sources of "cognitive load" is useful here._

**pg 40:** If we stress the team by giving it responsibility for part of the system that is beyond its cognitive load capacity, it ceases to act like a high-performing team and starts to behave like a loosely associated group of individuals, each trying to accomplish their individual tasks without the space to consider if those are in the team's best interest.

**pg 41:** A simple and wuick way to assess cognitive load is to ask the team, in a non-judgemental way: "Do you feel like you're effective and able to respond in a timely fashion to the work you are asked to do?" While not an accurate measure, the answer will help gauge whether teams are feeling overloaded.

**pg 42**: _Good case study on managing cognitive load by breaking into microteams._

This chapter also brings up the idea of _guilds_ around certain specialties to share knowledge and leaning.

**pg 56:** [T]echnology teams need to invest in proven team practices like continuous delivery, test-first development, and a focus on software operability and releasability. Without them, all the effort invested in a team-first approach to work and flow will be greatly undermined or at least underachieved.

## Chapter 4
**pg 68:** The key for the team to remain autonomous is for external dependencies to be non-blocking, meaning that new features don't sit idle, waiting for something to happen beyond the control of the team.

**pg 70:** [T]here needs to be a split between the responsibility of designing the cloud infrastructure process (by the cloud team) and the actual provisioning and updates to the application resources (by the product teams).

NOTE: This can be generalized -- one team decides how it should work, so others can work it autonomously.

**pg 72:** [T]raditional organizations adopting Agile -- moving to smaller batches of delivery -- often lacked the mature engineering practices required to keep a sustainable pace over time (such as automated testing, deployment, or monitoring). They could benefit from a temporary DevOps team with battle-tested engineers to bring in expertise and, more importantly, bring teams together by collaborating on shared practices and tools.
    However, without a clear mission and expiration date for such a DevOps team, it's easy to cross the thin line between this pattern and the corresponding anti-pattern of yet another silo (DevOps team) with compartmentalized knowledge (such as configuration management, monitoring, deployment strategies, and others) in the organization.

**pg 73:** Low maturity organizations will need time to acquire the engineering and product development capabilities required for autonomous end-to-end teams. Meanwhile, more specialized teams (development, operations, security, and others) are an acceptable trade-off, as long as they collaborate closely to minimize wait times and quickly address issues.

## Chapter 5
**pg 80:** [M]ultiple stream-aligned teams are the starting point... but an organization may also have several platform teams, a few enabling teams for different purposes (perhaps one addressing CI/CD and a second addressing infrastructure or architecture), and... one or two complicated-subsystem teams.

### On Stream-Aligned Teams
**pg 85:** What kinds of behaviors do we expect to see in an effective stream-aligned team? _(selected subset)_
- minimal (ideally zero) hand-offs of work to other teams.
- proactively adn regularly reaches out to the supporting fundamental-topologies teams (complicated subsystem, enabling, and platform)

### On Enabling Teams
**pg 86:** An enabling team is composed of specialists in a given technical (or product) domain, and they help bridge this capability gap. Such teams cross-cut to the stream-aligned teams and have the required bandwidth to research, try out options, and a make informed suggestions on adequate tooling, practices, frameworks, and any of the ecosystem choices around the application stack.

Enabling teams have a strongly collaborative nature; they thrive to understand the problems and shortcomings of steam-aligned taems in order to provide effective guidance. Jetta Eckstein calls them "Technical Consulting Teams"... provid[ing] guidance, not execution...

Enabling teams actively avoid becoming "ivory towers" of knowledge, dictating technical choices for other teams to follow, while helping teams to understand and comply with organization-wide technology constraints.

The end goal of an enabling team is to increase the autonomy of stream-aligned teams by growing their capabilities with a focus on their problems first, not the solutions per se. If an enabling team does its job well, the team... should no longer need the help... after a few weeks or months; there should not be a permanent dependency on the enabling team.

Knowledge transfer between an enabling and a stream-aligned team can take shape on a temporary basis or on a long-term basis. Pairing can be quite effective for some types of practices...

**pg 87:** What kinds of behaviors and outcomes do we expect to see in an effective enabling team? _(selected subset)_
- proactively seeks to understand the needs of stream-aligned teams, establishing regular checkpoints and jointly agreeing when more collaboration is needed.
- stays ahead of the curve in keeping abreast of new approaches, tooling, and practices in their area of expertise, well before an actual need is expected from steam-aligned teams.
- promotes learning not only inside the enabling team but across stream-aligned teams, acting as a curator that facilitates appropriate knowledge sharing inside the organization.

**pg 90:** Steam-aligned teams should expect to work with enabling teams only for short periods of time (weeks or months) in order to increase their capabilities around new technology, concept, or approach. After the new skills and understanding have been embedded in the stream-aligned team, the enabling team will stop daily interaction wiht the stream-aligned team, switching their focus to a different team.

### On Platform Teams
**pg 94:** What kinds of behaviors and outcomes do we expect to see in an effective platform team? _(selected subset)_
- uses strong collaboration with stream-aligned teams to understand their needs.
- relies on fast prototyping techniques and involves stream-aligned team members for fast feedback on what works and what does not.
- has strong focus on usability and reliability... and regularly assesses if the services are still fit for purpose and usable.

**pg 96**: A **key, key idea** -- a platform team has an internal topology of multiple other team types. Including sub-platform teams.

**pg 99:** _(Testimonial from AutoTrader)_ We have an Ops "squad buddy" for each Dev squad, a person from Ops who regularly works with specific Dev squads, attending their standups and providing the "glue" between dev and ops.

**pg 100:** Organizations that optimize for a safe and rapid flow of change tend to use mixed-discipline or cross-functional teams aligned to the flow of change -- what we call stream-aligned teams. Sometimes a particular area is so complicated that a dedicated complicated-subsystem team is needed. _**But such teams never sit in the flow of change; instead, they provide services to stream-aligned teams.**_ Work is never handed off to another team for a later stage in the flow.

### Converting Common Team Types to the Fundamental Team Topologies
**pg 107:** For organizations that are successful at delivering software rapidly and safely, most teams are stream aligned, wiht only around one in seven to one in ten teams not stream aligned. That is... the radio of stream-aligned teams to other kinds of teams should be between about 6:1 and 9:1.

**pg 109:** The most effective pattern for an architecture team is as a part-time enabling team.

## Chapter 6
**pg 111:** Flow is difficult to achieve when each team depends on a complicated web of interactions with many other teams. For a fast flow of change to software systems, we need to remove hand-offs and align most teams to the main streams of change within the organization. However, many organizations experience huge problems with the responsibility boundaries assigned to teams. Typically, little thought is given to the viability of the boundaries for teams, resulting in a lack of ownership, disengagement, and a glacially slow rate of delivery.

### On Fracture Planes
**pg 117:** **Change Cadence.** Another natural fracture plane is where different parts of the system need to change at different frequencies. 
Splitting off the parts of the system that typically change at different speeds allows them to change more quickly.

## Chapter 7: Team Interaction Modes
**pg 131:** [S]imply arranging teams into patterns is not enough for high effectiveness; it is also necessary to identify how these teams interact and when to change the teams and their interactions.

**pg 132:** In many organizations, poorly define team interactions and responsibilities are a source of friction and ineffectiveness. A team may have been told it is autonomous and self-organizing, but team members find they have to interact with many other teams in order to complete their work; and this feels frustrating.

When considering the relationship between any teams, a key decision is whether to collaborate with another team to achieve an objective or to treat the other team as providing a service.

**pg 133:** Intermittent collaboration gives the best results... Groups whose members interacted only intermittently... had an average quality of solution that was nearly identical to those groups that interacted constantly, yet they preserved enough variation to find some of the best solutions too. Intermittent collaboration found better solutions than constant interaction.

**pg 133:** The three essential ways that teams can interact:
- **Collaboration:** working closely with another team
- **X-as-a-Service:** consuming or providing something with minimal collaboration
- **Facilitating:** helping (or being helped by) another team to clear impediments

**pg 134** establishes visual diagram semantics

### on Collaboration
**pg 136:** During early phases of new systems development, and during periods where there is a need to quickly discover new information, technology limitations, and suitable practices, the collaboration mode is highly valuable. This is because team topologies that use collaboration can rapidly uncover new ways of working and unexpected behaviors of technologies.

**pg 137:** A team should use collaboration mode with, at most, one other team at a time.

### On X-as-a-Service
**pg 138:** During later phases of systems development and periods where predictable delivery is needed (rather than discovery of new approaches), the X-as-a-Service model works best. In this model, teams can rely on certain aspects of their technology landscape being provided as a service by other teams (internal or external), allowing the team to focus on delivering their work.

### on Facilitating
**pg 140:** The facilitating team interaction mode is suited to situations where one or more teams would benefit from the active help of another team facilitating (or coaching) some aspect of their work. The facilitating interaction mode is the main operating mode of an enabling team.

Teams that interact using the facilitating mode typically work across many other teams, detecting and reducing cross-team problems and heping to inform the direction and capabilities of things like code libraries, APIs, and platforms provided as a service by other teams or organizations.

**pg 141:** For example, a team facilitating the effectiveness of three stream-aligned teams might find that the logging service provided by the platform is quite difficult to configure: all three teams find it difficult to use. The team helping the three teams can then facilitate some improvements to the logging service from the platform.

## Chapter 8
**pg 155:** To reach the level of a high-performing organization, it is important to decide how much collaboration is appropriate for each team-to-team interaction. Should Team A simply be able to consume services from Team B with little effort? If they should but cannot yet, should Team A collaborate with Team B for a short time (Three weeks? Three months?) in order to better define the API for Team B and enable Team A to consume it "as a service"? Exactly what should the teams collaborate on, bearing in mind that the collaboration will likely tend to blur the boundaries of each part of the system between Team A and Team B?





