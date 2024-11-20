

<h1> First Normal Form (1NF) </h1>

<ul>
<li> 1NF helps us eliminate duplicate columns from a table and sets the stage for efficient data management. </li>

<li> In First Normal Form, we aim to ensure that each column contains atomic values—meaning they can't be divided further—and there are no repeating groups of data within a table. Columns should have unique names, and rows should be unique, often managed with a primary key. <br> 

let's say you're using a table called `Orders` to record every customer purchase. If each 'Item' field in your table can contain multiple Item IDs separated by commas for a single order, you're not in 1NF. The goal is to keep each value atomic—that is, singular and indivisible—so each entry in the 'Item' column should host only one Item ID.
</li>

<li> Splitting data into atomic values helps simplify queries and optimizes database performance. Doing this aligns the database with 1NF by making each entry atomic. </li>

<li> The concept of atomic values helps simplify database operations, making it easier to query, index, and update data. </li>

<li> When values are non-atomic, it complicates indexing and makes the database less efficient for querying. In 1NF, atomic values ensure that each piece of data is clearly identified and can be indexed optimally. </li>

</ul>

To summarize, First Normal Form ensures atomic values, unique names, no repeating groups, and unique rows. This is essential for efficient querying and database design.


<h1> Second Normal Form (2NF) </h1>

<ul>
<li> It's an important concept in database normalization, ensuring that relational databases are structured efficiently by eliminating partial dependencies of attributes on non-prime attributes. </li>
<li> To transform a table into 2NF, we begin by ensuring it is in 1NF. Then, we eliminate partial dependencies. This means any column that doesn't depend entirely on the primary key should be moved to a separate table. </li>

<li> Partial dependencies happen when attributes rely on just a part of a composite key. This can cause data to be duplicated across rows, leading to inefficient use of storage and increased chance of data anomalies. Understanding and eliminating these helps achieve 2NF. </li>

for example - Partial dependencies are like when you have a table with a composite key, say (A, B), and a column depends only on A or only on B, rather than (A, B) together. This can cause unnecessary repetition of data.

<li> To summarize, Second Normal Form (2NF) ensures that non-prime attributes are fully dependent on the whole primary key, eliminating partial dependencies. This helps reduce redundancy in the database.  </li>
</ul>

<b>Example</b> - Consider the table, where `EmployeeID` and `DepartmentID` together form the composite primary key. The `DepartmentName` depends only on `DepartmentID`, not the whole key. This creates a partial dependency, violating 2NF. <br>
In this scenario, since 'DepartmentName' depends only on 'DepartmentID', it leads to repeated storage of department names. This redundancy could be eliminated by creating a separate Department table with DepartmentID as the primary key and linking it using a foreign key. <br>
To resolve the partial dependency, we can split the table into two: 'EMPLOYEE' for employee details and 'DEPARTMENT' for department details. By linking them through DepartmentID, department information is no longer repeated across multiple employee records.



