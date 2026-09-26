Merchants log receipts, deliveries, transfers, stock adjustments, and damaged goods; stock updates automatically with a full transaction ledger, dashboard KPIs, and item-wise reporting.

# StockSense

StockSense is a lightweight Inventory Management System built in Python that digitizes stock tracking — replacing manual registers and Excel sheets.

## Features

- Sign up / Login
- OTP-style password reset (code shown on screen for demo)
- Add products with SKU, category, unit of measure, reorder level, and location
- Search products by name, SKU, or category
- Receipts (stock increases automatically)
- Delivery Orders with pick/pack/validate steps (stock decreases automatically)
- Mark Damaged Goods
- Stock Adjustments (reconcile recorded stock vs physical count)
- Internal Transfer between warehouses/racks
- Full Movement History (filterable by type)
- Dashboard KPIs: total products, total stock, damaged goods, low stock items, out of stock items
- Item-wise Summary Report (Received vs Delivered vs Damaged)

## Tech Stack

- Python
- SQLite (database)

## How to Run
python3 stocksense.p


## Database Design

- **users** — stores login credentials (salted, hashed passwords)
- **products** — stores SKU, category, unit of measure, current stock, damaged count, reorder level, location per item
- **movements** — full transaction ledger (every receipt, delivery, transfer, adjustment, and damage record)

Every transaction updates the live `products` table AND logs a permanent record in `movements`, so the dashboard is instant while the full history stays fully traceable.

## Future Scope

- Document status workflow (Draft → Waiting → Ready → Done → Canceled)
- Role-based access (Inventory Manager vs Warehouse Staff)
- Structured warehouse entities (real Warehouse/Rack objects, true multi-warehouse support)
- Real OTP delivery via email/SMS
- Dynamic filters by warehouse, category, and document status
- Web-based interface (Flask)
- OAuth login (Google/Microsoft)
- Multi-language support (Hindi, Telugu)
- Low-stock reorder alerts (proactive notifications)
- Visual Pie Chart of stock overview

## Team

- Dominion X

