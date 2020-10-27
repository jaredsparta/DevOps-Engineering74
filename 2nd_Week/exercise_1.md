# SQL Exercise

![](images/ex_erd.png)

**Explaining cardinalities**
- EBOOKS <-> USERS
    - An ebook must have one or more user author (1:N)
    - A user can have 0 or more ebooks that they have created (0:N)

- USERS <-> BOOKINGS
    - A user can have 0 or more bookings (0:N)
    - A booking can only have one user associated with it (1:1)



**Questions**
1. Shown in picture.
2. Shown in picture.
3. Users can rent out books.
4. There are three 1:N relationships shown.
5. We have one N:N relationship.

---
**SQL Querying**
- ```sql
    CREATE DATABASE bookstore;
    ---creates the database on the server

    USE bookstore;
    --ensure we are using the correct database when querying etc.

    CREATE TABLE users(
        user_id INT NOT NULL IDENTITY(1,1) PRIMARY KEY,
        first_name VARCHAR(20),
        last_name VARCHAR(50),
        email VARCHAR(50),
        phone_number VARCHAR(15)
    );
    -- IDENTITY(1,1) allows one to not specify user_id when inserting values as it will start counting from 1 incrementing by 1 each time

    CREATE TABLE bookings(
        booking_id INT NOT NULL IDENTITY(1,1) PRIMARY KEY,
        user_id INT NOT NULL,
        ebook_title VARCHAR(100),
        date_rented DATETIME,
        price DECIMAL(5,2),
        CONSTRAINT fk_booking_user
            FOREIGN KEY (user_id)
            REFERENCES users(user_id)
    );

    CREATE TABLE ebooks(
        ebook_id INT NOT NULL IDENTITY(1,1) PRIMARY KEY,
        user_id INT NOT NULL,
        ebook_title VARCHAR(100),
        release_date DATE,
        CONSTRAINT fk_ebooks_user
            FOREIGN KEY (user_id)
            REFERENCES users(user_id)
    );
    ```

---
**Used:**
- [Questions](https://github.com/Filipe-p/sql/blob/master/README.md)
- [Used to create diagram](https://www.diagrameditor.com/)
- [Creating foreign keys](https://www.techonthenet.com/sql_server/foreign_keys/foreign_keys.php)