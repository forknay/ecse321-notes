# Chapter 3 : Agile Software Development
*Last time: Plan-driven development*

- Activities all planned in advance
- Progress measured against plan

However, businesses operate in a constantly changing environment.
- Requirements are always changing!
- It is impossible to derive a complete set of requirements @ beginning of a project
- As a requirements change, design also must change!

Moreover, businesses want to develop and deliver software quickly.

**Agile methods** are designed to release software quickly.
(Type of software process)

All agile methods share 3 common characteristics.

1. Specification, design, implementation are **interleaved**.
    - Design documentation is minimized (expensive)
2. System is developed incrementally. **Stakeholders** give feedback
(Clients buying software, users of system)
3. The development process is supported by **tools** (automation and ease of use/integration of components.)

## 3.1 Agile manifesto
The philosophy behind agile methods is reflected in the **agile manifesto** (2001), which states:
1. Individuals + interaction >> processes and tools
    - Building projects around people!
    - Trust them to get the job done
    - Prioritize face to face communication (faster)
2. Working software >> Comprehensive documentation
    - Primary measure of progress is Software
    - Deliver Minimum Viable Product (MVP) quickly, then improve it
    - Keep it simple, keep the customer happy
3. Customer collaboration >> Contract negotiation
    - Team members (including customers) must work together!
    - Daily interactions
    - Frequent delivery
4. Responding to change >> following a plan
    - Changing requirements are welcome!
    - Team regularly reflects on how to become more efficient/effective

## 3.3 Agile Project Management (SCRUM)
Scrum was developed in 2001 as a framework for organizing agile projects

The process:
    - Reqs are translated into tasks
    - Tasks are grouped in a Product Backlog
    - For every increment (short period of time), a set vof tasks are selected from the PB and implemented by the team

Scrum uss a unique terminology to define people, events, and artifacts.

1. People
    - Developers: Create and implement tasks
    - Product owner:
        - Customer or PM
        - Identify features, modifications
        - Update the PB
        - Have a long-term vision for the product.
2. Artifacts
    - Backlog
        - List of outstanding tasks to be completed
        - Tasks can be added (usually not removed)
        - Ordered by priority
        - Types of tasks
            - User story
            - Other (e.g Refactoring)
    - User Story
        - Requirement written in customer's language
        - Written from customer POV
        - Not necessarily written by customer
        - "As a `<type of user>`, I would like to `<feature>` so that `<rationale>`"
        - "As a course instructor, I would like to add content to a course so that the enrolled students can access it on demand".
    - Epic
        - Set of related user stories that relate to a feature of the system
        - e.g "Content" epic
            - Instructor uploading material
            - Student accessing material
3. ScrumMaster
    - Ensure that the scrum process is followed
    - "Coach" the development team
    - Accountable for team's effectiveness
4. Events
    - Release (ie: version 2, version 3)
        - Set of features acting as long-term goal
        - Endpoint : new software version
    - Sprint (increment)
        - Short-term development plan
        - 1-4 weeks (usually 2 weeks)

How are sprints organized?
- Sprint planning
    - Select tasks from Product Backlog and add them to Sprint Backlog
    - Distribute tasks among developers
- Daily Scrum: "Stand-up" meeting (~15 min)
    - All members share progress, their plan for the day, and any roadblocks
- Sprint review
    - Inspect sprint outcome
    - Stakeholder feedback
- Sprint Retrospective
    - Reviewing problems
    - Identifying areas for improvement

How can we estimate accurately the number of tasks to add to the sprint backlog?
- Look at previous output
- Associate a unit of "effort" to each task
- During sprint planning, every story/task is given a number of **story points** (effort estimation)
- The **velocity** of a team is the average number of story points the team can complete in a sprint