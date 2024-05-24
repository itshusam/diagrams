1-4
First Normal Form (1NF): Each table has atomic values, and there are no repeating groups. For example, the Books table has separate columns for title, genre, and publication year, ensuring atomicity.

Second Normal Form (2NF): Each non-prime attribute is fully functionally dependent on the primary key. In the Books table, the genre and publication year depend only on the book_id, which is the primary key.

Third Normal Form (3NF): There are no transitive dependencies. For example, in the Transactions table, quantity and total_amount depend only on the primary key (transaction_id), and not on any other non-prime attributes.

Overall, the schema design adheres to the principles of normalization by structuring data to minimize redundancy, eliminate anomalies, and ensure data integrity. Each table serves a specific purpose, and relationships between entities are established through foreign keys, ensuring efficient data retrieval and manipulation.



2-4
New Vehicle Additions: When a new vehicle is added, a record is inserted into the Vehicles table. Since each vehicle has exactly one rental agreement, initially, there won't be any corresponding records in the Rental_Agreements table for the new vehicle. When a rental agreement is made for the new vehicle, a record will be inserted into the Rental_Agreements table with the corresponding vehicle_id.

Rental Agreement Updates: If a rental agreement needs to be updated, such as extending the rental period or modifying the rental fee, the relevant record in the Rental_Agreements table can be updated without affecting the Vehicles table. This ensures that changes to rental agreements do not impact vehicle details.

Vehicle Availability Checks: To check the availability of a vehicle, the system can query the Rental_Agreements table to see if there is an active rental agreement for the vehicle in question. If there is no active rental agreement (i.e., the vehicle is not currently rented out), it is considered available for rent. Conversely, if there is an active rental agreement, the vehicle is not available for rent until the rental period ends.
