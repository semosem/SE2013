>## SOFTWARE DOCUMENTATION :sweat:
                                                                                                   -the lost case 
><p>This document is written as software documentation for way finding system in a private hospital called Hayat Hospital located in Addis Ababa, Ethiopia. 


#####About this Project

Product Name       | Team members             |Original Date |Edited on |
|:-----------------|:-------------------------|:------------:|----------      
| Find my way      |  ~~Lily Gebremariam~~    | 6.12.2013    |16.3.2014
|                  |  Sem Gebreseillase       |              |

`Table>1: project description`


>###Table of Contents

1. `Introduction`
2. `User requirements definition`
    * User groups definitions
3. `system Architecture`
    * High-level overview of the system
    * Main modules and their functions represented
4. `system requirements`
    * Functional Requirements
5. `Non-functional System Requirements Non-functional system requirements`
    * Usability
    * Reliability
    * Efficiency
    * Other Non-functional Requirements
6. `User Interface`
7. `Project Management`



>### Introduction 

<p>At some point in our life, we all have wished if we could hear a magic direction whispered to our ear after getting in a situation where we couldn’t find a way to a particular destination inside a big building. It’s frustrating, especially if we have to get to the place we want to go in an emergency case. Situations like this are much worse and very serious issues when they involve healthcare service providing hospitals, as a patient or as a family of an injured person it might be necessary to get the service required immediately.

<p>This problem has inspired us to come up with idea of designing a “way finding” System for a certain health care center that uses touch screen standing kiosks and their interactivity nature. We believe that his system we are building will provide a step-by-step directions and distance- time information to patients and visitors of Hayat Hospital.
This Private Hospital named Hayat hospital is formerly a government hospital located in Addis Ababa Ethiopia and is infamous for having a huge departments and facilities but a weak information service. 

<p>The kiosk system requires a web browser with good support of standard web Technologies – HTML 4, CSS 2, JavaScript, DOM, XML and XSLT. Also browser should have possibility to play back audio files either built in or via external plugin and run Java applets, because printing will be implemented using this Technology.
<p>The system is also expected to introduce neat patient-flow, a significant increase in on-time appointments, improved patient experience and by providing a more efficient use of staff time and can reduced costs considerably.

>### User Requirement Definition 

####User group definition
-------------

<p> Our product will primary have two main actors and depending on the credential provided some features of our system will be available and some will be hidden. These two actors are

1. Administrators and 
2. visitor

| User group     |                                 Definition    |
| :------------- |:----------------------------------------------| 
| **Administrator** | The administrator is the IT-Specialist or middle man who works to eliminate or make simple content updates for the system such as updating location drop off points, and adding additional locations. Additionally, admins analyze how the way finding system is being used. | 
|**Users/Visitors/Patients** | The user can be a patient/new staff / or just a visitor who is wondering around inside the hospital nuilding. These visitors  can either view on screen or print a comprehensive set of directions — including the way to the parking and/or any internal hospital destination. The user can access the system via a touch screen dashboard (kiosk)at the gate of the hospital.| 




####User's use-cases
-------------
The folloing numbered out use-cases are available for anyone without any authorization request whatsoever from any kiosk terminal inside Hayat Hospital.

1. **Activate the system:** In order to calculate the amount of users who used each kiosk inside the building, a "new user" event will be stored in statistics journal whenever new user touches screen. To distinguish users, timeout mechanism will be engaged and system will have two conditions: 
 * *Active*, whenever someone is using it, and 
 * *Inactive*, when timeout period has passed since last user used the kiosk. 
Thus "new user" event is just a switch from inactive state to active one.

2. **Search location by department directory:** User will be given and opportunity to search directions by department. Once the search is in, he list of departments will be shown on the screen as a search result, Users then select/click the department of their choice from the directory.

3. **Search location by room or desk:** Another possibility for Users is to chooses the option to search a particular room or desk. Onces that is done, again a list of rooms with the searched index will be displayed for the user to pick one. Once the users clicked that room/desk the direction and information on how to get there will be displayed.


4. **Choose and browse direction:** When user is browsing directions retrieved after search, he can choose any direction (map view) for full view. Full view includes spot mark where the user current location is and where his destination is with full-size map photo. Every time user chooses any of locations to browse corresponding event should be added to statistics journal. This event should also include what recipe was browsed.

5. **Print a map:** User can print out the map or direction using a thermal printer connected to the kiosk at all times. Information to be printed is full map description. Printing of map (direction) should be recorded in statistics journal and record will contain what direction was printed.

