# Normalization

Normalization is a process in database design used to organize a database into tables and columns in such a way that it reduces data redundancy and improves data integrity. The process involves decomposing a database into smaller, related tables and defining relationships between them to eliminate undesirable characteristics like insertion, update, and deletion anomalies.

Normalization typically involves applying a series of rules, known as normal forms, to ensure that the database structure is optimal. These normal forms are:

1. **First Normal Form (1NF)**:
   - **Definition**: A table is in 1NF if all its columns contain atomic, indivisible values, and each column contains values of a single type. Additionally, each column should contain only one piece of information.
   - **Identification**: To ensure a table is in 1NF, verify that each table has a unique primary key and that every cell contains only one value (no repeating groups or arrays).

2. **Second Normal Form (2NF)**:
   - **Definition**: A table is in 2NF if it is in 1NF and all non-key attributes are fully functionally dependent on the entire primary key. This means that there should be no partial dependency of any column on the primary key if it is composite (consists of more than one column).
   - **Identification**: Eliminate any partial dependencies by removing the columns that depend only on a part of the composite primary key and placing them in a separate table.

3. **Third Normal Form (3NF)**:
   - **Definition**: A table is in 3NF if it is in 2NF and there are no transitive dependencies. A transitive dependency occurs when a non-key attribute depends on another non-key attribute rather than depending directly on the primary key.
   - **Identification**: Check that non-key columns are not dependent on other non-key columns. If they are, move them to a new table where they can depend on the primary key.

4. **Boyce-Codd Normal Form (BCNF)**:
   - **Definition**: A table is in BCNF if it is in 3NF and every determinant is a candidate key. This means that for every functional dependency X → Y, X should be a superkey.
   - **Identification**: Ensure that for any functional dependency, the attribute determining other attributes is a superkey.

5. **Fourth Normal Form (4NF)**:
   - **Definition**: A table is in 4NF if it is in BCNF and contains no multi-valued dependencies, which occur when one attribute in a table uniquely determines another attribute.
   - **Identification**: Remove any multi-valued dependencies by separating the tables so that each attribute pair that can be independently associated is separated into its own table.

6. **Fifth Normal Form (5NF)**:
   - **Definition**: A table is in 5NF, also known as Project-Join Normal Form (PJNF), if it is in 4NF and cannot be decomposed into smaller tables without loss of information.
   - **Identification**: Ensure that decomposing the table into smaller relations would not lose any data requirements or introduce new join dependencies.

7. **Sixth Normal Form (6NF)**:
   - **Definition**: Though not widely used and more theoretical, it deals with temporal databases and ensures no non-trivial constraints exist other than candidate key constraints.
   - **Identification**: Focuses on making every relation variable contain values irreducibly by time or other continuations of conventional data.

By following these normal forms, databases can be optimized to eliminate redundancies, ensure data integrity, and efficiently manage data storage and retrieval.  
