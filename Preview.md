## 5. Main work of the project

### Goal Formulation and Mid-term Pitch
Based on the preliminary results of the background analysis, we were able to identify the following issue of Neo4j:
External developers have difficulty contributing to the Neo4j project due to 
* (i) lack of transparency over the internal developement process.
* (ii) lack of understanding over the build process and the organization of the source code.

Therefore we formulated our goal for this project as "helping external developers understand the development process".
During the [mid-term pitch](presentation/pitch/index.html), we have presented the identified issues and our project goal.

### Goal, Questions and Metrics approach
The Goal of the [GQM assignment](Metrics.md) is to improve the succeeding rate of the contribution process of the Neo4j community.
We raises 3 questions and for each questions 2 metrics to test the validity of the statement 
"external developers have difficulty contributing to the Neo4j project".

### Context Viewpoint
[Context Viewpoint](ContextView.md) decribes the key requirements of the system and
the dependencies of the system to other external entities. 
This viewpoint gives the external developer the high level overview of the system.
  
### Development Viewpoint
The context viewpoint is useful, but it does not provide sufficient support to the external developers.
The most important contributions of our project can be found in the [Development Viewpoint](DevelopmentView.md).
We are planning to integrate the Repository Stucture, the Build Guides and the Vagrant build automation workflow 
into the [contributing section of the Neo4j manual](http://docs.neo4j.org/chunked/milestone/community-contributing.html).

#### Repository Structure/Module Structure Model
At this moment, the organization of the source code in the repository is not explained at all.
External developers need to waste a lot of time just try to get an initial understanding the codebase.
Therefore one of our contribution is to document the [repository structure](DevelopmentView.md#module-structure-model).
The repository structure contains an overview of the modules, a brief description of each module and
how they are interconnected to each other.

#### Build Guides
Difference in configuration/settings, such as the choice of the operating systems and the version of JDK, can results in build failures.
The difficulty of the build process can greatly affect the choice of the external developers whether they want to start working on this project.
As an example, our course instructor advised us to choose an open source project which can be built, as many project has serious build issues.
However, the build instructions is currently seperated into multiple documetns or even missing.
herefore a [build guide](build.txt) is created, which serves as a technical manual describing the existing build process.

#### Vagrant build automation workflow ~~Don't know what I am saying. ask Hans~~
the developer needs to verify all common build scenarios every time the code is updated.
There are still infinite amount of unknown reason why certain build fails on the some of the developer's machine.

Therefore we formulate the [Vagrant build automation workflow](where).
Vagrant can be used to automatically create multiple disposable, consistent environments,
where the source code can be built can tested.
This appoarch not only speeds up the process of verifying build scenarios, more importantly,
external developers should be able to *reproduce* the result of an explicietly documented build scenario.

#### Internal Development Process (Planned)
Our team has tried our best to schedule an interview with the internal developers for their insight in internal development process.
We have sent the core developer an email.
We have tweeted the internal developers.
We even made an pull request to the Neo4j Repository. But there were no positive response.

What would have been the results from this interview are 
for example their internal decisiion-making workflow and their roadmap.

### Final Presenation
We have presented our final results at the [final presentation](presentation/final/index.html). 
During the presenation, we have discussed the high level architecture of Neo4j, xplained our project goal 
and presented our contributions to the Neo4j project.

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
