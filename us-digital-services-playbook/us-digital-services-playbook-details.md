#U.S. Digital Services Playbook 
Per the RFI, we followed all of the applicable playbook plays for the prototype. 

## Play 1: Understand what people need
**Checklist** |**What we did**
:------------- |:-------------
Early in the project, spend time with current and prospective users of the service  | We met with users that represented the initial anticipated audience types based on the high level requirements in the RFI, including Taborda staff that are not involved with the project (as simulated users), and one actual Child Protective Services case worker.
Use a range of qualitative and quantitative research methods to determine people’s goals, needs, and behaviors; be thoughtful about the time spent |	Our user researcher met with our user groups and elicited information about their preferences, habits, expectations for easy-to-use systems, and their preconceptions about the processes related to child protective cases. The user researcher used this information to identify target audiences and their goals/needs/behaviors. *(2c)*
Test prototypes of solutions with real people, in the field if possible |	Our user researcher facilitated a walkthrough of an early wireframe prototype to get feedback 
Document the findings about user goals, needs, behaviors, and preferences |	During our human centered design phase for ideation, we conducted 1:1 and group workshops with target user groups and gathered feedback on their goals, needs, preferences and behaviors.
**Key Questions** |**Answers**
Who are your primary users?	| Parents interacting with Child Protective Services (CPS)


## Play 2: Address the whole experience, from start to finish
**Checklist** |**What we did**
:------------- |:-------------
Understand the different points at which people will interact with the service – both online and in person |	We received input from our user test group, primarily the actual case worker, regarding how parents interact with CPS -- both online and in person. *(2c)*
**Key Questions** |**Answers**
What are the different ways (both online and offline) that people currently accomplish the task the digital service is designed to help with? | Telephone; in-person (scheduled and unscheduled)

## Play 3: Make it simple and intuitive
**Checklist** |**What we did**
:------------- |:-------------
Use a simple and flexible design style guide for the service. Use the U.S. Web Design Standards as a default | 	We implemented a simple, responsive and accessible online Design Style Guide (DSG) using bootstrap, html, sass and css. As the style and layouts evolved through the iterations and feedback loops with users, the guide was automatically updated. *(2e)*
**Key Questions** |**Answers**
What primary tasks are the user trying to accomplish? | Create and manage their profile; View residential facilities in their ZIP code; Communicate with case workers via secure messaging system (inbox,outbox)


## Play 4: Build the service using agile and iterative practices
**Checklist** |**What we did**
:------------- |:-------------
Ship a functioning “minimum viable product” (MVP) that solves a core user need as soon as possible, no longer than three months from the beginning of the project, using a “beta” or “test” period if needed	 | We focused on the MVP and placed the remaining stories in the icebox (low-priority backlog)
Run usability tests frequently to see how well the service works and identify improvements that should be made	| We incorporated usability tests frequently at each sprint review and often mid-sprint with users. *(2f)*
**Key Questions** |**Answers**
How long does it take for a production deployment? | Our automated continuous integration pipeline (Jenkins / Docker) completes a build/deploy cycle within minutes.

## Play 5: Structure budgets and contracts to support delivery
**Key Questions** |**Answers**
:------------- |:-------------
What is the scope of the project? What are the key deliverables? | 3 weeks; Working prototype meeting feature requirements; Follow RFI technical approach requirements

## Play 6: Assign one leader and hold that person accountable
**Checklist** |**What we did**
:------------- |:-------------
A product owner has been identified | Brendan McGuire was identified as the product owner
The product owner has a product management background with technical experience to assess alternatives and weigh tradeoffs | Brendan has over 16 years of technical and product management experience implementing and managing product development engagements.
**Key Questions** |**Answers**
Who is the product owner?	| Brendan McGuire

## Play 7: Bring in experienced teams *(2b)*
**Checklist** |**What we did**
:------------- |:-------------
Member(s) of the team have experience building popular, high-traffic digital services | Most of our team members have been implementing high-traffic and mission-critical digital services

