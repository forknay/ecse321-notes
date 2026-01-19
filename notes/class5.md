# Class 5

## A good requirement

### "The online booking system shall allow the user to access search results for available rooms in less than 2 seconds"

* "online booking system" -> system
* "shall" -> need a verb (shall, may, etc)
* "to access search results for available rooms" -> positive end result
* "less than 2 seconds" -> quality criteria (may not be there for functional requirements)

## 4.2 Requirements Engineering Process

### 3 key activities
1. Requirement elicitation: derive system descriptions through discussions with users.
2. Requirement specification: write our user + system requirements
3. Requirement validation: check that requirements are realistic, consistent, complete

## 4.3 Requirements elicitation

* Research + Discover the requirements of system from user, stakeholder, etc
* Difficult process -> why?
    * Stakeholders don't always know exactly what they want
        * They struggle to express it
    * Stakeholders have implicit knowledge that they might omit to share
    * Some stakeholders might have conflicting requirements

#### Some elicitation techniques:
* Interviewing stakeholders
    * pre-written questions (closed) or not (open)
    * difficult to be specific without prototype (model)
* Ethnography
    * How people use an old system
    * How they interact in a company
    * Not always best for innovation

#### Output of elicitation Stories + Scenarios
##### Story (!= agile user story!)
- Narrative text with high-level description

##### Scenario
- More structured, describes a flow of events with the system state @ every step

## 4.4 Requirements specification
-> Writing down all requirements in a software requirements document
- Natual language
- Structured specifications
- Graphical model

### 4.4.1 Natural Language
-> Each requirement is a user (func) or system (N.F) requirement

-> Each requirement has an ID

-> Standardized sentence format
- FR1: The system shall display available rooms
- FR2: ...
- NFR1: ...
- NFR2: ...

### 4.4.2 Structured specification
- For system requirements
- Natural language following a template (less ambiguous)
- You don't have to do it for every single requirement (use your judgment)

### 4.4.3 Use cases
- Show interactions between user and system
- Uses graphical model (use case Diagram) and structured text (use case specification)
- A use case is a top-level service provided by system to its actors
    - ie: Consult available rooms -> Actor : Customer (human)
    - Save booking information -> Database (subsystem)

Use case diagram
-> Show what each actor can do in system  

- Use case: (bubbled) Consult available rooms
- Actor (stick figure) customer, database
- Relationship: (line between use case and actor) actor ---- UC
- Generalization: (arrow between actors) actor1 <- actor2 (basically inheritance)
- Includes (Generalization): (dotted arrow with `<<includes>>`) A -`<<includes>>`--> B "A includes the behavior of B"
- Extends (Generalization): (dotted arrow with `<<extends>>`) A <-`<<extends>>`-- C "C can be called while executing A"

                    (BUBBLE) Consult available rooms                 (STICKMAN) code management sys
                    /                                                      |                |
                   /                                                       |                |
        (STICKMAN) -------- (BUBBLE) Book a room <..`<<extends>>`..(BUBBLE) Apply Code      |
        customer \                                                                    (BUBBLE)
                  \                                                                 Apply promo code
                (BUBBLE) Request cancellation


                    (BUBBLE) Cancel Reservation....`<<includes>>`....>(BUBBLE) Connect to account (same one as below)
                  /
        (STICKMAN) ---- (BUBBLE) Apply promo code
        manager   \
                    (BUBBLE) Approve Booking ..(dotted line)`<<includes>>`...> (BUBBLE) Connect to account
