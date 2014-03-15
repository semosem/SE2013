##### [2013]

**By**	
* Lily Gebremariam
* Sem Gebressilase



#### [SOFTWARE DOCUMENTATION]
_[This document is written as software documentation for way finding system for a private hospital called Hayat Hospital located in Addis Ababa, Ethiopia.]_

Date of Original report	**6.12.2013**
Edited on **14.03.2013** 
Edited by **Sem Gebresilassie**







 



 

 Introduction

At some point in our life, we all have wished if we could hear a magic direction whispered to our ear after getting in a situation where we couldn’t find a way to a particular destination. It’s frustrating, especially if we have to get to that place in emergency cases. These situations are much worse and very serious issues when they involve getting to a healthcare service providing hospital as a patient or as a family of an injured person. 

This problem has inspired us to come up with idea of designing a “way finding” System for a certain health care center that uses touch screen smart phones and their interactivity nature. This system we are building will provide a step-by-step directions and distance- time information to patients and visitors of a hospital that we have in mind named Hayat Hospital.
 
Directions to any terminal/room and/or office found in the hospital can be accessed and printed. More importantly, our system can also be used to email direction related information to any mobile phone. The system is expected to introduce superior patient-flow, a rise in on-time appointments, and more efficient use of staff time and also reduced costs and a significantly improved patient experience.

We are planning to develop this product for a small private hospital called “Hayat Hospitals”.
The hospital was formerly a government hospital having a huge departments and facilities. And it was using the way finding system made by a company called” logic junction” .however  the hospital is now condensed and become a small private hospital having smaller departments, Thus why we need to customize the system as well.

The kiosk system requires a web browser with good support of standard web Technologies – HTML 4, CSS 2, JavaScript, DOM, XML and XSLT. Also browser should have possibility to play back audio files either built in or via external plugin and run Java applets, because printing will be implemented using this Technology.


 
User Requirement Definition
2.1. Revision History

Name 	
Date	
Reason For change	
Version
Lily Gebremairam
Sem Gebressilase	06.11.2013	The current system was designed for a bigger Firm and we need to customize it to a smaller faculty	1.0 Draft 1
2.2 User group definition


User group 	

Definition

Administrator	The administrator is the IT-Specialist or middle man who works to eliminate or make simple content updates for the system such as updating location drop off points, and adding additional locations. Additionally, it tracks usage and allows you to analyze how your way finding system is being used.

(user)
visitor/patient/staff	The user can be a patient/staff /visitor who want to use the Pre-Planning option. The visitors   can view on screen or print a comprehensive set of directions — including driving, parking and internal hospital guidance.  Those directions, essentially turning every screen in the facility into a dynamic way finding system.
The user can access the system via a touch screen dashboard (kiosk) at the gate of the hospital.

	
                           
     















2.3 User's use-cases
All the following use-cases are available for an authorized access from any kiosk terminal.
1. Activate the system: In order to calculate the amount of users who used each kiosk, whenever new user touches screen "new user" event will be stored in statistics journal. To distinguish users timeout mechanism will be engaged: system will have two conditions: active, whenever someone uses it, and inactive, when timeout period has passed since last user used the kiosk. Thus "new user" event is switch from inactive state to active.

2. Search location by department directory. User chooses option to search direction by department, the list of departments will be shown on the screen then, he select (click) the department of his choose from the department directory(using a scroll up and down arrows from the left), after search is done result is shown to user.

3. Search location by room or desk. User chooses option to search room. Then he chooses from sets of rooms. Example of room/desk are, room no 101……….auditorium conference room. With detailed description in front of the room will be displayed. Then the user chooses his choose of room, after search is done result is shown to user.
4. Search location by shops and dinning. User chooses option to search direction to a particular shop or dinning facility by shops and dinning search button. After search is done he has to choose again a particular shop or dinning services of his choose from the list.

