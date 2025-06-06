# vikdatashift

**vikdatashift** is a Python package designed to facilitate data migration between CSV files and databases (Oracle and PostgreSQL), as well as between different database systems.

## Version 1.0 Features

- Import data from CSV files to Oracle or PostgreSQL databases.
- Export data from Oracle or PostgreSQL databases to CSV files.
- Transfer data between Oracle and PostgreSQL databases.
- Create tables in the target database based on source structure.
- Truncate existing tables before data insertion (optional).
- Efficient data loading using chunked processing.

## Installation

Install **vikdatashift** using pip:

```bash
pip install vikdatashift
```

## Usage

To use **vikdatashift** in your Python script:

```python
from vikdatashift import csv_to_db, db_to_csv, db_to_db

# Import CSV to Oracle or PostgreSQL
db_type = "oracle"  # or "postgres"
csv_to_db(db_type)

# Export from Oracle or PostgreSQL to CSV
db_to_csv(db_type)

# Transfer data between Oracle and PostgreSQL
db_to_db("oracle", "postgres")  # or db_to_db("postgres", "oracle")
```

### Inputs Required:
When you run these functions, you'll be prompted to enter:
1. Database connection details (if not already saved).
2. Table names.
3. CSV file names (for CSV operations).
4. Actions to perform (e.g., truncate, create table).

## Requirements

- Python 3.6+
- `psycopg2`
- `cx_Oracle`

## Configuration

The package uses a `db_config.json` file to store database connection details. You'll be prompted to enter these details if they're not already saved.

## Features in Detail

### CSV to Database
- Import data from CSV files to Oracle or PostgreSQL.
- Create new tables based on CSV structure.
- Option to truncate existing tables before insertion.

### Database to CSV
- Export data from Oracle or PostgreSQL tables to CSV files.
- Handles large datasets efficiently.

### Database to Database
- Transfer data between Oracle and PostgreSQL databases.
- Option to create new tables in the target database.
- Option to truncate existing tables before transfer.
- Efficient data transfer using chunked processing.

## Contributing

Contributions to **vikdatashift** are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the **MIT License**.

## Author

**Satvik Jain**

## Support

If you encounter any problems or have any questions, please open an issue on the GitHub repository.

