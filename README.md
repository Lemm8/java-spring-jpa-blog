# Add Jpa Data to an Existing Spring Boot Blog
***
## Table of Contents
1. Create the Post Entity and Repository
2. Create the Category Entity and Repository
3. Display All Categories and Individual Categories
***
### Create the Post Entity and Repository ( Luis Meza )
- Added the `@Entity` annotation to the Post class
- Added `@Id` and `@GeneratedValue(GenerationType.IDENTITY)` annotations to the id field
- Updated the column length in the body field and specified the "Temporal" type to the data field
- Turned PostRepository.java into an interface that extends "JpaRepository".
- Moved the data.sql file to the main/resources directory
***
### Create the Post Entity and Repository ( Luis Meza )
