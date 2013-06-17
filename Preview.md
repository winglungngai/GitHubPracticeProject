## 7. Literature Concepts & Architectural Reflections
This section will give a quick introduction to some basic concepts from the literature used for this course 
and our reflection on the architectural theories after we applied them to our project.
First we will discuss the concepts of views, viewpoints, perspectives as introduced by the Software Systems Architecture book.
Then we will discuss the four different types of architectural sketches presented by [Andre van der Hoek](http://www.ics.uci.edu/~andre/) during the lectures.
Finally we discuss the Goal Question Metric approach as introduced by [Basili et al.](http://fub-taslim.googlecode.com/svn/trunk/WEMSE/INSTICC_Conference_Latex/gqm.pdf).

### Rozanski and Woods
The book Software Systems Architecture by Rozanski and Woods is used as the theoritical foundations for our project.
Most chapters of the book described a formal, heavy-weighted approach,
which guides software architects to construct complete architectural documentation for the software system they are going to build.
This approach is most applicable during the initial phase of the software project, and the stakholders are expected to participate actively.

However, we found this approach not applicable for our project. 
First of all, we are evaluating an existing software system, not building one.
Second, we are not in the position to ask for very high commitment of time and resources from the stakeholders,
as they are not likely to understand why the investment is worth it.

Rozanski and Woods suggests another light-weighted approach, Tiny Architectural Review Approach (TARA) in 
Chapter 14 Evaluating the Architecture, Validating the Architecture of an Existing System.
Note that TARA approach is very flexible, as the authors stated that they never used TARA the same way twice.
The main idea is to first identify the goals and the target audience, 
then focus only on the system aspects that are related to the goals, 
and finally give recommendations that are tailoring to the needs and desires of the target audience.


#### Stakeholders
According to Rozanski and Woods, stakeholders are those who have an interest in the realization of the system.
Each of the stakeholders have their own concerns about the system, 
and meeting the needs of the stakeholders is why the system is being created in the first place.

In our opinion, a stakeholder analysis is indeed essential for our project.
However, we are not able to follow the approach completely.
The original purpose of conducting a stakeholder analysis is 
to identify all classes of stakeholders (or at least their representatives)
which allows the archtiects to discuss with stakeholders about the architectural design, 
and to resolve conflicts of interests.
Altrough we have identified most of the stakeholder classes, 
unfortunately it is not possible to establish a proper communication channel 
with the most prominant stakeholder - Neo Technology. 
Without direct interaction with most of the stakeholder class, it defeats the purpose.

So we have taken a different approach: using the stakeholder analysis to 
identify the stakeholder whose needs are the most ignored, which turns out to be the external developers
Based on the stakeholder analysis, we made a decision to focus on our target stakeholder group  - the external developers, 
and help them by creating relevant architectural documents that are missing.

#### View & Viewpoints
A document describing how (part of) the system works 
and how it meets some of the concerns of its stakeholders, is called a View.
Rozanski and Woods grouped related concerns together into Viewpoints.
Each Viewpoint is basically a collection of concerns and is described by one or more Views.
Together, these Views should document the system to such an extent,
that all concerns of the Viewpoint are discussed.

For our project, we created a Context View, adhering to the Context Viewpoint.

We also created several Development Views, which partly cover the Development Viewpoint.

#### Perspective
The last important concept of the book is the Perspective.
A Perspective is related to quality properties (like security or performance) of the system.
Perspectives are applied to Views to make sure you take these quality properties into account.
For example, the Security Perspective was applied to our Context View to identify the places where the system is possibly vulnerable.

### Four types of design sketches
Andre van der Hoek of the university of California presented four types of design during one of the course's lectures.
When designing software, or when trying to understand a system's design,
these four types can help ensure that you don't miss parts of the system.

The identified design types are:
- Application design  
  This covers what the system should do.
  Note that this covers not only functional requirements,
  but also quality properties (like responsiveness)
- Interaction design  
  Describes how one interacts with the system.
  There may be many stakeholders who have to interact with the system.
  The user is the most obvious one, but the developers, 
  tester and maintainers have to interact with the system too.
- Architecture design  
  Architecture design describes what the conceptual core of the system is, 
  and how it is structured.
- Implementation design  
  This type of design is concerned with implementation details of the system.

### The Goal Question Metric (GQM) approach
The Goal Question Metric approach by Basili et al. describes a way to handle software metrics for measurement within a project.
The paper claims a top-down approach,
working downwards from a goal to find the metrics to measure,
is the right way of defining measurement procedures.

First, a goal should be formulated.
The goal should be specific enough so that it can actually be verified if it was met.
The GQM requires the goal to focus on a specific *quality issue* of some *object* of the system (a Product, Process or Resource), from a specific point of view.

So a goal should have four properties, which we can illustrate with the following example goal:
* Purpose: To improve
* Quality Issue: the timeliness
* Object: of change request processing
* Viewpoint: from the project manager's viewpoint.

Note that viewpoint here does not refer to the Viewpoint as defined by Rozanski and Woods.

When the goal is formulated, it should be refined into a series of questions.
Each question should try to characterize the object of the goal with respect to the selected quality issue and to determine its quality from the selected viewpoint.
So a question should try to determine the value of some quality property of the object.
This value has to take the viewpoint defined in the goal into account.

An example question for the previous example goal could be:
"What is the current change request processing speed?"  
The answer to this question will determine the speed (quality property related to timeliness) of the change request processing (the object of the goal).

Finally, metrics should be identified for each question.
These metrics can be measured and used to answer the question.
When doing this, keep in mind that the metric has to take the viewpoint of the goal into account.
For objective metrics like code size, this is not an issue.
However, for subjective measures like readability, 
the metrics have to be measured according to the correct viewpoint.

An example of an objective metric for the previous example question could be
the average cycle time.
