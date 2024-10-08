
# Football Reservation System

## Overview
The Football Reservation System is a Spring Boot application designed to manage football match reservations. It provides RESTful APIs to create, retrieve, update, and delete match information. The project uses Maven for dependency management and is built with Java.

## Features
- **Create a Match**: Add a new football match to the system.
- **Retrieve All Matches**: Get a list of all football matches.
- **Retrieve Future Matches**: Get a list of all upcoming football matches.
- **Retrieve Matches by Team**: Get a list of matches for a specific team.
- **Retrieve Match by ID**: Get details of a specific match by its ID.
- **Delete a Match**: Remove a match from the system.

## Technologies Used
- Java
- Spring Boot
- Maven

## Getting Started

### Prerequisites
- Java 11 or higher
- Maven 3.6.0 or higher

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/AdhamEzz1/Football-Reservation-System.git
   cd Football-Reservation-System
   ```

2. Build the project using Maven:
   ```bash
   mvn clean install
   ```

3. Run the application:
   ```bash
   mvn spring-boot:run
   ```

## API Endpoints

### Create a Match
- **URL**: `/api/v1/matches`
- **Method**: `POST`
- **Request Body**: JSON representation of the `Match` object.
- **Response**: Created `Match` object.
- **Example**:
  ```bash
  curl -X POST http://localhost:8080/api/v1/matches -H "Content-Type: application/json" -d '{"homeTeam": "Team A", "awayTeam": "Team B", "matchDateTime": "2023-12-01T15:00:00", "venue": "Stadium", "totalCapacity": 50000}'
  ```

### Retrieve All Matches
- **URL**: `/api/v1/matches`
- **Method**: `GET`
- **Response**: List of all `Match` objects.
- **Example**:
  ```bash
  curl http://localhost:8080/api/v1/matches
  ```

### Retrieve Future Matches
- **URL**: `/api/v1/matches/future`
- **Method**: `GET`
- **Response**: List of future `Match` objects.
- **Example**:
  ```bash
  curl http://localhost:8080/api/v1/matches/future
  ```

### Retrieve Matches by Team
- **URL**: `/api/v1/matches/team/{teamName}`
- **Method**: `GET`
- **Response**: List of `Match` objects for the specified team.
- **Example**:
  ```bash
  curl http://localhost:8080/api/v1/matches/team/TeamA
  ```

### Retrieve Match by ID
- **URL**: `/api/v1/matches/{matchId}`
- **Method**: `GET`
- **Response**: `Match` object with the specified ID.
- **Example**:
  ```bash
  curl http://localhost:8080/api/v1/matches/1
  ```

### Delete a Match
- **URL**: `/api/v1/matches/{matchId}`
- **Method**: `DELETE`
- **Response**: HTTP status code indicating the result.
- **Example**:
  ```bash
  curl -X DELETE http://localhost:8080/api/v1/matches/1
  ```

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For any inquiries or issues, please contact [Adham Ezz](https://github.com/AdhamEzz1).