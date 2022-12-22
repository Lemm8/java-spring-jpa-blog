# Add Jpa Data to an Existing Spring Boot Blog
***
## Table of Contents
1. Create the Post Entity and Repository
2. Create the Category Entity and Repository
3. Display All Categories and Individual Categories
***
### Create the Post Entity and Repository ( Luis Meza )
- Added the `@Entity` annotation to the Post class
- Added `@Id` and `@GeneratedValue(strategy = GenerationType.IDENTITY)` annotations to the id field
- Updated the column length in the body field and specified the "Temporal" type to the data field
- Turned PostRepository.java into an interface that extends "JpaRepository".
- Moved the data.sql file to the main/resources directory
***
### Create the Category Entity and Repository ( Luis Meza )
- Added the `@Entity` annotation to the Category class
- Added `@Id` and `@GeneratedValue(strategy = GenerationType.IDENTITY)` annotations to the id field
- Added the category field to the Post class and added the `@ManyToOne` relationship
- Added the posts field to the Category class with the `@OneToMany` relationship, modified the getter to return the list of posts and modified the addPost method to add a post to the posts list.
- Turned the CategoryRepository to an interface that extends from "JpaRepository"
- Added the "findByCategory" method to the CategoryRepository, that takes a category as an argument and returns a list of posts
- Copied the content of file "data-categories" and replace the "data.sql" content file with the recent copied content
- Displayed the category name on the <h3> element in the "post-details.html" template file. 