5. Browse search result. After one of search options was chosen and clicked and result direction map is shown to user. Map should be shown in short form for the sake of fitting more directions on screen. User Interface will have usable means of navigating through resulting collection in case of it contains too many directions and cannot fit on screen. During browsing through resulting collection user can choose any department to be shown in full form.
6. Choose and browse direction. When user is browsing directions retrieved after search, he can choose any direction (map view) for full view. Full view includes spot mark where the user current location is and where his destination is with full-size map photo. Every time user chooses any of locations to browse corresponding
Event should be added to statistics journal. This event should also include what recipe was browsed.
7. Print a map. User can print out the map or direction using thermal printer connected to the kiosk. Information to be printed is full map description. Printing of map (direction) should be recorded in statistics journal and record will contain what direction was printed.
8. Email map : user can send the map showing his journey path to his email address by choosing  the email action button and one again he can re type or edit his email address by pressing the edit email button and send the map to his email account.
9. Send map to phone: the user can send the map to a his phone by entering his phone number by entering his phone number on the phone number typing bar after pressing” send to phone button”.

10. Browse daily event (news). At any moment of time user can browse information about system updates, place where terminal located, etc. Each piece of such information, news for simplicity, will have along with content start and end dates to be displayed. Also news will be assigned to one or more terminals, on which they should be shown. Every time when user chooses news to be displayed corresponding event has to be written to statistics journal.


Administrator's use-cases
The administrator can use any personal computer for accessing administration functionality, but this functionality should be protected from unauthorized access.
2.1. Login to administration area. Whenever the administrator wants to use service he has to provide authentication information in form of User name and password. However he doesn’t have to log in whenever he has to done something. Once logged in his session should last until administrator logs out.
2.2. Browse list of locations. Administrator can get list of all locations stored in database with possibility to filter out list by department directory or and shop and dinning. Location list will contain only location name to be able to show more directions on screen.
2.3. Add location to database. Administrator can add new location to Database at any moment. For adding a new location he has to enter its description, edit the name of the location and select appropriate categories. (Determine whether the specific location is in the department, room or shop category)
2.4. Edit location in database. During browsing location list administrator can choose any location for editing. When he does it direction will be shown in full view – title, description, categories, with possibility to edit update any of these components. When updates are made administrator can save them in database.
2.5. Remove database. When administrator browses the location list (Use-case 2.2) he can choose any of them for deletion. But before location will be deleted from database administrator must confirm it once again. After confirmation location will be erased from database permanently.
2.6 add route path (direction map): If the admin add a new location, edit, or delete in (case 2.4, 2.5, 2.6)he has to update the direction map for the newly added location or edit the map for the edited location. For example, in case of an elevator broke down the route path might be different one from the one that has already been made.
2.7. Browse list of “daily events”. Administrator can get list of “all daily event” stored currently in database. News list will contain news title and description, time period, when news will be displayed, and terminals, where news will be shown.
2.8. Add news to database. Administrator can add news to database at any moment. For adding news he has to enter its title, description, choose period, when it should be displayed, and select appropriate terminals, where news will be shown.
2.9. Edit (daily event) news in database. During browsing news list administrator can choose any “daily event “and edit it. When he does it all parts of news will be shown – title, description, terminals and time period, with possibility to edit update any of these components. When updates are made administrator can save them in database.
2.10. Remove “daily event “from database. When administrator looks through news list (Use-case 2.6) he can delete any event that doesn’t occur at that date or outdated. But before news will be deleted from database administrator must confirm it once again. After confirmation news will be erased from database permanently.
2.11. Browse list of terminals. Administrator can have the access to any terminal connected to the system. For each terminal there should be information if terminal is working currently or not.
2.12. Browse terminal's statistics. While browsing list of terminal administrator can choose any terminal to browse detailed information about. This information can include place where terminal is located and statistical data of terminal's use. Administrator can choose period for which statistics should be calculated. Statistical data will include how many people used terminal, what directions where browsed and what directions were printed.
fig: use case diagram
 
 









3. System archtecher
3.1. High-level overview of the system
The UL class diagram below is a description of high-level components responsible for required functionality and associations between these components.it represent the logical view on architecture
3.2. Main modules and their functions represented







 


