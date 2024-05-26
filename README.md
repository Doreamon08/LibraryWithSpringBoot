## Project Description

This is a Java project that implements the basic functionality of an electronic library.

### Stack of Technologies Used
1. **Java 17**
2. **Spring Boot 3.1.2**
   - Spring Boot Starter Data JPA
   - Spring Boot Starter Thymeleaf
   - Spring Boot Starter Validation
   - Spring Boot Starter Web
   - Spring Boot Starter Test
3. **PostgreSQL**
4. **Thymeleaf**
5. **Maven**

### Implemented Features

#### BookController:
1. **View all books**:
   - Route: `GET /books`
   - Description: Displays a list of all books with optional pagination and sorting by year.

2. **View a specific book**:
   - Route: `GET /books/{book_id}`
   - Description: Displays information about a specific book, its owner, and all users.

3. **Add a new book**:
   - Route: `GET /books/new`
   - Description: Displays a form for adding a new book.
   - Route: `POST /books`
   - Description: Processes the form submission and saves the new book.

4. **Edit a book**:
   - Route: `GET /books/{book_id}/edit`
   - Description: Displays a form for editing book information.
   - Route: `PATCH /books/{book_id}`
   - Description: Processes the form submission and updates the book information.

5. **Delete a book**:
   - Route: `DELETE /books/{id}`
   - Description: Deletes a book.

6. **Release a book (remove owner)**:
   - Route: `PATCH /books/{book_id}/free`
   - Description: Removes the owner of the book.

7. **Assign an owner to a book**:
   - Route: `PATCH /books/{book_id}/assign`
   - Description: Assigns an owner to the book.

8. **Search for books**:
   - Route: `GET /books/search`
   - Description: Displays the book search page.
   - Route: `POST /books/search`
   - Description: Performs a search for books by name and displays the results.

9. **Create test data**:
   - Route: `POST /books/createTests`
   - Description: Creates test data for books.

#### PeopleController:
1. **View all users**:
   - Route: `GET /people`
   - Description: Displays a list of all users.

2. **View a specific user**:
   - Route: `GET /people/{person_id}`
   - Description: Displays information about a specific user and all books owned by them.

3. **Add a new user**:
   - Route: `GET /people/new`
   - Description: Displays a form for adding a new user.
   - Route: `POST /people`
   - Description: Processes the form submission and saves the new user.

4. **Edit a user**:
   - Route: `GET /people/{id}/edit`
   - Description: Displays a form for editing user information.
   - Route: `PATCH /people/{id}`
   - Description: Processes the form submission and updates the user information.

5. **Delete a user**:
   - Route: `DELETE /people/{id}`
   - Description: Deletes a user.

### Installation Instructions

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/yourrepository.git
   cd yourrepository
   ```

2. **Configure the database**:
   - Ensure PostgreSQL is installed and running.
   - Create a database for the project.
   - Update the database configuration in `application.properties`.

3. **Build the project**:
   ```bash
   mvn clean install
   ```

4. **Run the project**:
   ```bash
   mvn spring-boot:run
   ```

### Usage

- Access the application in your browser at `http://localhost:8080`.
- Use the provided routes to manage books and users.

