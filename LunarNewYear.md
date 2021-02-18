
### Create a database for user registration, which include the *necessary* information for a user of a generic application. 
1. Draw the ER diagram


2. Create the SQL script to create the database and add some sample users

```py 
CREATE TABLE IF NOT EXISTS userInformation(
    ID INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
    email varchar(150) NOT NULL,
    userame varchar(50) NOT NULL,
    password text NOT NULL

);

INSERT INTO userInformation(email, userame, password)
VALUES  ('2022.isabel.andreatta@uwcisak.jp', '2022isabel', 'verysecret');

INSERT INTO userInformation(email, userame, password)
VALUES ('2022.abraham.lincoln@uwcisak.jp', 'HonestAbe', 'Democracy!');

INSERT INTO userInformation(email, userame, password)
VALUES ('jj@uwcisak.jp','woofwoof','imadog');

``` 

1. Create the UML class diagram for the db


2. Create the database using ORM and add some sample users


3. Research what Hash functions are and think how they could be used to improve the security of the private data in the database.

Hash functions are functions that convert any length input into fixed-length encrypted string. This is very valuable to secure a database because vulnerable information, because usually hash values are always unique and hard to interpret (no matter if a novel or word, they will always result in the same length value so hackers will not know the actual length of the original input), the brute force method of "decyphering" a hash value makes it almost impossible because of the high computational power and time needed. 
