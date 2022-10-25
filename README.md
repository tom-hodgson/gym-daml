# Gym 

This project simulates a very basic workflow for gym class registration. A user can apply for membership of the gym. Once the gym accepts this request the member can register for gym classes. 

Each gym class can accomodate a maximum number of members. People are assigned to a class on a first come first served basis. Once the class is full, members can still register, but will be added to a waiting list. A registered member may cancel a class, resulting in everyone on the waiting list moving up one place.

If a member registers for a gym class but doesnt show up, they receive a 'strike'. People with 3 strikes can't register for another class. These strikes expire after six months.


## Implementation

This implementation keeps the member's registrations, attendences, and strikes private to that individual (and the Gym party). This means each member enters a contract with the gym (not with each other). Because of this restriction we need an off ledger process `updateWaitingList` to update the waiting list due to any cancelations that may have happened. This could be run periodically or possibly from a DAML trigger (I didn't read much about triggers). 

