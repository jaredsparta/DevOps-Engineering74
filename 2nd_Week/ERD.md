# ERD or Entity Relationship Diagrams

**Components**
1. Entities
    - The nmber of tables you need for a database.
2. Attributes
    - Information such as property, facts you need to describe each table.
3. Relationships
    - How entities are linked to one another.

<br>

**Entities**
- These form the tables in a database.
- They are nouns and can usually be split into: concepts, locations, roles, events or things.
- A specific example of an entity is called an instance; every instance is a row in the table.

<br>

**Relationships and Cardinality**

![Relationships](images/erd.png)

1. ONE-TO-ONE (1:1)
    - A single entity instance is related to a single entity instance in another entity class.
    - e.g. a student is assigned one seat and one seat is assigned to only one student.

2. ONE-TO-MANY (1:N)
    - One entity instance is related to multiple instances in another entity class.
    -  e.g. a student is assigned one lecturer but a lecturer is assigned many students.

3. MANY-TO-MANY (N:N)
    - Each entity instance is related to many instances in another entity class and vice-versa.
    - e.g. a customer can buy many products in a store and a product can be bought by many customers.

- It is common to represent N:N relationships via two 1:N relationships since they are hard to represent.






---
**Used:**
- [ERD's](https://www.cs.uregina.ca/Links/class-info/215/erd/)