## Play 8: Choose a modern technology stack
**Checklist** |**What we did**
:------------- |:-------------
Choose software frameworks that are commonly used by private-sector companies creating similar services	| We selected modern open source frameworks and tools.  *(2i)* 
Whenever possible, ensure that software can be deployed on a variety of commodity hardware types| Our prototype is deployed in Docker - it will deploy the same on a variety of hardware platforms. The UI was developed and tested to work on multipe devices using a responsive design. *(2h)* 
**Key Questions** |**Answers**
What is your development stack and why did you choose it? | Our stack is: Bootstrap, Javascript, Angular, jQuery, SASS, Font-awesome, JAWT, Guava, Gulp, WAVE, NGINX, Java, Dropwizard, Jetty, Jersey, Jackson, Hibernate ORM, Gradle, Flyway, PostgreSQL, GitHub, Jenkins, Docker, Protractor, Jasmine, Junit 4, and Mockito.
Which databases are you using and why did you choose them? | PostgreSQL

## Play 9: Deploy in a flexible hosting environment
We deployed to Amazon Web Services (AWS), which supports all of these aspects.  *(2j)*
**Checklist** |**What we did**
:------------- |:-------------
Resources are provisioned on demand | AWS
Resources scale based on real-time user demand | AWS 
Resources are provisioned through an API | AWS
**Key Questions** |**Answers**
Where is your service hosted? | Amazon Web Services (AWS)

## Play 10: Automate testing and deployments 
**Checklist** |**What we did**
:------------- |:-------------
Create automated tests that verify all user-facing functionality | We used Test Driven Development (TDD) techniques that include unit tests in the automated build process. *(2k)*
**Key Questions** |**Answers**
What percentage of the code base is covered by automated tests? | ???
How long does it take to build, test, and deploy a typical bug fix? | Minutes
How long does it take to build, test, and deploy a new feature into production?| 1 sprint
How frequently are builds created?	Each commit; Many times each day | Many times each day
What test tools are used?	| Protractor; Jasmine; Junit 4; Mockito; WAVE
Which deployment automation or continuous integration tools are used? | Jenkins; Docker
What is the estimated maximum number of concurrent users who will want to use the system| Targeting 200 for prototype purposes

## Play 11: Manage security and privacy through reusable processes
**Checklist** |**What we did**
:------------- |:-------------
“Pre-certify” the hosting infrastructure used for the project using FedRAMP | AWS is FedRAMP certified. *(2j)*
**Key Questions** |**Answers**
Does the service collect personal information from the user? How is the user notified of this collection? |	Yes: Name and Email for registration purposes; Web form 
Does it collect more information than necessary? Could the data be used in ways an average user wouldn't expect?	| No; No
How does a user access, correct, delete, or remove personal information? | Web page to manage profile
Will any of the personal information stored in the system be shared with other services, people, or partners? | No

## Play 12: Use data to drive decisions 
**Checklist** |**What we did**
:------------- |:-------------
Monitor system-level resource utilization in real time | We employ Datadog and Pagerduty to provide real-time monitoring. *(2n)*
**Key Questions** |**Answers**
How does your team receive automated alerts when incidents occur? | Datadog sends automated alerts as needed

## Play 13: Default to open
**Checklist** |**What we did**
:------------- |:-------------
Ensure that data from the service is explicitly in the public domain, and that rights are waived globally via an international public domain dedication, such as the “Creative Commons Zero” waiver | Data from our prototype is not proprietary.
Ensure that we maintain the rights to all data developed by third parties in a manner that is releasable and reusable at no cost to the public | The State owns all software developed by Taborda as part of this prototype.
When appropriate, publish source code of projects or components online | The source code and artifacts are provided in GitHub.
**Key Questions** |**Answers**
How are you collecting user feedback for bugs and issues? | We included a feedback link/page in mockups. To be implmented in future sprint(s)