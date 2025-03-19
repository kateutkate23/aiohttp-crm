# CRM backend with aiohttp

This is a simple educational backend project built with `aiohttp`, implementing a basic CRM system. It provides three CRUD endpoints to manage users without a database, storing data in memory. The project includes API documentation via Swagger and basic authentication for secure access.

## Features

- **List Users (GET /api/users)**: Retrieve a list of all users.
- **Get User (GET /api/user?id={user_id})**: Fetch a specific user by their ID.
- **Add User (POST /api/users)**: Add a new user with an email address.
- In-memory storage (no database).
- Basic authentication for GET requests.
- API documentation with Swagger (available at `/docs`).

## Prerequisites

- Python 3.10
- Virtualenv (optional but recommended)

## Setup and Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/kateutkate23/aiohttp_crm.git
   cd aiohttp_crm
   ```

2. **Create and activate a virtual environment**:
   ```bash
   python3.10 -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**:
   ```bash
   python main.py
   ```

5. **Access the API**:
   - The server will run on `http://127.0.0.1:8080`.
   - Swagger documentation is available at `http://127.0.0.1:8080/docs`.

## API Endpoints

| Method | Endpoint            | Description         | Authentication Required |
|--------|---------------------|---------------------|-------------------------|
| GET    | `/api/users`        | List all users      | Yes                     |
| GET    | `/api/user?id={id}` | Get user by ID      | Yes                     |
| POST   | `/api/users`        | Add a new user      | No                      |
### Authentication

- GET endpoints require basic authentication.
- Default credentials (defined in `config.yaml`):
  - Username: `kate`
  - Password: `pass123`
- Use the format: `Authorization: Basic <base64-encoded-username:password>`.

## Notes

- This project uses in-memory storage, so data will be lost on server restart.
- The project is intended for educational purposes.

## License

This project is for educational purposes and does not include a specific license.
