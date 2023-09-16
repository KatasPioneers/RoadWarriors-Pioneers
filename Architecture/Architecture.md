Two essential business use cases in the problem statement are:

1. Trip organization
2. Travel updates

Two primary sources we considered to extract the trip details and travel updates from are:

1. **Travel-related user emails:**
   In case the user doesn't want to grant read access to an external entity, they can choose to forward their travel-related emails to the Road Warriors mailbox, where the processing of travel-related emails from the respective user is extracted.

2. **Manual entries from the user:**
   The user can manually enter the details of their reservations directly into the dashboard.

Organized Trip Details:

Once the dashboard has entries pertaining to the reservations through any of the two sources above, the organizer service kicks in to analyze and segregate the reservations, grouping them into trips chronologically.

Travel Updates:

The three primary sources we considered for flight/cab/hotel updates are:

- Travel update emails from travel agencies/airlines/cabs/hotels
- The integrated API component that fetches the updates from Global Distribution System platforms like SABRE/APollo or directly from the flight/cab/hotel using vendor API services.
- Manual updates



![Architecture](https://github.com/KatasPioneers/RoadWarriors-Pioneers/assets/144905960/c3408c32-bedb-4bb3-a6ad-6f8e48b49cca)


![TravelUpdatesWorkflow](https://github.com/KatasPioneers/RoadWarriors-Pioneers/assets/144905960/dcd5a80e-2308-4e22-bfe7-97f14ac70c97)


Poll email looking for travel-related emails
Filter and whitelist certain emails
Customers should be able to add, update, or
delete existing reservations manually as well.



# User Registration Service

When a user wants to register for our app 'The Road Warrior,' they must provide specified fields/information via the user registration service interface.

The identity management database is then called to save all the user registration information.

# Login Authentication Service

Once a user is registered, they can log in using their credentials. The user's credentials are validated by the identity management system, allowing them to log in.

When the user logs in, they can choose the following settings:

- Grant read access to emails.
  - Grant our application portal access to read emails via their email ID.

- Grant access to forward emails.
  - Forward the user's emails to our portal mailbox server.

# Manual Entries to Dashboard

Users can manually add trip details to the dashboard. The information entered by the user will be processed by the 'Trip Organizer Service' and displayed in the dashboard.

# Travel Email Scan Service

If the user grants access to read emails, this service will scan incoming travel emails from the user's mailbox and filter all trip-related emails, forwarding them to the 'Travel Emails Repository.'

This service is triggered every 3 minutes to scan user emails.

# Target User Email Filter Service

This service identifies all travel emails from the server's mailbox concerning the user, filters them, and forwards them to the 'Travel Emails Repository.'

This service is triggered when new emails are forwarded to the mailbox server.


The system must interface with the agency’s
existing airline, hotel, and car rental interface
system to update travel details (delays,
cancellations, updates, gate changes, etc.).
Updates must be in the app within 5 minutes of an
update (better than the competition)

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





