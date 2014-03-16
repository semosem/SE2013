>## SOFTWARE DOCUMENTATION :sweat:
                                                                                                   -the lost case 
><p>This document is written as software documentation for way finding system in a private hospital called Hayat Hospital located in Addis Ababa, Ethiopia. 


#####About this Project

Product Name                                           | Team members             |Original Date |Edited on |
|:------------------------------------------------------|:--------------------------|:--------------:|----------      
| Find my way                                          |  ~~Lily Gebremariam~~    | 6.12.2013    |16.3.2014
|                                                      |  Sem Gebreseillase       |              |




>###Table of Contents

1.	`Introduction`
2.	`User requirements definition`

    * User groups definitions
3.	`system Architecture`
    * High-level overview of the system
    * Main modules and their functions represented
4.	`system requirements`
    * Functional Requirements
5.	`Non-functional System Requirements Non-functional system requirements`
    * Usability
    * Reliability
    * Efficiency
    * Other Non-functional Requirements
6.	`User Interface`
7.	`Project Management`



>### Introduction 

<p>At some point in our life, we all have wished if we could hear a magic direction whispered to our ear after getting in a situation where we couldn’t find a way to a particular destination inside a building. It’s frustrating, especially if we have to get to the place we want to go in an emergency cases. These situations are much worse and very serious issues when they involve healthcare service providing hospitals, as a patient or as a family of an injured person it might be necessary to get the service required immediately.

<p>This problem has inspired us to come up with idea of designing a “way finding” System for a certain health care center that uses touch screen standing kiosks and their interactivity nature. We believe that his system we are building will provide a step-by-step directions and distance- time information to patients and visitors of Hayat Hospital.
This Private Hospital named Hayat hospital is formerly a government hospital located in Addis Ababa Ethiopia and is infamous for having a huge departments and facilities but a weak information service. 

The kiosk system requires a web browser with good support of standard web Technologies – HTML 4, CSS 2, JavaScript, DOM, XML and XSLT. Also browser should have possibility to play back audio files either built in or via external plugin and run Java applets, because printing will be implemented using this Technology.
The system is also expected to introduce neat patient-flow, a significant increase in on-time appointments, improved patient experience and by providing a more efficient use of staff time and can reduced costs considerably.

>### User Requirement Definition 

#####User group definition
<p> Our product will primary have two main actors and depending on the credential provided some features of our system will be available and some will be hidden. These two actors are

1. Administrators and 
2. visitor

| User group     |                                 Definition    |
| :------------- |:----------------------------------------------| 
| **Administrator** | The administrator is the IT-Specialist or middle man who works to eliminate or make simple content updates for the system such as updating location drop off points, and adding additional locations. Additionally, admins analyze how the way finding system is being used. | 
|**Users/Visitors/Patients** | The user can be a patient/new staff / or just a visitor who is wondering around inside the hospital nuilding. These visitors  can either view on screen or print a comprehensive set of directions — including the way to the parking and/or any internal hospital destination. The user can access the system via a touch screen dashboard (kiosk)at the gate of the hospital.| 


######User's use-cases

The folloing numbered out use-cases are available for anyone without any authorization request whatsoever from any kiosk terminal inside Hayat Hospital.

1. **Activate the system:** In order to calculate the amount of users who used each kiosk, a "new user" event will be stored in statistics journal whenever new user touches screen. To distinguish users, timeout mechanism will be engaged and system will have two conditions: 
 * *Active*, whenever someone is using it, and 
 * *Inactive*, when timeout period has passed since last user used the kiosk. 
Thus "new user" event is just a switch from inactive state to active one.

2. **Search location by department directory:** User will be given and opportunity to search directions by department. Once the search is in, he list of departments will be shown on the screen as a search result, Users then select/click the department of their choice from the directory.

3. **Search location by room or desk:** Another possibility for Users is to chooses the option to search a particular room or desk. Onces that is done, again a list of rooms with the searched index will be displayed for the user to pick one. Once the users picked on/clicked that room/desk the direction and information on how to get there will be displayed.

