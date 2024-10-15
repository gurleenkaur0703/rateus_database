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
