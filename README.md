# SA-Workbench
Collaborative Software Architecting with an Extensible Web-based Workbench
The main contribution of this work is the development of a prototype of a Computer-Aided Software Engineering (CASE) host environment supporting a variety of software architecture related work activities which could be used as a proof that a collaborative, extensible, and customisable web-based tools could improve the productivity and enhance the capabilities of the software architects.


**Software architecture - development methodology**

We compared two different software architecture development methodologies, namely the developed by the Software Engineering Institute (SEI) of Carnegie Mellon University Attribute Driven-Design (ADD) and the suggested by Microsoft technique for architecture and design. All of the applications requirements were defined before the start of the software architecture design and it was identified that changes to the requirements during development of the software architecture design were not expected. For this reason, we selected the Attribute Driven-Design method for development of software architecture design. Subsequently we identified, categorised, and rated the requirements of the proposed system in accordance with the Attribute Driven-Design (ADD) method for development of software architecture design and documentation.
We selected the set of views proposed by Philippe Kruchten in their work called “Architectural Blueprints - The ‘4+1’ View Model of Software Architecture”, namely Logical, Process, Physical, Development views and Scenarios to illustrate the resulting from the ADD process architectural design of the SA Workbench software.


**Architectural styles used:**

-	3-Tier client-server
-	component-based
-	publisher-subscriber messaging pattern
-	blackboard pattern


**Support for collaboration **

The requirement that the workbench should support collaborative work translates into the requirement that the physical machines, where instances of the workbench reside, should be able to communicate with each other. There is a number of architectural styles which satisfy this requirement such as peer-to-peer, master-slave, and client-server architectural styles. The master-slave architectural style suggests that there would be a master machine controlling the communication between the nodes participating in the system. This, however, was not acceptable for the designed system since the system required all nodes to be able to initiate the communication. The client-server architectural style has been identified as more appropriate for the needs of this project than the peer-to-peer architectural style due to its advantages related to ease of maintenance, higher security, and centralised data access. We have selected the 3-Tier client-server architectural style since it overcomes some of the disadvantages of the traditional 2-Tier style related to extensibility, scal ability, and reliability.


**Extensibility and Reusability**

In order to address the requirements for extensibility and reusability we have incorporated the component-based architectural style into our architectural design. The component-based architectural style focuses on decomposition of the design into individual functional or logical components which provide interfaces for communication. This architectural style uses components that are encapsulated, independent and not context specific which allows them to be reusable, replaceable, and extensible. Additional benefits of the incorporation of this style are that it mitigates technical complexity which leads to decrease of development effort and reduction of costs.

The required functionalities for collaborative work are provided via chat and notification services. Both services have server and client-side parts and share the same architectural design. The architectural design selected is a combination of the publisher-subscriber messaging pattern and the blackboard pattern. In this pattern, the publishers do not need to know about the subscribers which results in design with loose coupling between the participating objects which improves the flexibility and scalability of the system. Blackboard is a data-centred architectural pattern which is applicable in situations where multiple users work on the same problem. This pattern allows multiple independent programs, also called “knowledge sources”, to communicate exclusively through a shared global data repository known as blackboard.

Additionally, we use the Open Close, Dependency Inversion, and Single Responsibility software design principles to achieve the extensibility of the system and reusability of its components.


**Conclusion** 

It is worth mentioning that there are many more methodologies for development of software architecture design neither of which being better of worst. The degree of applicability of the different methodologies depends on a great number of factors including software development methodology, the application domain and purpose, and preferences and experience of the software architecture stakeholders. For example, a business application would benefit more from agile software development process and architectural design process, avoiding the big up-front design, such as the one suggested by Microsoft since the business environment is changing at rapid rates and the users find new strategies and form new requirements as they use the application. On the other hand, a mission critical system such as an air traffic control system would benefit more from planned software development and detailed up frond software architecture design such as the one provided by ADD. ADD might take many iterations and time before the actual software development commences but it allows the designers to identify the quality attribute trade-offs at the early design stages and leads to architectural design which satisfies both the quality and functional requirements of the system. 




