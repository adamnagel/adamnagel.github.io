---
title: "Team Toplogies: Reading Notes"
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

# Chapter 5
**pg 80:** [M]ultiple stream-aligned teams are the starting point... but an organization may also have several platform teams, a few enabling teams for different purposes (perhaps one addressing CI/CD and a second addressing infrastructure or architecture), and... one or two complicated-subsystem teams.

## On Stream-Aligned Teams
**pg 85:** What kinds of behaviors do we expect to see in an effective stream-aligned team? _(selected subset)_
- minimal (ideally zero) hand-offs of work to other teams.
- proactively adn regularly reaches out to the supporting fundamental-topologies teams (complicated subsystem, enabling, and platform)

## On Enabling Teams
**pg 86:** An enabling team is composed of specialists in a given technical (or product) domain, and they help bridge this capability gap. Such teams cross-cut to the stream-aligned teams and have the required bandwidth to research, try out options, and a make informed suggestions on adequate tooling, practices, frameworks, and any of the ecosystem choices around the application stack.

Enabling teams have a strongly collaborative nature; they thrive to understand the problems and shortcomings of steam-aligned taems in order to provide effective guidance. Jetta Eckstein calls them "Technical Consulting Teams"... provid[ing] guidance, not execution...

Enabling teams actively avoid becoming "ivory towers" of knowledge, dictating technical choices for other teams to follow, while helping teams to understand and comply with organization-wide technology constraints.

The end goal of an enabling team is to increase the autonomy of stream-aligned teams by growing their capabilities with a focus on their problems first, not the solutions per se. If an enabling team does its job well, the team... should no longer need the help... after a few weeks or months; there should not be a permanent dependency on the enabling team.

Knowledge transfer between an enabling and a stream-aligned team can take shape on a temporary basis or on a long-term basis. Pairing can be quite effective for some types of practices...

**pg 87:** What kinds of behaviors and outcomes do we expect to see in an effective enabling team? _(selected subset)_
- proactively seeks to understand the needs of stream-aligned teams, establishing regular checkpoints and jointly agreeing when more collaboration is needed.
- stays ahead of the curve in keeping abreast of new approaches, tooling, and practices in their area of expertise, well before an actual need is expected from steam-aligned teams.
- promotes learning not only inside the enabling team but across stream-aligned teams, acting as a curator that facilitates appropriate knowledge sharing inside the organization.