6. **Email map :** user can also send the map showing his journey path to his email address by choosing  the email action button and onece again users can re-type or edit his email address by pressing the edit email button and send the map to his email account.

7. **Send map to phone:** another option for users to grab on to the inofrmation they want is by  sending it to a their phone. This can be done by entering a phone number on phone number typing bar and  pressing *”send to phone button”*.

8. **Browse daily event (news):** At any moment of time users can browse information about system updates, place where terminal located, or advertizments etc. Each piece of such information/news for simplicity, will have a long list with content start and end dates. Also news will be assigned to one or more terminals, on which they should be shown. 



'![hmmm](http://users.metropolia.fi/~semg/SoftwareEngineering/useruc.jpg)'

`Figure>1: User's use-case diagram`


####Administrator's use-cases
-------------
The administrator can use any personal computer for accessing administration functionality by plugging it a central system that connect with all kiosks in the building, These following functionality are protected from unauthorized access.

1. **Login to administration area:** Whenever the administrator wants to use service he has to provide authentication information in form of User name and password. Once logged in his session the admin can continue with admin activities should last until loged out.

2. **Browse list of locations:** Administrator can get list of all locations stored in database with possibility to filter out lists by department directory and/or rooms with in the building. Locations will be displayed following the search command.

3. **Add location to database:** Administrator can add new location to the database at any moment while logged in. For adding a new location he has to enter its description, name of the location and select appropriate categories. (Determine whether the new location is in the department catagory or room).

4. **Edit location in database:** During browsing locations list administrator can also choose any location for editing. When he does it direction will be shown in full view – title, description, categories, with possibility to edit update any of these components. When updates are made administrator can save them in database.

5. **Remove location from database:** When administrator browses the location list (Use-case 2) he can choose any of them for deletion. But before location will be deleted from database administrator must confirm it once again. After confirmation location will be erased from database permanently.

6. **Add route path (direction map):** If the admin add a new location, edit, or delete in (case 2.4, 2.5, 2.6)he has to update the direction map for the newly added location or edit the map for the edited location. For example, in case of an elevator broke down the route path might be different one from the one that has already been made.

7. **Browse list of *daily events*:** Administrator can get list of “all daily events” stored currently in database for analysis perpose. News list will contain news title and description, time period, when news will be displayed, and terminals, where news will be shown.

8. **Add news to database:** Administrator can add also add news and advertizments if interested. For adding news he has to enter its title, description, choose period, when it should be displayed.

10. **Remove *daily event* from database:** When administrator looks through news/daily events list (Use-case 7) he can delete any event that doesn’t occur at that date or outdated. But again,before news will be deleted from database administrator must confirm it once again. After confirmation news will be erased from database permanently.

11. **Browse list of terminals:** Administrator can have the access to any terminal connected to the system. For each terminal there should be information if terminal is working currently or not.

12. **Browse terminal's statistics:** While browsing list of terminal administrator can choose any terminal to browse detailed information about it. This information can include place where terminal is located and statistical data of terminal's use. Administrator can choose period for which statistics should be calculated. Statistical data will include how many people used terminal, what directions where browsed and what directions were printed.


