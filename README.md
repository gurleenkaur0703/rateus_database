# RateUs Database
## Database Schema 
### Creating the RateUs Database
```
CREATE DATABASE RateUs;

USE RateUs;
```
### Creating the Organisation Table
```
CREATE TABLE Organisation(
    Org_ID varchar(10) PRIMARY KEY,
    Org_Name varchar(200),
    Owner_id varchar(10),
    Logo varchar(100),
    Org_Address varchar(200),
    Listed_On DATE DEFAULT CURRENT_TIMESTAMP
);
```
### Creating the User Table
```
CREATE TABLE User_(
    User_ID varchar(10) PRIMARY KEY,
    User_Name varchar(100),
    Email varchar(200),
    Contact varchar(12),
    Password varchar(300),
    Created_ON DATE DEFAULT CURRENT_TIMESTAMP
);
```
### Creating the Items Table
```
CREATE TABLE Items(
Items_ID varchar(10) PRIMARY KEY,
Item_Name varchar(100),
Org_ID varchar(10),
Added_On DATE DEFAULT CURRENT_TIMESTAMP
);
```
### Creating the Reviews Table
```
CREATE TABLE Reviews (
    Review_ID VARCHAR(10) PRIMARY KEY,
    Org_ID VARCHAR(10),
    Item_ID VARCHAR(10),
    Review VARCHAR(100)
);
```
### Creating the Ratings Table
```
CREATE TABLE Ratings (
    Rating_ID VARCHAR(10) PRIMARY KEY,
    Item_ID VARCHAR(10),
    Rating VARCHAR(10)
);
```
### Creating the Aggregate_Ratings  Table
```
CREATE TABLE Aggregate_Ratings (
    Item_ID VARCHAR(10) PRIMARY KEY,
    Rating VARCHAR(10)
);
```
### Creating the Sentimental_Scores Table
```
CREATE TABLE Sentimental_Scores (
    Review_ID VARCHAR(10) PRIMARY KEY,
    Sentimental_Score VARCHAR(100)
);
```
## Database Queries
### Inserting User Details
```
INSERT INTO User_ (User_ID, User_Name, Email, Contact, Password) 
VALUES ('enter_UserID', 'enter_Name', 'enter_Email', 'enter_Contact', 'enter_Password');
```
### Inserting Organisation Details
```
INSERT INTO Organisation (Org_ID, Org_Name, Owner_ID, Org_Address) 
VALUES ('enter_OrgID', 'enter_OrgName', 'enterOrg_OwnerID', 'enter_OrgAddress');
```
### Fetching User Details by Email
```
SELECT User_ID, Contact, Password 
FROM User_ 
WHERE Email = 'backend_provided';
```
### Retrieving ID and name from Organisation by Org_Name='search%'
```
SELECT Org_ID, Org_Name 
FROM Organization 
WHERE Org_Name LIKE 'search%';
```
### Inserting Items Details
```
INSERT INTO Items (ID, Item_Name, Org_ID) 
VALUES ('Enter_ID', 'Enter_Item', 'Enter_OrgID');
```
### Inserting Reviews Details
```
INSERT INTO Reviews (Review_ID, Org_ID, Item_ID, Review) 
VALUES ('Enter_ReviewID', 'Enter_OrgID', 'Enter_ItemID', 'Enter_Review');
```
### Inserting Ratings Details
```
INSERT INTO Ratings (Rating_ID, Item_ID, Rating) 
VALUES ('Enter_RatingID', 'Enter_ItemID', 'Enter_Rating');
```
### Inserting Aggregate_Ratings Details
```
INSERT INTO Aggregate_Ratings (Item_ID, Rating) 
VALUES ('Enter_ItemID', 'Enter_Rating');
```
### Inserting Sentimental_Scores Details
```
INSERT INTO Sentimental_Scores (Review_ID, Sentimental_Score) 
VALUES ('Enter_ReviewID', 'Enter_SentimentalScore');
```
