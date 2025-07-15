# Telegram Data Pipeline

## Overview
This project builds An end-to-end data platform that extracts medical product insights from public Telegram channels using Telethon, YOLOv8, dbt, and FastAPI—fully orchestrated with Dagster. From raw messages and images to a clean analytical API, this pipeline delivers real-time health market intelligence at scale.

## Features
- Telegram channel scraping for medical business data
- Data cleaning and transformation using DBT (Data Build Tool)
- Object detection in images using YOLOv8
- Data warehouse implementation
- FastAPI interface for data access

## Technologies Used
- Python
- Telethon (for Telegram scraping)
- DBT (Data Build Tool)
- YOLOv8 (You Only Look Once) for object detection
- FastAPI
- SQLAlchemy
- PostgreSQL


## Setup and Installation
1. Clone the repository:
   ```
   git clone https://github.com/yourusername/eth-meddata-warehouse.git
   cd eth-meddata-warehouse
   ```

2. Set up a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   - Create a `.env` file in the root directory
   - Add necessary variables (e.g., database credentials, Telegram API keys)


## Usage
1. Run the Telegram scraper:
   ```
   python scripts/telegram_scraper.py
   ```

2. Execute DBT transformations:
   ```
   dbt run
   ```
3. dbt Testing and documentation
   ```
   dbt test
   dbt docs generate 
   dbt docs serve 
   ```
4. Run object detection on scraped images:
   ```
   python scripts/yolo_object_detection.py
   ```

5. Start the FastAPI server:
   ```
   cd FastAPI
   uvicorn main:app --reload
   ```

## Project Structure
```
eth-meddata-warehouse/
│
├── scripts/
│   ├── telegram_scraper.py
|   ├── data_cleaning_transformation.py
│   ├── yolo_object_detection.py
│   └── README.md
├── notebooks/
│   ├── scraped-data.ipynb
│   ├── yolo_object_detection.ipynb
│   └── README.md
├── eth_meddata_warehouse/    # directory for dbt models 
│   └── models/
|
├── FastAPI/     # directory for fastapi call 
│   ├── main.py
│   ├── models.py
│   └── schemas.py
│   └── database.py
│   └── crud.py
|
├── logs/   # log files 
├── tests/
├── requirements.txt    # all dependencies 
└── README.md
```

## Author
Waggari Misganu
## Meet me @
wagarimisganu12@gmail.com

