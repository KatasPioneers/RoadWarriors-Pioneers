Two essential business use cases in the problem statement are :

 

Trip organisation
Travel updates

 

Two primary sources we considered to extract the Trip details and travel updates from are:

 

Travel related user e-Mails :
   In case the user doesn't want to give read access to an external entity, he can chose to forward his travel related e-mails to Road warriors mailbox
   where the processing of travel related emails from the respective user is extracted.

 

Manual entries from the user:
   The user can manually enter the details of his reservations directly in the dashboard.

 

 

Organised trip details:

 

Once the Dashboard has entries pertaining to the reservations through any of the two sources above, the organiser service kicks in to analyse and segregate the reservations and groups them  
in trips chronologically.


Travel Updates:

 

The three primary sources we considered for flight/cab/hotel updates are:

     - Travel update e-mails from trvel agancies/airlines/cabs/hotels
     - The Integrated API component that fetches the updates from Global distribution system platforms like SABRE/APollo or directly to the flight/cab/hotel 
        using vendor api services.
     - Manual update


![Architecture](https://github.com/KatasPioneers/RoadWarriors-Pioneers/assets/144905960/c3408c32-bedb-4bb3-a6ad-6f8e48b49cca)


![TravelUpdatesWorkflow](https://github.com/KatasPioneers/RoadWarriors-Pioneers/assets/144905960/dcd5a80e-2308-4e22-bfe7-97f14ac70c97)


Poll email looking for travel-related emails
Filter and whitelist certain emails
The system must interface with the agency’s
existing airline, hotel, and car rental interface
system to update travel details (delays,
cancellations, updates, gate changes, etc.).
Updates must be in the app within 5 minutes of an
update (better than the competition)
Customers should be able to add, update, or
delete existing reservations manually as well.

Items in the dashboard should be able to be
grouped by trip, and once the trip is complete, the
items should automatically be removed from the
dashboard.
Users should also be able to share their trip
information by interfacing with standard social
media sites or allowing targeted people to view
your trip.
Richest user interface possible across all
deployment platforms

Provide end-of-year summary reports for users
with a wide range of metrics about their travel
usage
Road Warrior gathers analytical data from users
trips for various purposes - travel trends, locations,
airline and hotel vendor preferences, cancellation
and update frequency, and so on.

must integrate seamlessly with existing travel
systems (i.e, SABRE, APOLLO)
Must integrate with preferred travel agency for
quick problem resolution (help me!)
must work internationally

Users must be able to access the system at all
times (max 5 minutes per month of unplanned
downtime)
Travel updates must be presented in the app
within 5 minutes of generation by the source
Response time from web (800ms) and mobile
(First-contentful paint of under 1.4 sec)





