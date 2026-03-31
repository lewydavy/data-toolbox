# SchemaViz

Lightweight SQL schema visualizer that converts `CREATE TABLE` statements
into interactive ER diagrams.

- Parses PostgreSQL / MySQL / SQLite / T-SQL
- single HTML file

## Usage

1. Open `index.html`
2. Paste your `CREATE TABLE` SQL
3. Click **Visualize**

## Example

```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT
);

CREATE TABLE orders (
  id SERIAL PRIMARY KEY,
  user_id INT REFERENCES users(id)
);