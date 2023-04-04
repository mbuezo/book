-- Create a database called 'bookstore'
CREATE DATABASE bookstore;

-- Switch to the 'bookstore' database
USE bookstore;

-- Create a table for books
CREATE TABLE books (
  id INT PRIMARY KEY,
  title VARCHAR(255),
  genre_id INT,
  drink_id INT
);

-- Create a table for genres
CREATE TABLE genres (
  id INT PRIMARY KEY,
  name VARCHAR(255)
);

-- Create a table for drinks
CREATE TABLE drinks (
  id INT PRIMARY KEY,
  name VARCHAR(255)
);

-- Insert data into the 'genres' table
INSERT INTO genres (id, name)
VALUES
  (1, 'Fiction'),
  (2, 'Non-fiction philosophy'),
  (3, 'Non-fiction philosophy'),
  (4, 'Non-fiction philosophy');

-- Insert data into the 'drinks' table
INSERT INTO drinks (id, name)
VALUES
  (1, 'Matcha'),
  (2, 'Matcha'),
  (3, 'Chai tea'),
  (4, 'Matcha');

-- Insert data into the 'books' table, linking each book to its genre and drink
INSERT INTO books (id, title, genre_id, drink_id)
VALUES
  (1, 'A Little Life', 1, 1),
  (2, 'On Being Someone Else', 2, 2),
  (3, 'Letters from a Stoic', 3, 3),
  (4, 'Meditations', 4, 1);
