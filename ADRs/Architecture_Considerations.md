# Here are 5 important reasons why a microservices and event-driven architecture would be suitable for meeting the Road Warrior requirements:
<h3>Why microservices?</h3>

1. **Scalability for High User Base:** With 2 million active users per week and a total of 15 million user accounts, a microservices architecture can efficiently handle the scalability requirements. Each microservice can be independently scaled up or down based on demand, ensuring optimal resource allocation.

2. **Real-time Updates:** Microservices can be designed to handle real-time updates efficiently. 

3. **Flexibility and Agility:** Microservices provide the flexibility to implement different functionalities as separate services. This aligns with requirements like interfacing with travel agency systems, providing end-of-year summaries, and gathering analytical data. Each microservice can evolve independently, enhancing agility.

4. **Responsive User Interface:** A microservices architecture enables the development of responsive user interfaces tailored to various deployment platforms. This ensures a rich user experience across web and mobile devices, meeting the specified response time requirements.

5. **Interoperability and Integration:** Microservices can seamlessly integrate with existing travel systems like SABRE and APOLLO, as required. Additionally, the event-driven approach allows for easy integration with external systems, such as preferred travel agencies, to facilitate quick problem resolution and international compatibility.

<h3>Why event driven?</h3>
    Incoming travel-related emails do not follow a continuous or periodic process at regular intervals. Instead, they are events that occur as a result of reservations and bookings made on external platforms or apps. These travel-related emails serve as trigger points within an asynchronous, real-time, and event-driven architecture. They initiate the extraction of trip-related information and its presentation on the user's dashboard. This approach ensures that users receive timely updates and information as events unfold in their travel plans.


Event-driven architecture, coupled with microservices, allows the system to react instantly to events like email updates, ensuring that travel information is updated in the app within the specified 5-minute window. The system can efficiently handle the high traffic, real-time updates, and diverse functionalities outlined in the requirements while ensuring high availability and a responsive user interface.

## Why a Monolithic Architecture May Not Be Ideal for Specified Requirements

1. **Scalability:** Managing the demands of 2 million active users per week and a total of 15 million user accounts presents a significant challenge within a monolithic architecture. Scaling the entire application to accommodate such volumes can result in inefficiencies and high costs.

2. **Real-time Updates:** Fulfilling the requirement for updates within a 5-minute timeframe of an event, as well as efficiently polling and processing email data for travel-related information, becomes considerably more intricate when dealing with a monolithic system. Event-driven and microservices architectures are better suited for handling real-time updates.

3. **Flexibility and Agility:** A monolithic architecture may struggle to adapt to the diverse array of requirements, particularly when integrating with external systems such as airline, hotel, and car rental interfaces, as well as social media platforms. Microservices offer the advantage of independent development, deployment, and maintenance, resulting in greater agility.

These three considerations underscore the significant challenges that a monolithic architecture could encounter in effectively meeting the specified requirements.

