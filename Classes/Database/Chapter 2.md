### <u>Database System Concepts and Architecture</u>

##### Entity Relation Model Concepts
- *Entities* : Specific things or objects in the mini-world, able to be represented within databases
- *Attributes* : Properties used to describe an entity
	- Single/Atomic : Only one value per attribute
	- Composite : Composed of attributes of its own
	- Multi-Valued : More than one value per attribute
	- Derived: Able to be calculated from other stored data

##### Keys
- A uniquely identifiable attribute, minimally so
	- Can be composite attributes, and each entity may have more than one key
- *Super Key* : Can contain non-unique attributes, but when paired with certain other values, can make a key
- All keys are super keys, but not all super keys are keys

##### Relationship  Types
- *Relationships* : describes the connection of two or more entities, and can have attributes
- The degree of the relationship is how many entities participate in said relationship
- *Cartesian Product* : All possible associations of entities within the entity set
- *Recursive* : Both participants have the same entity type in different roles
	- EX : Employees and supervisors. Supervisors are also employees.

##### Weak Entities
- *Weak Entity* : Does not have a key of its own, and such must participate in an identifying relationship with an identifying entity

##### Constraints
- Help maintain integrity within a DB
- Two types
	- Cardinality Ratios
	- Existence Dependencies

*Cardinality Ratios*
- One to One (1:1) : An entity in one set is associate with at most one entity in another set
- One to Many (1:N) : An entity in the first set is associated with *N* entities in another set
- Many to One (N:1) : *N* entities in the first set can be associated with one entity in another set
- Many to Many (N:M) : *N* entities in the first set can be associate with many entities in another set

*Existence  Dependencies*
- Dictate if an entity in one set must be related to an entity in another set
- If an entity must be related, it has total participation in said relationship (ATM cards to Bankers)
	- If not, partial participation is designated (Bankers to ATM cards)