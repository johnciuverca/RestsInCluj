

# RestsInCluj  

This Web App moves towards connecting people's points of view and thoughts on good food and having a hoot and a half of an experience in their own city. Finding a nice place to enjoy the company of your friends is always something that should not be taken for granted.
                                    This is where our App comes in handy. Bon Appetit!
                                    
This application stared as a final project for the Java Development course of The Informal School of it and up to a presentation it was developed by 3 students and now I'm working alone on it.

We used:
1. Spring Boot
2. PostgresSQL
3. JDBC
4. RestAPI
5. Thymeleaf
6. JUnit
7. Mockito

# Local setup

## Requirements

- Java 8
- PostgreSQL
- Maven Wrapper

## Configure PostgreSQL

Create a database named `restsInCluj`.

The local configuration expects:

- Host: `localhost`
- Port: `5433`
- User: `ciuverca`
- Password: blank
- Database: `restsInCluj`

Create the local files directory:

```bash
mkdir -p "$HOME/RestsInCluj-files"
```

## Import the database schema

From the project root, run:

```bash
psql -h localhost -p 5433 -U ciuverca -d restsInCluj -f src/main/resources/db_querys.sql
```

Warning: the schema script drops and recreates local tables. Rerunning it deletes local restaurants, reviews, users, and roles.

## Start the application

```bash
JAVA_HOME=$(/usr/libexec/java_home -v 1.8) bash mvnw spring-boot:run
```

Open:

```text
http://localhost:8090
```

# Images

  --- Home Page ---       
<img src="Images/HomePage.PNG" width="300">


 --- Register form ---    
<img src="Images/RegisterForm.PNG" width="200">
  
     
 --- Login form ---    
<img src="Images/SignInForm.PNG" width="250">
  
  
  --- Places to eat ---     
<img src="Images/PlacesToEat.PNG" width="250">


  --- Add/Edit Restaurant Form ---    
<img src="Images/Add,EditRestaurantForm.PNG" width="250">


  --- Reviews ---     
<img src="Images/ReviewsPage.PNG" width="250">


  --- Add review form ---    
<img src="Images/AddReviewForm.PNG" width="250">


  --- About Us ---    
<img src="Images/AboutUsPage.PNG" width="250">
