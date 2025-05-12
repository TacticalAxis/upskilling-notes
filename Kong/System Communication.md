Communication is about:
- sending data
- receiving data

Multiple ways to communicate:
- Getting data: A gets weather data from B
- Sending data example: X sends sales transaction data to Y

One way is using a text file (using CSV):
B privides weather data in CSV daily in a folder on the server
System A then retrieves data from that CSV and processes it according to its requirements

X sending data means sales transactions occur on X
X provices sales data in CSV everyday at midnight
X sends data to fileserver on Y so Y can process it

Another way is Database to Database
A database has read access to weather table on B database
So A can directly query data from B table

In sending data, the source system can write to certain tables in the destination system
This is called staging table or an interface table

Y has sales_transaction table where data can only be accessed by Y
it also has sales_staging table where X can insert data into
A scheduler on Y will automatically fetch data from sales_staging and insert into the real table (sales_transaction)
Incorrect data wont be added to the real table, but instead just marked as incorrect on staging table

THis approach is typically used in olrder systems


Another way is through REST APIs (Representational State Transfer)
Get data example:
B provides weather API
Weather API is something A can query
A access rest API instead of database
A doesnt need to know how B fetches the waether data
As long as A knows the URL, A can get the weather data

FOr Sending Data:
Y provides api to accept sales transactions
WIth correct endpoint and auth, X posts data to Y endpoint