Figure: class diagram
Structure above narrowly looks like model-view-controller (MVC) architectural pattern.
The Model contains three components: direction Service, Terminal Statistics Service and daily event Service. This part is responsible for management data recovery and alteration activities.
View part is represented by direction UI, daily event UI, Administrator UI and Print Utility, email utility.
These tablets provide data presentation functionality both on screen and printer. Direction UI decreases interfaces for direction search, search results and direction itself, however it is not providing means for direction management: addition, update or deletion. Direction controlling interfaces are included in Administrator UI. Administrator Ul is in charge for daily event management user interface and displaying statistical data. Daily event UI is responsible for showing daily event and navigating through them.
Other middle components – Kiosk Controller and Administrator Controller –control data flows between model and view parts. They are supposed to handle user inputs and send appropriate message to model. After responses from model received controllers update view depending on information contained in them.
Main task of Administrator Controller is executing authentication and authorization functionality before administrator can use rest of its services. Direction, Log Event, Terminal and News components on the top of diagram correspond to data entities used for informational exchange between view, controller and model and they are depicted with more details later on in data view.
Regardless of that class diagram is used for representing logical view in reality components shown on it can be implemented using several programming language classes. And to keep the diagram simple only large significant components are shown.









2 User Interface

User interface prototype
These figures below are drawings of user interface at different circumstances of the system. when the full page is reloaded, and it means that prototypes below are not designs of separate web pages, but rather screen-shots of user interface during system usage and only some subclass of interface elements are updated, added or removed, while whole interface stays consistent and user gets all-in-one experience of interface functioning.
Image 1:image1 is the initial page, which user sees when he starts using kiosk.
User can see the initial page comes with a women(audio assistant ) image in the top and  Three buttons o listed in column used to switch between” department browsing” and room, “shop and dinning” search options. At the very bottom of the page there is a detached bar containing the daily event search button. The interface comes with a recorder sound guide asking the user what he wants to do.
Image 2: Search by Department: when the user chooses the option to find a location by department the interface will appear as in “image 2”which will have the list of departments listed down, with down and up arrows buttons  on the left  assisted to browse the user the specific department he wants to choose. Once the user found and click the department of his chooses the link bar having the department name will turn into blue and the department will be taken as the user’s final destination automatically.
Image 3: once the search is done, the next page will appear with a full map image indicating the whole direction path. The map has a spot (a red button locating the current location of the user), and green button indicating the final destination of the user. The route path is drawn between this spots on the map. The map image will appear at the middle of the page beneath that there are two option buttons indicating the walking distance and time. However the audio assistant will also address the walking distance the description of the route path verbally.
At the very bottom of this page there are department, room, shop and dinning option buttons that will redirect the user to another new search using the other options. This buttons are the ones that appear at the initial page of the system.
At the left edge of the page the print action option and email option buttons are placed.
The back option button at the bottom will redirect us to the earlier page.
Some elements of user interface are common and should be displayed regardless .All contents and description that will appear in the image 3 will appear for room or shop and dinning search options except the search is room or shop.(print,email,back)
Image 4: this interface will appear whenever we want to email direction (map) from any page. Email address entry bar to enter your email address , send option to send the map to your email once you finished putting the address, edit option to edit the address that has been typed.
Send to phone: the interface appear In order to send map to your phone the phone must have turned on blue-tooth. Phone number entry bars to enter your phone number; send option to send the map to your phone.
Image 5: this image will occur when user chooses the “daily event button”. In the center of screen user sees image related to the “daily event “news. At the top the page contains the event tile and description. If concatenated news titles and descriptions cannot fit screen then this text is split to pages and user can use two buttons on the left and right side to move between available pages.

Image 12: News view screen 

Hayat Hospital

What would you like to do?

 
What would you like to do?
find a room or desk

department directory

shop and dinning

daily event (news)
      yoga exercise at: 8:30
image:1


Hayat Hospital
 DEPARTMENT DIRECTORY


DENTAL                    detail                        floor

EYE CLININC       ……………………………………………………..3rd

radiology……………………………………………………………….4th

audiology ……………………………………………………………..1st

agent casher………………………………………………………………………….1st






	















image:2



Print
Direction map
map image

email
Walking distance: 0.5km
walking time: 4min
Find a room
Department
Shop and dinning
Back

enter emali adrress



send 