![hmmm](http://users.metropolia.fi/~semg/SoftwareEngineering/adminuc.jpg)

`Figure>2: admin's use-case diagram`


>###System archtecher

#### High-level overview of the system
______

The UML class diagram below shows a more clear description of high-level components necessary for required functionality and the associations amaong them. We recoment to take you to give it a closer look because it represents the logical view on system architecture.



![hmmm](http://users.metropolia.fi/~semg/SoftwareEngineering/ULclass.jpg)

`Figure>3: UL Class diagram(Main modules and their functions represented)`



>###User Interface

####User interface prototype

The figures below are drawings of user interface at different circumstances of the system. Figure 4 below is the initial page, which user sees when he starts using kiosk.Users can see the initial page that has an operator recorded women(audio assistant ) that explains what the user shall do inorder to get the most out of the kiosk. Users define whether they want to browse through *departments* or  *room* with in the building. 


![hmmm](http://users.metropolia.fi/~semg/SoftwareEngineering/userinitial.jpg)

`Figure>4: User interface prototype of the initial page`

<p>At the very bottom of the page there is a detached bar containing the daily event ocurance. The interface comes with a recorder sound guide asking the user what he wants to do.

When the user chooses the option to find a location by department name the interface will appear as in “Figure 2” below which will have the list of departments listed down, with down and up arrows buttons  on the left  assisted to browse the user the specific department he wants to choose. 

![hmmm](http://users.metropolia.fi/~semg/SoftwareEngineering/dept.jpg)

`Figure>4: User interface Search result in department search`

Once the users found and clicked on the department of their liking the link bar having the department name will turn into blue and the department will be taken as the user’s final destination automatically.



After users choice is recieved from search results, the next page will appear containing a full map image and all information indicating the whole direction path. The map will have a red spot that indicates current location of the user and green button indicating the final destination of the user.The route path is drawn between this two spots on the map.

![hmmm](http://users.metropolia.fi/~semg/SoftwareEngineering/map.jpg)
`Figure>4: User interface Search result in department search`

<p>The map image will appear at the middle of the page beneath that there are two option buttons indicating the walking distance and time. However the audio assistant will also address the walking distance the description of the route path verbally.
At the very bottom of this page there are department, room, shop and dinning option buttons that will redirect the user to another new search using the other options. This buttons are the ones that appear at the initial page of the system.
At the left edge of the page the print action option and email option buttons are placed.





>###System requirement

####Functional requirements
___

• Whenever new user appears to use the system at first glance he has three options for search, to search direction: by department, room/desk or shop and dinning, Such as radiology department. 
•after the first interaction, the interface will appear with list of directions and then he can choose any of the directions from the list and browse it with more details on the screen.
•the displayed information will show details like:  walking distance, time it takes, direction path starting from the kiosk terminal up to the chosen destination, description and map. During browsing through direction user should have possibility to return back to search result.
• The user has the option either to print the map or
• He/she can email or send the map to his phone.
•if kiosk is idle and nobody uses it for the moment, a map which will show the whole building will appear by default; moreover news of the day will appear at the very bottom left of the screen.
• The user can browse and have access to the news from the display.
• Taking into consideration the user for the system might be computer illiterates and doesn’t have any experience with similar system it should be appealing and have to have easy to use functions like single touch on the screen.
• Tough the user have the right to access to files on the kiosk, it is prohibited to gain kiosk functionality related task.
•the recorded voice guide is designed to promote users to use the system and help the user with the functionality of the system. This message should be played periodically when someone is using the system.
• All terminals found in the hospital work at the same moment (simultaneously) and give the information requested at the same level.
• the number of users who uses the kiosk and the specific task they perform like the map that was displayed to them and whether the map being printed will be stored as a data.
•possible tasks will be designed for the administrator like adding, editing and deleting directions when conditions change, like an out-of-service elevator or closed hallway. And news, viewing statistical data;
• The administrator’s task should be secured from unauthorized person, authentication is checked using password and user name.


>###Non-functional requirments

####Usability 
The interfaces are very straight and simple to use. The map simply spots your current location; draw the path that you follow until you reach your destination. The system spots facilities, stairs, and emergency exits with icons and explain them. Make rest-rooms stand out (more often than not, the first thing visitors will look for when they enter your building). The maps will give a better sense of space, distance and direction.
The direction is signified by buttons. Make them large, the text self-explanatory and present them clustered in a designated area, the audio guide makes the path easier to understand, even if we were unable to understand the path from the map. Above all the audio will help for disabled patients, have eyesight problem and the user can be sited and able to the kiosk
4.2. Reliability
These applications interface, stop users from changing the configuration of software or downloading computer viruses.it provides a 24, 7 services, and includes a fully-fledged digital signage system. : improved patient-flow, an increase in on-time appointments, more efficient use of staff time, decrease costs and a significantly boosted patient experience, all at a cost far less than you would pay a single FTE.
4.3. Efficiency
4.4. Other Non-functional Requirement
• The project doesn’t need to cost lot of money as the company’s request so we minimize the Internet traffic; no additional cost could be added to the project like additional software cost.
• As the system will be viable, so we could not revile the source code to the public;
• The company set 9 months to implement and deliver the system to them.
2 Project Management
 In order to prepare this documentation it took us more than 60 hours, probably each person take 20 hrs. And the most difficult part was to decide on which system should we take as our project because the way finding system has both a web based application that could be run on Pcs and the kiosk terminal ,which we consider now. We were about to write about the web based app however we found it having too much details and with the time that we had we found It better to take this system. We almost write for both options and that’s way we had to linger on the project submission deadline. However to be genuine we didn’t start the project in time we promised ourselves not to rush when another project came up.



