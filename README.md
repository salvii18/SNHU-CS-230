# SNHU-CS-230
**Author:** Benj Salvador
**Class:** SNHU CS 230

## Project Summary
**Client:** The Gaming Room
**Software Requirement:** The client requested a multi-platform, web-based version of their Android game, *Draw It or Lose It*. The system needed to transition from a single-device mobile app to a scalable 3-tier web architecture supporting multiple teams, unique game/team/player naming via the Iterator pattern, and centralized state tracking using the Singleton pattern in a Java backend (`GameService`)

## Reflection

### What I did well
I did well on having a clearly articulated documenting the architectural transition from a single mobile device to a distributed cloud environment. Specifically, showing a detailed evaluation matrix and giving a good recommendation that provides a thoroughly analyzed host platforms (Linux vs. Windows vs. macOS), JVM memory management, PostgreSQL storage, WebSockets networking, and security protocols like TLS and JWT that helps the client know the advantages and disadvatages of the possible choices they can make.

### Helpfulness of Design Documents In Regards to Coding
While working through the UML class diagrams and software design document before I made the code made the implementation phase smoother. Having a predefined class relationships, `Entity` superclass leading to `Game`, `Team`, and `Player', and explicit patterns, Singleton for `GameService` and Iterators for collection searches,  eliminated the most annoying process while developing Java for me which is guesswork.

### Areas for Improvement
If I could revise one part of my design work, I would expand the UML diagram and documentation around dynamic database scaling and Redis caching strategies. While I am happy with the current design which outlines PostgreSQL storage, detailing the exact ORM mapping (e.g., Hibernate/JPA) and real-time cache synchronization I think it would make the document better if I further expanded on strengthening system performance under high concurrency.

### Interpreting and Implementing User Needs
The way I interpreted the client's need for unique entity names and concurrent game sessions is by implementing strict input pre-validation using the Iterator pattern and restricting `GameService` to a single memory instance via the Singleton pattern. Considering the user needs is critical since non functional requirements like uptime,  cross-platform browser support, dynamic scaling, and data security—directly impact player experience and business success.

### Software Design Approach and Future Strategies
My approach relied on modularity, OOP principles (inheritance, encapsulation, abstraction), and standard design patterns. In the future, I will continue using top-down domain modeling, sequence diagrams for distributed APIs, and containerized dev environments as something to use to analyze, plan, and architect complex software applications before writing code. 
