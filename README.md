# Alpha Photo Share

## desctiption

**Alpha Photo Share** is a web application for sharing photos that allows users to upload, edit, rate, and comment on photos. It provides authentication for users with different roles and supports search, filtering, and image transformation functionality, as well as the ability to work with QR codes and photo ratings.

## Requirements

- Python 3.12+
- `.env` file with the necessary environment variables

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-org/alpha-photo-share.git
cd alpha-photo-share
```

2. Install dependencies via Poetry:

```bash
poetry install
```

3. Create a `.env` file in the root directory based on `.env.example`:

```bash
   cp .env.example .env
   ```

4. Activate the environment:

```bash
   poetry shell
   ```

## Launch the application

```bash
uvicorn main:app --reload
```
- `app.main` — path to the FastAPI application.
- `--reload` — automatic reload when the code changes.

    or

```bash
python -m main
```
- `main` — path to the main.py file.

## Project structure
```bash
.
├── src/
│   ├── db/                  # Connecting to databases, declarative_base
│   ├── api/                 # Routers
│   ├── models/              # ORM models
│   ├── schemas/             # Pydantic Schemes
│   ├── repository/          # Logic of access to the database
│   ├── services/            # Business logic
│   └── core/                # Configurations, logging
├── tests/                   # Unit tests
├── main.py                  # FastAPI entry point
├── .env                     # Configuration
├── .env.example             # Configuration template
├── pyproject.toml           # Poetry configuration
├── CONTRIBUTING.md          # Instructions for making changes to the project
└── README.md                # Main project documentation
```

## API Documentation

- Swagger UI: [http://localhost:8000/docs](http://localhost:8000/docs)
- ReDoc: [http://localhost:8000/redoc](http://localhost:8000/redoc)

## Testing

```bash
pytest
```

Or, if you are not in the `poetry shell`:

```bash
poetry run pytest
```
