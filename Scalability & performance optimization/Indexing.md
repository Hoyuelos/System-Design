
<h1> Indexing </h1>

An effective indexing strategy can be a game-changer for your database queries by making data retrieval faster and more efficient. <br>

<ul>
<li>   `Index Types`: B-Tree, Hash, Bitmap </li>
<li>    `Usage Scenarios`: Optimal situations for each index type </li>
<li>    `Trade-offs`: Speed vs. storage considerations </li>
</ul>

<h2> Types of Indexes </h2>

<ul>
<li> <b>`B-Tree Indexes` </b>: Good for range queries and ordered data. </li>
<li> <b>`Hash Indexes`</b>: Fast for exact matches, not suitable for range queries. </li>
<li> <b>`Bitmap Indexes`</b>: Ideal for columns with low cardinality, like gender fields. </li>
</ul>

Each index type serves different purposes. B-Tree indexes, for instance, are versatile and work well with range and equality queries. In contrast, Hash indexes excel in quick retrieval by exact key matches but aren't suitable for range queries. Bitmap indexes are efficient for data with low cardinality and are usually employed in data warehousing for analytics. <br><br>

B-Tree indexing is highly efficient for retrieving data within a range, which is often required in scenarios like fetching records between dates or price ranges. Hash indexes are better suited for scenarios where precise data retrieval is needed, without needing range lookups. Bitmap indexes, meanwhile, excel in situations dealing with low-cardinality data, such as gender or binary states. <br><br>

When you're looking for an exact match, like retrieving employee information by ID, a hash index optimizes the search process by mapping each ID directly to its data row, making lookups lightning-fast. <br><br>


<h4> B-Tree index </h4>

<p>They are designed to maintain a balanced tree structure where nodes contain keys and pointers. As data is inserted or deleted, the tree remains balanced, allowing operations to access data in logarithmic time. This makes B-Tree indexes optimal for handling range queries efficiently. </p>

<h4> Hash Indexing </h4>

<p> Hash indexes map data using hash functions. This process provides efficient access for exact match queries by directly linking hash values to the corresponding records. However, since hash indexes do not maintain order, they are not useful for range queries. </p>

<h4> Bitmap Index </h4>

<p> Bitmap indexes use bit arrays to represent unique values, allowing efficient representation of data. They are excellent for performing operations like AND, OR, and NOT on low-cardinality columns with minimal computational cost. </p>