

![Architecture_characteristics](https://github.com/KatasPioneers/RoadWarriors-Pioneers/assets/144905960/fbefffaf-5307-43bb-9d20-9a86c3f0d416)

Top driving charactersitics
1. __Availabilty__ :
   Availability is an essential aspect in a travel-related app where the user requires real-time updates during their journey. In such a context, minimizing downtime becomes paramount, allowing users to access information at their convenience from any geographical location. To achieve this level of uninterrupted service, we also implement a remote replication service for our database. This ensures maximum availability, enhancing our app's reliability for travelers who rely on timely information and access to essential services throughout their journeys. Our commitment to robust availability is central to delivering a seamless and dependable travel experience. We will customise to have a maximum downtime of 5 minutes/month.
2. __Interoperability__:
   Since real-time updates are sourced from various vendors and GDS, the Road Warrior system design must enable seamless integration with different platforms. This integration is crucial for providing real-time updates to users. Furthermore, the system must allow for dynamic inclusion and exclusion of platforms as needed, considering future circumstances. Therefore, interoperability is a decisive factor in the design of the Road Warrior system.
3. __Performance__:
   Travel-related apps experience a surge in traffic during the holiday season, when a maximum number of travelers plan their trips. Consequently, there is a high possibility of traffic bursts over a period of time. This behavior should not lead to latency issues when users access updates from the app. Therefore, there must be a robust system capable of handling latency and other performance issues, ensuring consistent performance even during significant spikes in user activity. We anticipate accommodating 2 million active users per week, with a total user base of 15 million.
4. __Scalability__:
Since this app targets global users and integrates with various Global Distribution Systems, it is expected that the user database will grow significantly over time. Therefore, the Road Warrior system has to be highly scalable to accommodate the expanding user base and the corresponding processing capabilities in proportion. It is imperative to design the system to scale effectively to handle high workloads over time."
5. __Elasticity__:
The system should possess the elasticity required to accommodate traffic spikes during holiday seasons and weekends. The activity of Road Warrior users is limited when there are no upcoming or planned trips, especially during non-traveling periods. Hence, it is essential to handle activity spikes during specific time spans, such as holidays, given the high number of active users during those times. In addition to scalability, elasticity is also a crucial characteristic influencing the architecture design."

