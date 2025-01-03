# Cafe RESTful API Development

A Flask-based RESTful API for managing a cafe database, built with SQLite and SQLAlchemy. This project provides endpoints to perform CRUD operations, including adding, retrieving, updating, and deleting cafes. It’s designed for easy interaction via Postman or similar tools.

---

## Features
- **Retrieve a Random Cafe**: Fetch a random cafe from the database.
- **Get All Cafes**: View a list of all cafes, ordered by name.
- **Search Cafes by Location**: Find cafes in a specific location.
- **Add a New Cafe**: Add a new cafe to the database with details like name, location, amenities, and coffee price.
- **Update Coffee Price**: Update the coffee price for a specific cafe.
- **Delete a Cafe**: Remove a cafe from the database using an API key for authentication.

---

## Technologies Used
- **Python**: Core programming language.
- **Flask**: Web framework for building the API.
- **SQLAlchemy**: ORM for database interactions.
- **SQLite**: Lightweight database for data storage.
- **Postman**: For testing API endpoints.

---

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cafe-restful-api.git
   cd cafe-restful-api
Install dependencies:

bash
Copy code
pip install flask flask_sqlalchemy
Run the application:

bash
Copy code
python app.py
Access the API at http://127.0.0.1:5000.

API Endpoints
1. Get a Random Cafe
URL: /random
Method: GET
Response: A random cafe's details in JSON format.
2. Get All Cafes
URL: /all
Method: GET
Response: A list of all cafes.
3. Search Cafe by Location
URL: /search
Method: GET
Query Parameter: loc (location name)
Response: Cafes matching the location or a 404 error.
4. Add a New Cafe
URL: /add
Method: POST
Body Parameters (x-www-form-urlencoded):
name, map_url, img_url, loc, sockets, toilet, wifi, calls, seats, coffee_price
Response: Success message in JSON format.
5. Update Coffee Price
URL: /update-price/<cafe_id>
Method: PATCH
Query Parameter: new_price (new coffee price)
Response: Success or error message.
6. Delete a Cafe
URL: /report-closed/<cafe_id>
Method: DELETE
Query Parameter: api-key (authentication key)
Response: Success or error message.
Database Schema
The database consists of a single table, Cafe, with the following fields:

id: Primary key (integer).
name: Name of the cafe (string).
map_url: Google Maps URL (string).
img_url: Image URL (string).
location: Location of the cafe (string).
seats: Seating capacity (string).
has_toilet: Whether the cafe has a toilet (boolean).
has_wifi: Whether the cafe has WiFi (boolean).
has_sockets: Whether the cafe has power sockets (boolean).
can_take_calls: Whether calls are allowed (boolean).
coffee_price: Price of coffee (string, optional)
