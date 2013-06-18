## 5. Main work of the project

### Goal Formulation and Mid-term Pitch
Based on the preliminary results of the background analysis, we were able to identify the following issue of Neo4j:
External developers have difficulty contributing to the Neo4j project due to 
* (i) lack of transparency over the internal development process.
* (ii) lack of understanding over the build process and the organization of the source code.

Therefore we formulated our goal for this project as "helping external developers understand the development process".
During the [mid-term pitch](presentation/pitch/index.html), we have presented the identified issues and our project goal.

### Goal, Questions and Metrics approach
The Goal of the [GQM assignment](Metrics.md) is to improve the succeeding rate of the contribution process of the Neo4j community.
We raises 3 questions and for each questions 2 metrics to test the validity of the statement 
"external developers have difficulty contributing to the Neo4j project".

### Context Viewpoint
[Context Viewpoint](ContextView.md) describes the key requirements of the system and
the dependencies of the system to other external entities. 
This viewpoint gives the external developer the high level overview of the system.
  
### Development Viewpoint
The context viewpoint is useful, but it does not provide sufficient support to the external developers.
The most important contributions of our project can be found in the [Development Viewpoint](DevelopmentView.md).
We are planning to integrate the Repository Structure, the Build Guides and the Vagrant build automation workflow 
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
However, the build instructions is currently separated into multiple documents or even missing.
Therefore a [build guide](build.txt) is created, which serves as a technical manual describing the existing build process.

#### Vagrant build automation workflow ~~Don't know what I am saying. ask Hans~~
the developer needs to verify all common build scenarios every time the code is updated.
There are still infinite amount of unknown reason why certain build fails on the some of the developer's machine.

Therefore we formulate the [Vagrant build automation workflow](where).
Vagrant can be used to automatically create multiple disposable, consistent environments,
where the source code can be built can tested.
This approach not only speeds up the process of verifying build scenarios, more importantly,
external developers should be able to *reproduce* the result of an explicitly documented build scenario.

#### Internal Development Process (Planned)
Our team has tried our best to schedule an interview with the internal developers for their insight in internal development process.
We have sent the core developer an email.
We have tweeted the internal developers.
We even made an pull request to the Neo4j Repository. But there were no positive response.

What would have been the results from this interview are 
for example their internal decision-making workflow and their roadmap.

### Final Presentation
We have presented our final results at the [final presentation](presentation/final/index.html). 
During the presentation, we have discussed the high level architecture of Neo4j, explained our project goal 
and presented our contributions to the Neo4j project.

## 6. Conclusion
After conducting the background analysis, 
our project team is able to gain an [initial understanding](Sketches.md) of Neo4j
and the [stakeholders](Stakeholders.md) involved.

The preliminary results of the background analysis shows that 
external developers have difficulty contributing to the Neo4j project due to 
(i) the lack of understanding over the build process and the source code organization
(ii) the lack of transparency over the internal design process.
The validity of the main issue is tested and verified using [GQM approach](Metrics.md).

Our goal is to help external developers understand the development process, 
therefore, besides the [Context Viewpoint](ContextView.md), we also created the [Development Viewpoint](DevelopmentView.md) 
for the purpose of providing an detailed elaboration about the development process.

Finally, our main contributions to the Neo4j project are:
* [Repository Structure](DevelopmentView.md#module-structure-model)
* [Build Guide](build.txt)
* [Vagrant build automation workflow](where)
These documents should be integrated into the [contributing section of the Neo4j manual](http://docs.neo4j.org/chunked/milestone/community-contributing.html).
