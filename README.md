# Restaurant Ratings System (MySQL)

This project implements the backend database for a Restaurant Ratings System. It was developed as part of a university course focused on relational databases and SQL. The system is designed to support the storage, retrieval, and management of restaurant reviews, user profiles, and restaurant metadata in a structured and normalized MySQL database.

## Features

- Stores information about:
  - Restaurants and their attributes (e.g. name, location, cuisine type)
  - Users and their profile details
  - User-submitted ratings and reviews
- Enforces referential integrity using **foreign key constraints**
- Supports complex SQL queries including:
  - **Aggregations** (e.g. average rating per restaurant)
  - **Joins** (e.g. users with their reviews)
  - **Subqueries** and **nested SELECT statements**
- Enables data manipulation with **INSERT**, **UPDATE**, and **DELETE** queries
- Demonstrates proper **normalization** to minimize redundancy

## Technologies Used

- **MySQL** for relational database design and querying
- **SQL DDL/DML** for schema creation and data interaction
- **MySQL Workbench** (optional) for visualization and query testing

## Schema Overview

The database consists of the following primary tables:

- `Restaurants`: Contains data on each restaurant (name, address, cuisine, etc.)
- `Users`: Stores user information (username, join date, etc.)
- `Ratings`: Associates a user with a restaurant and includes their numeric rating and written review
- `Categories`: Optional support for tagging restaurants with multiple cuisine categories

Each table includes primary keys and the `Ratings` table includes foreign keys to ensure valid user and restaurant references.

## Example Queries

- Get the average rating for each restaurant:
  ```sql
  SELECT restaurant_id, AVG(score) AS avg_rating
  FROM Ratings
  GROUP BY restaurant_id;
  
## Project Team

This project was developed collaboratively by a team of three as part of an **Agile software development process**. The team worked in **iterative two-week sprints**, incorporating regular **peer reviews** to ensure code quality and maintain consistent progress.

## Future Work

While the current version focuses on the database backend, potential future extensions include:

- A web front-end for users to browse restaurants and submit reviews  
- Data scraping scripts to populate the database with real-world data  
- Additional analytics for identifying restaurant trends and user behavior  

## License

This project was created for educational purposes only and is not intended for production use.
