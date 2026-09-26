# StockSense

StockSense is a lightweight Inventory Management System built in Python 
that digitizes stock tracking — replacing manual registers and Excel sheets.

## Features
- Sign up / Login
- Add products with SKU, category, location
- Receive Goods (stock increases automatically)
- Sell Goods (stock decreases automatically)
- Mark Damaged Goods
- Internal Transfer between warehouses/racks
- Full Movement History (audit trail)
- Item-wise Summary Report (Received vs Sold vs Damaged)


## Tech Stack
- Python
- SQLite (database)
- Matplotlib (charts)

## How to Run
```bash
pip install -r requirements.txt
python stocksense.py
```

## Database Design
- **users** — stores login credentials
- **products** — stores current stock, damaged count, location per item
- **movements** — full transaction ledger (every receipt, sale, transfer, adjustment)

Every transaction updates the live `products` table AND logs a permanent 
record in `movements`, so the dashboard is instant while the full history 
stays fully traceable.

## Future Scope
- Web-based interface (Flask)
- OAuth login (Google/Microsoft)
- Multi-language support (Hindi, Telugu)
- Low-stock reorder alerts
- Visual Pie Chart of stock overview

## Team
- Dominion X
