

![Architecture_characteristics](https://github.com/KatasPioneers/RoadWarriors-Pioneers/assets/144905960/fbefffaf-5307-43bb-9d20-9a86c3f0d416)

Top driving charactersitics
1. __Availabilty__ :
   Availability is an essential aspect in a travel-related app where the user requires real-time updates during their journey. In such a context, minimizing downtime becomes paramount, allowing users to access information at their convenience from any geographical location. To achieve this level of uninterrupted service, we also implement a remote replication service for our database. This ensures maximum availability, enhancing our app's reliability for travelers who rely on timely information and access to essential services throughout their journeys. Our commitment to robust availability is central to delivering a seamless and dependable travel experience. We will customise to have a maximum downtime of 5 minutes/month.
2. __Interoperability__:
   Since real-time updates are sourced from various vendors and GDS, the Road Warrior system design must enable seamless integration with different platforms. This integration is crucial for providing real-time updates to users. Furthermore, the system must allow for dynamic inclusion and exclusion of platforms as needed, considering future circumstances. Therefore, interoperability is a decisive factor in the design of the Road Warrior system.
3. __Performance__:
   Travel-related apps experience a surge in traffic during the holiday season, when a maximum number of travelers plan their trips. Consequently, there is a high possibility of traffic bursts over a period of time. This behavior should not lead to latency issues when users access updates from the app. Therefore, there must be a robust system capable of handling latency and other performance issues, ensuring consistent performance even during significant spikes in user activity. We anticipate accommodating 2 million active users per week, with a total user base of 15 million.
