# haskell-salesforce-transaction-analyzer
Analyze the code which runs in a Salesforce transaction. Goals: find performance bottlenecks and assist with optimizations.

## Motivation

### About Salesforce

A company's IT team loves Salesforce because it provides software tools and abstractions which shortens the time required for building a software system which fulfills the needs of its users. From a high level, the Salesforce development platform consists of a relational database with an automatically-generated default web interface for each of creating, viewing, editing, and deleting records, along with all other niceties a user would expect of a data platform like this.

### Customizing Salesforce

When an organization initially adopts Salesforce, it's common for a single team to use it for a simple thing, like representing a record's process through multiple stages, represented by a picklist field on that record. Once having Salesforce to extend their team's ability to define, refine, and manage their business' complexity, the team is encouraged to increase their reliance on Salesforce. Over time, however, they add more data validation and business processes to their Salesforce org, so their org's complexity grows more complex over time.

### System Knowledge

Because each change added to the system is unlikely to be passed through a single gatekeeper or, moreover, a gatekeeper concerned with ensuring the maintainability and performance of the system. Even if there was a knowledgable person like that acting as the owner of the system, understanding the performance and maintenance implications of any one change is only feasible for a person who has deeply considered the theory of software and systems. People who care about this kind of knowledge are likely few and far between. Therefore, it's easy to see how useful it would be to encode this knowledge into a tool, which makes it easier for newcomers to understand and apply this knowledge.
