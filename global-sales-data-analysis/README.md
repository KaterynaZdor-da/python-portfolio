# Global Sales Data Analysis

## Overview
This project focuses on a comprehensive analysis of international sales data for a company operating in both physical retail stores and online channels worldwide. The analysis aims to uncover buying patterns across different regions, evaluate sales channel performance, analyze shipping efficiency, and identify top-performing products to optimize global supply chain and marketing strategies.

## Data Architecture & Dataset Description

The project processes data distributed across three relational tables, combining product details, geographic insights, and transaction events.

### 1. Source Data Dictionary

#### 📊 Table: `Products`
Contains the directory of items available for sale.
| Column Name |  Description |
| :--- | :--- | 
| `id` | Unique identifier for each product |
| `item_type` |  Name or category of the product |

#### 📊 Table: `Countries`
Provides geographical mapping and regional hierarchies.
| Column Name |  Description |
| :--- | :--- |
| `name` | Full name of the country |
| `alpha-2` | Two-letter ISO country code |
| `alpha-3` |  Three-letter ISO country code |
| `region` |  Broad geographic region (e.g., Europe, Asia) |
| `sub-region`| Specific sub-region (e.g., Eastern Europe) |

#### 📊 Table: `Events`
The core transactional table containing all order history and metrics.
| Column Name |  Description |
| :--- | :--- | 
| `Order ID` |  Unique identifier for the order |
| `Order Date` |  The date when the order was placed |
| `Ship Date` | The date when the order was shipped |
| `Order Priority`|  Priority level of the order (e.g., Critical, High, Medium, Low) |
| `Country Code` |  Reference to the country (matches `Countries` codes) |
| `Product ID` |  Reference to the product (matches `Products(id)`) |
| `Sales Channel` | Channel of sale: `Online` or `Offline` |
| `Units Sold` | Quantity of items sold in the transaction |
| `Unit Price` | Selling price per single unit |
| `Unit Cost` | Production/acquisition cost per single unit |

---

## Analysis Objectives (Key Focus Areas)

1. **Geographic Performance**: Identify top-revenue regions, sub-regions, and specific countries.
2. **Sales Channel Efficiency**: Compare sales volume, revenue, and profit margins between Online and Offline channels.
3. **Product & Profitability Analysis**: Calculate total revenue, total cost, and net profit per product category (`Units Sold * Unit Price` vs `Units Sold * Unit Cost`).
4. **Shipping & Logistics Tracking**: Analyze the duration between `Order Date` and `Ship Date` to evaluate delivery efficiency across different priority levels.

## Technologies Used
* **`Python`**
* **`Pandas`** for data merging (joining `Events` with `Products` and `Countries`), cleaning, and feature engineering.
* **`Matplotlib & Seaborn`** for geospatial and analytical visualizations.
* **`Google Colab`**.
