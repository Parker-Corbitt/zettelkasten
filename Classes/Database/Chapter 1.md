***
#### <u>Characteristics of Databases and Database Users</u>
###### Definitions
- *Database*: A collection of related data
- *Data*: Known facts that can be recorded and have an implicit meaning
- *Mini-World*: Some part of the real world about which data is stored in a database
	- An example of this are transcripts of students at a university
- *Database Management System (DBMS)*: Software package / system used to create and maintain a database
- *Database System*: The DBMS software together with the DB, and sometimes applications

##### Properties of Databases
- Representation of a section/aspect of the real world
- Data is logically coherent and has some form of meaning
- Designed, built, and populated with a specific purpose in mind
- Built with a target audience / group of users in mind

##### Applications of Databases
- General Numerical / Textual databases
- Multimedia databases
- Geographical information system
- Data warehouses

##### Affects of Databases
- *Businesses*: Banking, Insurance, Retail, Transport
- *Service*: Real-estate, Legal, E-Commerce
- *Big Data*: Social Networks, Environmental & Scientific applications
- Various customized applications can take advantage of many general functions

##### Database Functionality
- *Define*: Set in place data types, structure, and constraints
- *Construct*: Loads the initial DB contents on to a storage medium.
- *Manipulate*: Retrieve, modify, and access data
- *Process & Share*: Able to be done at the same time by many users while maintaining data integrity
- *Protect*: Keeps the data protected from unauthorized access
- *Present*: Provides visualization capabilities for end users to view the data

##### Database Application Interactions
- *Queries*: Access various parts of a database, and formulate the results of the request
- *Transactions*: Read and update certain values, or even generate new data

##### Characteristics of DBMS
- *Self Describing Nature*: Typically signified by a catalog, which itself stores the description of the database (types, constraints, etc)
	- Said description is called meta-data
	- Allows for increased ease of use when working with other DB apps
- *Program-Data Independence*: A concept describing the insulation between the catalog, and the programs that access it
	- This allows for the changing of structures and storage organization without having the change the access applications
- *Data Abstraction*: Done with a data model, which hides storage details, and presents the users with a conceptual view of the data
	- Programs refer to the conceptual views, and not directly to base storage.
- *Multiple Data Views*:  Each person should be able to create their own view, only with information that matters to them
- *Sharing of Data*: Should allow for concurrent multi-user access, providing control for transaction flow in order to ensure data integrity

##### Database Users
- *Database Administrators*: Handles authentication, access, monitors user activity, acquires resources, and monitors how various apps perform
- *Database Designers*: Defines the constraints, structures, content, functions, and transactions able to be made against the database. *Must communicate with end users!*
- *End Users*: Use the database to primarily make queries, along with other types of operations
	- Casual: Only occasionally access database, for relatively small tasks
	- Naive: Not quite ignorant of the capabilities of the database, but very close  to being so
	- Advanced: Able to use personal databases to an efficient degree, such as tax software
	- Sophisticated: Familiar with the capabilities of a database, and frequently use DB related packages
- *BTS*: DBMS designer & implementer, tool developer, maintainer

##### Implications of Databases
*Advantages*
- Able to easily control redundancy on both storage and development sides
- Management of authentication is much easier
- Provides a general increase in efficiency (if well implemented)
- Provides easy access to backup, recovery, and presentation tools
- Enforces integrity constraints & general standards in a more manageable way
- Drastically increases availability of information

*Disadvantages
- High initial investment
- Overhead of understanding the DMBS and related programs can be substantial
	- Especially if implementation is clunky
- Unavailable for use in embedded systems due to significant overhead
