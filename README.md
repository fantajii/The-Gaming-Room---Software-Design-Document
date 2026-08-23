# The-Gaming-Room---Software-Design-Document
Project Reflection

The Client and Software Requirements
The Gaming Room is a game development company that required a robust, web-based distributed platform for their existing Android application, Draw It or Lose It. The goal was to transition the game to a centralized, in-memory Java server capable of supporting multiple concurrent users and teams. The core requirements included ensuring horizontal scalability, enforcing naming uniqueness across all sessions, assigning unique identifiers to all entities, and strictly maintaining a single instance of the game service in memory to serve as the single source of truth for the game state.

Strengths in Documentation
In developing this documentation, I was particularly effective at crafting the Executive Summary and defining the Design Constraints. By clearly separating the high-level business goals (like user engagement and scalability) from the technical constraints (like managing synchronization to prevent race conditions), I created a document that is accessible to both non-technical stakeholders and the development team.

The Value of Design Documentation
Working through the design document—specifically mapping out the UML Domain Model—was incredibly helpful before writing any code. By defining the Entity hierarchy and planning out exactly where to implement specific Java design patterns (like the Singleton pattern for the GameService and the Iterator pattern for safe collection traversal), I had a clear blueprint. It eliminated the guesswork of how classes would interact and made the actual development phase much more efficient.

Areas for Revision and Improvement
If I were to revise one part of my early work on this document, it would be the initial Evaluation of operating platforms. Initially, my focus was too narrow on basic server hosting. I improved this by expanding the recommendations to explicitly include modern distributed systems architectures—specifically, how deploying Linux servers across scalable cloud hosting tiers with load balancers is necessary to handle the client's requirement for thousands of concurrent players.

Interpreting User Needs
Drawing on my professional background in technical support, I know firsthand how frustrating a system can be when it isn't designed with the end-user's actual environment in mind. I interpreted the client’s needs by looking beyond just making the code work; I considered how network latency, browser compatibility, and concurrent access would impact the players. Considering the user's needs is critical because a system can be technically flawless, but if it drops a user's connection without attempting to reconnect or fails to adapt to their mobile browser, the application ultimately fails its primary purpose.

Approach to Software Design and Future Strategies
My approach to designing this software was highly methodical: I started with the broader business requirements, defined the environmental constraints, and then drilled down into the object-oriented architecture. In the future, I will continue to rely heavily on UML diagrams to visually map out relationships and identify necessary design patterns early in the process. Additionally, I plan to integrate security considerations (like token authentication and input sanitization) from the very first draft of the architecture, rather than treating them as an afterthought.