edit email

BACK


Image:4

Daily event : yoga exercise at 8:30 in the physiology department room n0.13


image


Image: 5
3. System requirement
Functional requirement

• The user of developed system has two options for search for direction: by department, room/desk or shop and dinning, Such as radiology department. The three search options should be easy to understand and use – users should not be required to execute complex sequences of actions to get result.
• When the search is done, the user gets resulting list of directions and then he can choose any of the directions from the list and browse it with more details on the screen.
• Directions will contain following basic parts that should be displayed:  walking distance, time it takes, direction path starting from the kiosk terminal up to the chosen destination, description and map. During browsing through direction user should have possibility to return back to search result.
• If the user wants he can print the map using thermal printer connected to terminal. 
• If the user wants he can email or send the map to his phone.
• When system is not used by anyone, the general blue print of the whole building should be shown; news of the day should be displayed: 
• Sometimes news about place where kiosk located, information about system updates, new functionality or any other kind of news will be announced and the user should have ability to browse this information.
• User interface should be attractive, consistent and simple for use, because the most of the kiosk users will be inexperienced computer users. The most of the actions should be possible to execute using 1-2 'touches'.
• The user should be prohibited from accessing any kiosk functionality but one described in this specification, for examples users can't launch any other applications or have access to files on the terminal.
• The application will use some audio messages to attract people to use it and help them to understand purpose of kiosk. This message should be played periodically when someone is using the system.
• Many terminals can be used simultaneously from different places and they should operate on the same directions set.
• Statistical data of the number of people have used the terminal and what directions they have looked through and printed must be collected. To count   the number of new users the system should use timeout – if no actions were executed during some period of time since last action then system considers new action completed by new user.
• There should be additional utility for administration purposes – adding, editing and deleting directions when conditions change, like an out-of-service elevator or closed hallway. And news, viewing statistical data;
• The utility for administration use should be protected from unauthorized access by means of user-names and password requirements
4.1 Usability 
The interfaces are very straight and simple to use. The map simply spots your current location; draw the path that you follow until you reach your destination. The system spots facilities, stairs, and emergency exits with icons and explain them. Make rest-rooms stand out (more often than not, the first thing visitors will look for when they enter your building). The maps will give a better sense of space, distance and direction.
The direction is signified by buttons. Make them large, the text self-explanatory and present them clustered in a designated area, the audio guide makes the path easier to understand, even if we were unable to understand the path from the map. Above all the audio will help for disabled patients, have eyesight problem and the user can be sited and able to the kiosk
4.2. Reliability
These applications interface, stop users from changing the configuration of software or downloading computer viruses.it provides a 24, 7 services, and includes a fully-fledged digital signage system. : improved patient-flow, an increase in on-time appointments, more efficient use of staff time, decrease costs and a significantly boosted patient experience, all at a cost far less than you would pay a single FTE.
4.3. Efficiency
4.4. Other Non-functional Requirement
• The project has low budget and no additional cost should be paid for any used software;
• due to technology low budget it also preferable that amount of the Internet traffic must be as small as possible;
• The kiosk system will be commercial, so the project is not open-source and the source code cannot be published;
• The kiosk system is not the first project for the company, that is why there are   legacy systems or constituents that must be used and application cannot be developed using any programming languages, components and tools with regards to other requirements and constraints.
The customer didn't put exact time constraints for the project operation, but roughly it was set to 6-8 month for the first working implementation.
 The customer had a previous experience with an electronic kiosk system however we didn’t had.  and the requirements specification is produced in the general procedure with many required details left undiscovered. However during the development process some of the requirements were developed especially hardware configuration. And above is the final version of the customer requirements was given.
2 Project Management
 In order to prepare this documentation it took us more than 60 hours, probably each person take 20 hrs. And the most difficult part was to decide on which system should we take as our project because the way finding system has both a web based application that could be run on Pcs and the kiosk terminal ,which we consider now. We were about to write about the web based app however we found it having too much details and with the time that we had we found It better to take this system. We almost write for both options and that’s way we had to linger on the project submission deadline. However to be genuine we didn’t start the project in time we promised ourselves not to rush when another project came up.
