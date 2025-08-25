This file contains the instructions to create a script of sqlite3 commands named sql/scripts/inventory.sql to manage an inventory system with suppliers, categories, and products. The script will include table creation, data population, a view for product listing, and triggers for referential integrity.

Requirements:
- Foreign key constraints are enabled (`PRAGMA foreign_keys = ON;`)
- Referential integrity is enforced
- All tables must have an 'id' column as the primary key (auto-incrementing)
- All tables must have a 'created_at' column to hold the timestamp of when the record was created
- All tables must have an 'updated_at' column to hold the timestamp of when the record was last updated

Steps:
1) Create a file named 'sql/scripts/inventory.sql' to contain the script, if one does not exist.
2) Set foreign key constraints on (`PRAGMA foreign_keys = ON;`).
3) Create a 'suppliers' table with the following columns:
   - id: integer, primary key, auto-increment
   - name: text, not null
   - address: text, nullable
   - city: text, not null
   - state: text, not null
   - zip: text, not null
   - created_at: datetime, default current timestamp
   - updated_at: datetime, default current timestamp
4) Create a 'categories' table with a one-to-many relation to 'suppliers':
   - id: integer, primary key, auto-increment
   - name: text, not null
   - description: text, nullable
   - supplier_id: integer, foreign key references suppliers(id)
   - created_at: datetime, default current timestamp
   - updated_at: datetime, default current timestamp
5) Create a 'products' table with a one-to-many relation to 'categories':
   - id: integer, primary key, auto-increment
   - name: text, not null
   - price: real, not null
   - category_id: integer, foreign key references categories(id)
   - created_at: datetime, default current timestamp
   - updated_at: datetime, default current timestamp
6) Populate the 'suppliers' table with sample data.
7) Populate the 'categories' table with sample data.
8) Populate the 'products' table with sample data.
9) Create a view named 'product_list' that displays:
   - product_id
   - product_name
   - category_name
   - supplier_name
10) Provide a SELECT statement to retrieve all records from the 'product_list' view.
11) Create a trigger that updates the 'products' table when a 'categories' record is deleted (e.g., set category_id to NULL or delete related products).

