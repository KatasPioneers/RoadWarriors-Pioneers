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
must integrate seamlessly with existing travel
systems (i.e, SABRE, APOLLO)


# Updating Reservations and Trip Details

When it comes to updating existing reservations or trip details for users, Road Warrior relies on the following primary sources:

1. **Travel Update Emails:** These emails come from agencies, airlines, cabs, and hotels.

2. **Integrated API Interface:** Road Warrior interfaces with individual airline exchanges, cab services, hotels, and Global Distribution System (GDS) platforms such as SABRE and APOLLO.

3. **Manual Updates:** Users can manually update their reservations and trip details directly on the Road Warrior Dashboard.

In the travel update workflow, the Road Warrior Dashboard interfaces with the following services:

- **Travel Update Parser Service:** Similar to the trip gathering flow, the Travel Email Scan Service polls the user's mailbox every 3 minutes to scan for new travel-related emails and feeds them to the Travel Emails Repository. The Travel Update Parser Service then identifies changes made to reservations and updates the dashboard accordingly.

- **Travel Update Request Service:** This service polls all integrated travel exchanges, including airlines, cabs, hotels, SABRE, and APOLLO, every 3 minutes to request travel updates via their standard APIs. It updates the details in the dashboard.

- **Manual Updates:** The Road Warrior Dashboard also interfaces with the user, allowing them to update or delete any existing reservation details.

- **Notification Service:** Finally, any travel updates made on the dashboard are notified to the user via SMS and email.



Items in the dashboard should be able to be
grouped by trip, and once the trip is complete, the
items should automatically be removed from the
dashboard.

Users should also be able to share their trip
information by interfacing with standard social
media sites or allowing targeted people to view
your trip.

Here are the points in a formatted Markdown list:

- **User Authentication:**
  - Implement user authentication to allow users to connect to their social media accounts securely.

- **User Info Storage:**
  - Store user information, including social media account details and access tokens, securely in your system.

- **Token Management:**
  - Handle token expiration and implement token refreshing mechanisms to maintain users' connections to social media platforms.

- **API Integration:**
  - Integrate with APIs provided by different social media platforms to facilitate data exchange.

- **Posting User Information:**
  - Use the social media platform APIs to post user information and content as required.

- **Error Handling:**
  - Implement robust error handling mechanisms to address cases where posts fail to share, providing appropriate feedback to users.

- **Terms of Service Compliance:**
  - Understand and adhere to the terms of service and policies of the social media platforms to ensure legal and ethical compliance.

- **Front-End Implementation:**
  - Develop and integrate share buttons into the front-end of your application, allowing users to easily share content on various social media platforms.

Richest user interface possible across all
deployment platforms

Provide end-of-year summary reports for users
with a wide range of metrics about their travel
usage

# Year-End Summary: getTravelSummaryService

- A "Summary" button will be displayed on the Dashboard.

- When clicked, users will be shown their Travel Summary using the following metrics:

  - **Traveling Done Month Wise:** 
    - Used to deduce the preferred month for travel.
    - Used to deduce the preferred hotel for stay.
    - Used to deduce the preferred flight courier for travel.
    - Used to deduce the preferred cab provider for travel.
    - Used to deduce the preferred destination for travel.
    - Used to deduce the preferred type of travel (short trips/long trips/solo/family/group).


Must integrate with preferred travel agency for
quick problem resolution (help me!)
must work internationally

# Global Help: getHelpService

- The `getHelpService` will be used, which will call `getHelpServiceByAgency` once the Name of the Agency is provided by the User.

- A "Help" button will be displayed on the Dashboard.

- When clicked, the user will be asked for the "Agency Name" they want to contact.

- On providing the "Agency Name," the app will use the corresponding Agency's Contact API to provide Help.

# Help on Each Reservation Line Item: getHelpServiceByAgency

- On clicking the "Help" option from the context menu, the App will use the respective Agency's Contact API for the specific reservation to provide Help.


Road Warrior gathers analytical data from users
trips for various purposes - travel trends, locations,
airline and hotel vendor preferences, cancellation
and update frequency, and so on.


# Road Warrior Analytics

Road Warrior performs analytics on both real-time and batch data gathered from various sources, including:

- Trip details from different users
- Reservation and update details from various Global Distribution Systems (GDS), agencies, and vendors

## Real-Time Data Analysis

Real-time data, such as GPS location from users, is used to assess the status of ongoing trips. This data, collected from multiple users, is processed and analyzed in the backend and presented to the user as various trends, including:

- Number of visitors to a particular tourist spot in a location.
- Average time spent at a specific spot.
- Users' restaurant preferences.
- Users' accommodation preferences.
- Optimized plans for visiting tourist spots in a particular destination.

Real-time weather updates collected from places on the itinerary can also assist users in making decisions about their upcoming bookings based on changes in weather.

## Batch Data Analysis

Batch data, including users' flight, cab, and hotel preferences, cancellations, and update frequencies, is collected from both users (local database) and GDS, travel agencies, and vendors. This data can be used to identify trends such as:

- Most punctual airlines to a specific destination.
- Airlines preferred by users for a particular destination.
- Preferred cab services among users.
- Preferred hotel preferences for a destination city or, more specifically, a tourist spot, etc.

## Analytical System

The real-time and batch data collected are fed into the analytical system to derive trends in the travel domain. The analytical system consists of:

- An ingest system that collects data from different sources.
- The ETL (Extract, Transform, Load) component, which processes batch data and loads it into the target data warehouse.
- Real-time and batch data stored in the data warehouse for further analysis.
- The analytic engine, which analyzes the data and produces various statistical observations and predictions presented to users' dashboards as trends.



Users must be able to access the system at all
times (max 5 minutes per month of unplanned
downtime)
Travel updates must be presented in the app
within 5 minutes of generation by the source
Response time from web (800ms) and mobile
(First-contentful paint of under 1.4 sec)





