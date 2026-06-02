## Data Architecture & Dataset Description

The project utilizes data from a relational SQLite database (`db.sqlite3`) consisting of three core tables. Below is the detailed database schema and data dictionary.

### 1. Source Database Schema

#### 📊 Table: `restaurant_order`
Contains general information about each placed order.
| Column Name |  Description |
| :--- | :--- | 
| `id` |  Unique identifier for each order |
| `datetime` |  Timestamp when the order was placed |

#### 📊 Table: `restaurant_product`
A directory of all available menu items and their prices.
| Column Name | Data Type | Description |
| :--- | :--- |
| `id` |  Unique identifier for each product |
| `name` |  Name of the dish/product |
| `price` |  Base price of the product |

#### 📊 Table: `restaurant_orderitem`
A bridge table that connects orders with products, representing specific items within an order (Handles Many-to-Many relationship).
| Column Name | Description |
| :--- | :--- | 
| `id` |  Unique identifier for the order item line |
| `quantity` |  Number of units purchased |
| `order_id` |  References `restaurant_order(id)` |
| `product_id`|  References `restaurant_product(id)` |

---

### 🔑 Relational Connections (ERD Logic)
* `restaurant_orderitem.order_id` ➡️ `restaurant_order.id` 
* `restaurant_orderitem.product_id` ➡️ `restaurant_product.id` 

---

### 📁 Target Dataset: `combined_restaurant_data.csv`

After executing the ETL pipeline script and performing SQL `INNER JOIN` operations, the data was flattened into a single structured CSV file for analysis. It contains the following columns:

| Column Name | Source Table | Description |
| :--- | :--- | :--- |
| `quantity` | `restaurant_orderitem` | The number of items ordered |
| `name` | `restaurant_product` | Name of the specific dish |
| `price` | `restaurant_product` | Price per single unit |
| `datetime` | `restaurant_order` | Date and time of the order |