4. **Browse search results:** After one of search options was chosen and clicked and result direction map is shown to user. Map should be shown in short form for the sake of fitting more directions on screen. User Interface will have usable means of navigating through resulting collection in case of it contains too many directions and cannot fit on screen. During browsing through resulting collection user can choose any department to be shown in full form.

6. **Choose and browse direction:** When user is browsing directions retrieved after search, he can choose any direction (map view) for full view. Full view includes spot mark where the user current location is and where his destination is with full-size map photo. Every time user chooses any of locations to browse corresponding
Event should be added to statistics journal. This event should also include what recipe was browsed.

7. **Print a map:** User can print out the map or direction using thermal printer connected to the kiosk. Information to be printed is full map description. Printing of map (direction) should be recorded in statistics journal and record will contain what direction was printed.

8. **Email map :** user can send the map showing his journey path to his email address by choosing  the email action button and one again he can re type or edit his email address by pressing the edit email button and send the map to his email account.

9. **Send map to phone:** the user can send the map to a his phone by entering his phone number by entering his phone number on the phone number typing bar after pressing” send to phone button”.

10. **Browse daily event (news):** At any moment of time user can browse information about system updates, place where terminal located, etc. Each piece of such information, news for simplicity, will have along with content start and end dates to be displayed. Also news will be assigned to one or more terminals, on which they should be shown. Every time when user chooses news to be displayed corresponding event has to be written to statistics journal.

######Administrator's use-cases


The administrator can use any personal computer for accessing administration functionality, but this functionality should be protected from unauthorized access.

1. Login to administration area. Whenever the administrator wants to use service he has to provide authentication information in form of User name and password. However he doesn’t have to log in whenever he has to done something. Once logged in his session should last until administrator logs out.

2. Browse list of locations. Administrator can get list of all locations stored in database with possibility to filter out list by department directory or and shop and dinning. Location list will contain only location name to be able to show more directions on screen.

3. Add location to database. Administrator can add new location to Database at any moment. For adding a new location he has to enter its description, edit the name of the location and select appropriate categories. (Determine whether the specific location is in the department, room or shop category)
4. Edit location in database. During browsing location list administrator can choose any location for editing. When he does it direction will be shown in full view – title, description, categories, with possibility to edit update any of these components. When updates are made administrator can save them in database.

5. Remove database. When administrator browses the location list (Use-case 2.2) he can choose any of them for deletion. But before location will be deleted from database administrator must confirm it once again. After confirmation location will be erased from database permanently.

6. Add route path (direction map): If the admin add a new location, edit, or delete in (case 2.4, 2.5, 2.6)he has to update the direction map for the newly added location or edit the map for the edited location. For example, in case of an elevator broke down the route path might be different one from the one that has already been made.

7. Browse list of “daily events”. Administrator can get list of “all daily event” stored currently in database. News list will contain news title and description, time period, when news will be displayed, and terminals, where news will be shown.
2.8. Add news to database. Administrator can add news to database at any moment. For adding news he has to enter its title, description, choose period, when it should be displayed, and select appropriate terminals, where news will be shown.

9. Edit (daily event) news in database. During browsing news list administrator can choose any “daily event “and edit it. When he does it all parts of news will be shown – title, description, terminals and time period, with possibility to edit update any of these components. When updates are made administrator can save them in database.

10. Remove “daily event “from database. When administrator looks through news list (Use-case 2.6) he can delete any event that doesn’t occur at that date or outdated. But before news will be deleted from database administrator must confirm it once again. After confirmation news will be erased from database permanently.

11. Browse list of terminals. Administrator can have the access to any terminal connected to the system. For each terminal there should be information if terminal is working currently or not.

12. Browse terminal's statistics. While browsing list of terminal administrator can choose any terminal to browse detailed information about. This information can include place where terminal is located and statistical data of terminal's use. Administrator can choose period for which statistics should be calculated. Statistical data will include how many people used terminal, what directions where browsed and what directions were printed.
