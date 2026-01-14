# Class 4

 ## Recap from class 3
* Agile was developed to deliver software faster
* Was designed for small teams/projects

Hows does aAgile scale to larger teams/projects?

* Working software over comprehensive documentation

* Agile frameworks for scaling
  * without comprehensive documentation, harder to maintain large systems
  * good documentation = priority

* Customer collaboration over contract negotiation
  * not neceessarily compatible with the legal approach of large companies
  * Try to have both (start with contract + communication)
* informal communication is prioritized
    * Teams now spread out over multiple locations and async communication is required

---

<p align="center">In many cases, Agile is adapted to buisness needs</p>


## Chapter 4: Requirments Engineering

What are requirements?
* A requirement is a condition or capability needed by a user to solve a problem or achieve an objective

* A requirement is a condition or capability that must be met or possessed by a system to satisfy a contract, standard, specification, or other formally imposed document

### 4.1: Types of Requirements

Requirements can be categorized

1. User vs System Requirements
    * User Requirement:
        * High level
        * Describes the services the system is expected to provide to the user

        example: RoomBookingSystem (AirBnB)

        "A user shall be able to book a room"
        "A user shall be able to cancel a booking"
        (structure to be fixed)

    * System Requirement:
        * low level
        * Describes the system's functions, services, and operational constraints in detail

        example: RoomBookingSystem (AirBnB)
        "The system shall check room availability and present the relevant information to the user with a link redirecting toi a page with room details"

        -> specific

2. Functional vs Non-Functional Requirements
    * Functional Requirement:
        * Describes the system's functionality
        * Desctibes how the system should behave in particular situations

        example: RoomBookingSystem (AirBnB)

        "The system shall allow users to book a room that is available for the selected dates"

        -> structure


    

    * Non-Functional Requirement:
        * Relate to properties/constraints
        * "How should the system do this?"
        * timing, performance, security, usability, reliability

        example: RoomBookingSystem (AirBnB)

        "The system shall respond to user actions within 2 seconds"

        -> I want a system req

#### Examples:
1. The system shall support at least 100,000 concurrent users without performance degradation. (System, Non-functional)

2. The system shall allow users to filter their search results by amenities. (User, Functional)
3. The system shall prevent double bookings by blocking dates during the reservation process (System, Functional)
4. The system shall log users out automatically after 15 minutes of inactivity. (System/User, Non-functional)