# Data Engineering Toolbox

A collection of lightweight browser-based tools for working with data, SQL, and developer workflows.

All tools are designed to be **simple, fast, and dependency-free** — single HTML files that run entirely in your browser with no installs, no build steps, and no data leaving your machine.

## 🔧 Tools

### SchemaViz
Visualize SQL schemas from `CREATE TABLE` statements as interactive ER diagrams.

**Features:**
- Supports PostgreSQL, MySQL, SQLite, and T-SQL
- Auto-detects primary keys and foreign key relationships

**Location:** `/schema-viz/index.html`

---

### BatchFlow
Define field mapping rules once and run them against any batch of local files. A lightweight local pipeline runner — no cloud, no API costs, no data uploaded anywhere.

**Features:**
- Supports XML, JSON, CSV, and plain text input
- Auto-detects file format and surfaces available fields
- Field aliases — define fallback paths for inconsistent schemas (e.g. `DecisionDate`, `decision_date`, `date_decided` all mapping to one output column)
- Transforms: date normalisation (any format → ISO 8601), trim, upper/lower, number parsing, boolean normalisation, regex extract
- Save and reload named jobs via browser localStorage
- Export results to CSV or JSON

**Location:** `/batch-flow/index.html`

---

## Philosophy

These tools are designed to be:

- **Lightweight** — single HTML files, no frameworks or build systems
- **Private** — everything runs client-side, no data is uploaded or stored externally
- **Repeatable** — jobs and configurations can be saved and re-run
- **Portable** — open directly in any browser, share as a file, or host on GitHub Pages

Perfect for quick data engineering tasks.

## Access

**Live site:** https://lewydavy.github.io/data-toolbox/

## Running Locally

No server required. Clone the repo and open any tool directly:

```bash
git clone https://github.com/lewydavy/data-toolbox.git
cd data-toolbox
open index.html              # homepage
open schema-viz/index.html   # SchemaViz
open batch-flow/index.html   # BatchFlow
```