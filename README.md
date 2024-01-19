# NoSQL Food Hygiene Analysis

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. I will use Mongo DB and Python in order evaluate some of the ratings data in order to help journalists and food critics alike decide where to focus future articles in regards to food safety.

![image](https://github.com/meehal0203/nosql-challenge/assets/146681542/6b5b9b59-f71d-4c27-be12-c87b394f4915)


This analysis will be broken into 3 parts: <br />
[Link to Parts 1&2](https://github.com/meehal0203/nosql-challenge/blob/main/Starter_Code%2012/NoSQL_analysis_starter.ipynb)
 will focus on  Database set-up and updating <br />
[Link to Part 3](NoSQL_analysis_starter_ipynb)
 will perform some exploratory analysis on the findings



## Part 1



Import the data provided in the establishments.json file from Terminal. Name the database uk_food and the collection establishments. Copy the text used to import your data from your Terminal to a markdown cell in notebook.

Within the notebook, import the libraries needed: PyMongo and Pretty Print (pprint).

Create an instance of the Mongo Client.

Confirm database creation 

* List the databases you have in MongoDB. Confirm that uk_food is listed.
* List the collection(s) in the database to ensure that establishments is there.
* Find and display one document in the establishments collection using find_one and display with pprint.
* Assign the establishments collection to a variable to prepare the collection for use.

## Part 2

The magazine editors have some requested modifications for the database before performing any queries or analysis for them. Make the following changes to the establishments collection:

An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked this to be included in your analysis. Add the following information to the database:

{
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
}

* Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

* Update the new restaurant with the BusinessTypeID you found.

* The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.

* Some of the number values are stored as strings, when they should be stored as numbers.

* Use update_many to convert latitude and longitude to decimal numbers.
* Use update_many to convert RatingValue to integer numbers.


## Part 3 - Analysis


Answer the following questions:
* Which establishments have a hygiene score equal to 20?

* Which establishments in London have a RatingValue greater than or equal to 4?

* What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

* How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.


While completing this assignment I used Ask BCS learning Assistant, tutoring sessions and Stack Overflow.
