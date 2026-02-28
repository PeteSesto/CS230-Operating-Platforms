# CS230-Operating-Platforms
Repository of CS-230 submitted coursework

# CS-230 Project Reflection: Draw It or Lose It

## Client and Software Requirements
The client was The Gaming Room, a company looking to expand their existing "Draw It or Lose It" game. They needed to transition the software from a single-platform Android application into a highly scalable, web-based environment accessible across multiple operating systems (Windows, Mac, Linux, iOS, Android). The required software was a distributed, real-time multiplayer game capable of hosting multiple concurrent instances and teams, requiring a centralized server logic rather than local device hosting.

## Documentation Strengths
The documentation breaks down the complex transition from a standalone mobile app to a robust Three-Tier Client-Server architecture. The UML domain model clearly maps out the object-oriented structure needed to meet the client's strict memory and identification constraints, specifically detailing how inheritance and the Singleton pattern solve the requirement for unique entities and a single-instance game manager.

## Value of the Design Process
Working through the design document forces a high-level, strategic perspective before getting bogged down in coding syntax. Defining the system constraints and the domain model upfront (such as establishing the `GameService` as a Singleton) prevents fundamental architectural mistakes that would be extremely difficult and time-consuming to refactor later in the actual development phase.

## Areas for Revision
If I could revise one part of the work, I would expand the design documentation regarding edge-case network latency and offline capabilities for mobile users. While the current design recommends WebSockets and load balancing for real-time communication, adding specific fallback strategies, such as local caching for drawing progress if a player's cellular connection temporarily drops, would make the application's architecture even more resilient.

## Interpreting User Needs
The users needed a seamless, highly responsive experience across different devices, from high-end gaming PCs to budget smartphones. This was implemented by designing a responsive HTML5 web interface to eliminate platform barriers and recommending double-buffering memory techniques to ensure the 8MB high-definition images render smoothly without stuttering. Considering the user’s needs is paramount because technically sound software is useless if the end-user finds it frustrating or inaccessible.

## Software Design Approach and Future Strategies
The approach began with a strict analysis of the constraints (web-based, multi-platform, singleton memory), mapping out the logical system topology, and then selecting the appropriate operating environments (like a Linux server and MySQL database). In the future, I plan to continue implementing UML diagramming early in the design phase, and I would incorporate more detailed threat-modeling to anticipate security and authorization needs before writing any foundational code.
