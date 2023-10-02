## Date: 9 - 27 - 23

###### PRE-MEETING PREP

A more broken down and comprehensive list of requirements based on feedback we received from the client:

**Verification and Permissions**
- Authenticate user's via. Ohio University account.
- 3 tiers of USER permissions, **admin** who can edit or add rooms to any building, add new buildings, and add new building admins, **building admin (BA)** who can edit and add rooms within a building, and a **user** who can only view rooms.

**UI/UX**
- List rooms and buildings in a mobile-friendly view, preferably with some type of route or map view.
- Indicate the status of the room with a color-scheme, including whether or not its available, if its occupied, and potentially how many people are inside.
- Indicate the type of room, such as study room or office space.
- Allow user to favorite/unfavorite rooms and view their favorites.
- Allow user to view history of rooms clicked on / viewed.
- Allow user to set up notification when a room changes status.
- Allow (building) admins to "reserve" a room so that its status updates during certain times automatically. (e.g: 6pm - 6am unavailable, otherwise available)

**Server & Hardware**
- Automate status updates from the sensors across the server and interface.
- Create a database to store information about rooms. (status, created by, building, etc.) and users (favorites, permissions, etc.)
- Use microcontroller or microprocessor to send data from pins in sensors to a central server.
- Create an API for handling requests that interact with both the database and the interface.
- Create a program to process data from the sensors to gather specific data such as people count, exiting/entering, door open/closed, etc. (could be done on microcontroller/microprocessor)
***
**Agenda**
- Draw updated FlowChart on whiteboard, that shows where every piece of the tech stack comes into play, how they interact with each other, and what they *do*. Additionally, writing down/indicating who is working within which pieces of the flow.
- Curate a list of updated requirements for the app, taking reference from client meeting feedback and the current requirements.
- Discuss SRS Document and fill out some information that we already have.
-  Discuss potential first sprint starting points and/or milestones.

**Attended:** ALL TEAM MEMBERS PRESENT

**Started:** <t:1695845220:R>

**Ended:** <t:1695849320:R>

**Goals:**
Parker - SRS Work
Damon - Environment setup & testing
Jude - Environment setup & testing
Asa - Environment setup & testing


# Date: 10 - 1 - 2023

**Agenda**
- Review SRS document. Discuss and fill out parts that are still left in template form, and review parts that have been filled out. Revise as needed.
- Revisit test environment progress
- Any additional Correspondence to Naseef Other than webhook and PI?

**Attendance**: **ALL MEMBERS ATTENDED**

**Meeting Start**:  5:10

**Meeting End**: 6:20

**Goals**
- General: Continuing SRS document
- Parker: Set up a couple programs, one to report occupancy and the other to read that information  and send it via MQTT
- Asa: Make diagrams for data models and backend flow
- Damon: Pick a software for prototyping UI for  3 types of flow, continued environment testing
- Jude: Dockerizing the communication services and CSM