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
