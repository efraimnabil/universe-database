# Universe Database

Welcome to the **Universe Database** repository! This project is designed to explore the structure and relationships of various astronomical entities including galaxies, stars, planets, and moons. It serves as a fun and educational project for managing celestial bodies using PostgreSQL.

## Table of Contents

- [Features](#features)
- [Database Schema](#database-schema)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)

## Features

- Create and manage a database for storing information about:
  - Galaxies
  - Stars
  - Planets
  - Moons
  - Various types of galaxies and celestial bodies
- Support for relationships between entities through foreign keys.
- Example data provided for testing and exploration.

## Database Schema

The database consists of the following tables:

1. **galaxy**
   - `galaxy_id`: Primary key (auto-incrementing)
   - `name`: Unique name of the galaxy
   - `type`: Type of the galaxy (e.g., spiral, elliptical)
   - `description`: A brief description of the galaxy

2. **star**
   - `star_id`: Primary key (auto-incrementing)
   - `name`: Unique name of the star
   - `star_type`: Type of the star (e.g., red dwarf, giant)
   - `age_in_millions_of_years`: Age of the star in millions of years
   - `is_spherical`: Boolean indicating if the star is spherical
   - `galaxy_id`: Foreign key referencing `galaxy`

3. **planet**
   - `planet_id`: Primary key (auto-incrementing)
   - `name`: Unique name of the planet
   - `diameter`: Diameter of the planet in kilometers
   - `has_life`: Boolean indicating if the planet has life
   - `star_id`: Foreign key referencing `star`

4. **moon**
   - `moon_id`: Primary key (auto-incrementing)
   - `name`: Unique name of the moon
   - `diameter`: Diameter of the moon in kilometers
   - `planet_id`: Foreign key referencing `planet`

5. **galaxy_types**
   - `galaxy_types_id`: Primary key (auto-incrementing)
   - `name`: Unique name of the galaxy type
   - `description`: A brief description of the galaxy type

## Getting Started

To get started with this project, follow the steps below:

### Installation

1. Clone the repository:
```bash
git clone https://github.com/efraimnabil/universe-database.git
```

2. Navigate to the project directory:
```bash
cd universe-database
```

3. Log in to PostgreSQL: Open your terminal and log in to PostgreSQL:
```bash
psql --username=your_username --dbname=postgres
```

4. Create the Database and Tables: Execute the SQL commands in universe.sql to create the database schema:
```bash
\i universe.sql
```

## Usage
After setting up the database, you can perform SQL queries to explore the data, analyze celestial relationships, or integrate it into your applications.

## Acknowledgments
- Special thanks to **[freeCodeCamp](https://www.freecodecamp.org/)** for the inspiration and guidelines to create this project as part of the Relational Database courses.