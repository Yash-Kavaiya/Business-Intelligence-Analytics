# NORMALISATION

You're absolutely right! Normalization in SQL is a crucial process for designing a database effectively. It helps to avoid data redundancy and anomalies during data operations like insertion, deletion, and updating. Here's a bit more detail:

- **Data Redundancy**: This occurs when the same piece of data is held in two separate places. It's not only a waste of storage space, but can also lead to inconsistencies.

- **Insertion Anomalies**: These occur when certain attributes cannot be inserted into the database without the presence of other attributes. This is a problem because it should be possible to insert any attribute into the database without the presence of any other.

- **Deletion Anomalies**: These occur when certain attributes are lost because of the deletion of other attributes. This is a problem because it should be possible to delete any attribute without losing any other.

- **Update Anomalies**: These occur when certain attributes are updated, leading to inconsistencies within the database. This is a problem because it should be possible to update any attribute without affecting any other.

LEVELS OF NORMALISATION
Pallaptor
• Database normalization is the process of decomposing relat
produce smaller, well structured relations
1st Normal form: Multivalued attributes (repeating groups)|
2nd normal form: Partial dependencies addressed
3rd normal form: Transitive dependencies addressed (golde
normalisation)
Boyce/Codd NF, 4th NF and higher normal forms do exist
Trade off: Efficient storage space vs efficient data processing→ De-normalizatior

1 NF
• If your DB not even in INF→ Then poor DB design
• NO multivalued alibutes
• A column should have values of same type
• Each column should have unique name
• Order in which you slore data doesn't malter

2NF
• For a table to be in the Second Normal form, it should be in the First
Normal form and it should not have Partial Dependency.
Partial Dependency exists, when for a composite primary key, any
attribute in the table depends only on a part of the primary key and
not on the complete primary key.
• To remove Partial dependency, we can divide the table, remove the
attribute which is causing partial dependency, and move it to some
other table where it fits in well.
PRIMARY KEY AND PARTIAL DEPENDENCY
• PK- can uniquely identify each row of the
table
• Student_id + Subject_id is the PK but here
teacher's name depends only on the
subject (This is Partial dependency)
• How to remove PD? Move teacher's
name to subject table or create a table of
teacher with name and id → 2NF

3 NF
• Should be in 2nd NF
• Should not have Transitive Dependency
• TD is when there is an attribute in a table which depends on a non prime attribute and
not on a prime attribute
• All non prime attributes should depend only on prime attributes


Boyce-Codd Normal Form (BCNF) is a stricter version of the Third Normal Form (3NF). A table is in BCNF if, and only if, for every one of its dependencies X → Y, X is a superkey—that is, X is either a candidate key or a superset thereof.

Let's break down the terms you mentioned:

- **Prime attribute**: An attribute that is part of a candidate key.
- **Non-prime attribute**: An attribute that is not part of any candidate key.
- **Functional Dependency**: A constraint between two sets of attributes in a relation from a database. If A → B, then if we know the value of A, we can determine the value of B.
- **Partial Dependency**: A type of functional dependency where a non-prime attribute is functionally dependent on part, not all, of a candidate key.
- **Transitive Dependency**: A type of functional dependency where a non-prime attribute is functionally dependent on another non-prime attribute.

In BCNF, for any dependency A → B, A should be a superkey. This means that a non-prime attribute (A) cannot determine a prime attribute (B). This rule helps to eliminate redundancy and update anomalies.

Here's an example of a table that is in BCNF:

| StudentID (A) | CourseID (B) | Grade (C) |
|---------------|--------------|-----------|
| 1             | CS101        | A         |
| 2             | CS101        | B         |
| 1             | MATH101      | C         |

In this table, the dependencies are:

- StudentID, CourseID → Grade
- StudentID → CourseID
- CourseID → StudentID

For each of these dependencies, the determinant is a superkey, so the table is in BCNF.

I hope this clarifies things! Let me know if you have any more questions. 👍