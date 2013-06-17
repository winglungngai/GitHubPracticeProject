## 5. Main work of the project

Based on these observations, we were able to identify the following issue of Neo4j:
External developers have difficulty contributing to the Neo4j project due to 
* (i) lack of transparency over the internal developement process.
* (ii) lack of understanding over the build process and the organization of the source code.

And we formulated our goal for this project as "helping external developers understand the development process".

After we formulated the goal of our project, we are 
 - results
  - pitch - formulates the goal of our project (mention the issues that resulted in our goal and the lacking contribution sectio nof the manual)
  - gqm - provides a way to measure success of the project
  -[Context View](ContextView.md)
  - Neo4j repo + build guides
  - interview
 - interview results + repo + build guides can be integrated in the 'contributing' section of the manual (i.e. our main contribution)
 - interviewing core developer from Neo4j for their insight in internal development process.

## 6. Conclusion
 - issue, goal, solution
 - neo4j should use our cool development views

After investigating several information sources as stated in the main activities, 
our project team is able to gain better insight over the basic architecture of Neo4j([Chapter2](Sketches.md))
and the stakeholders([Chapter 3](Stakeholders.md)) involved.

The main issue we have identified([Chapter4](MainIssue.md)) can be formulated as follow: 
External developers have difficulty contributing to the Neo4j project due to 
(i) lack of understanding over the source code in the repository and 
(ii) lack of transparency over the internal design process. ~~(TODO: help need better formulation of the main issue?)~~ 
The validity of the main issue is tested and verified using GQM approach([Chapter 5](Metrics.md)).

Our goal is to help external developers understand the development process ~~(TODO: help need better formulation of the main issue?)~~, 
therefore the context view([Chapter 6](ContextView.md)) is created to describe 
the interaction between the Neo4j server and other external entities ~~(TODO: is this reason valid?)~~. 
More importantly, the development view([Chapter 7](DevelopmentView.md)) is created to describe 
the stucture and the organisation of the source code in the repository. ~~(TODO: is this reason valid?)~~ 
In addition, an extra decision-making flow view/model/scenario~~(TODO: what should it be exactly?)~~ is added to the set of architecture documents. 
The decision-making (model) contains the decision-making process and the decisions made in the past and the project planning in the future.~~(TODO: too ambitious?)~~

Finally, we would like to make contribution ourself to the Neo4j project. 
Based on the architecture documents, we have written/improved ~~(TODO: what should it be exactly?)~~ 
several Quick Start/Manaul of Neo4j, which is meant for external developers to quickly understand and work with the source code of Neo4j.
