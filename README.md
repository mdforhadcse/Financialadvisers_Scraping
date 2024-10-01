# Financialadvisers_Scraping
Data(Company Name and Website URL) Scraping from https://financialadvisers.co.uk/

## Overview
This project scrapes data (Company Name and Website URL) from `financialadvisers.co.uk`. The script reads input data from a CSV file, makes HTTP requests to the website, parses the HTML content, and extracts the required information. The results are saved into CSV files.

## Prerequisites
- Python 3.x
- Required Python packages:
  - `requests`
  - `beautifulsoup4`
  - `pandas`

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/Financialadvisers_Scraping.git
    cd Financialadvisers_Scraping
    ```

2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage
1. Prepare the input CSV file (`input.csv`) with the following columns:
    - `Sector`: The sector to search for.
    - `Town`: The town to search in.

2. Run the scraping script:
    ```sh
    python Scaping_IFA_list.py
    ```

3. The script will generate temporary CSV files for each page and a final CSV file for each sector and town combination.

## Output
- The final CSV files will be saved in the `data` directory with the format: `<sector>_<town>.csv`.
- Temporary CSV files will be created and deleted during the process.

## Notes
- The script uses a list of user-agent strings to avoid being blocked by the website.
- The script includes error handling for failed HTTP requests and missing HTML elements.

## Directory Structure
```
Financialadvisers_Scraping/
├── Scaping_IFA_list.py
├── input.csv
├── data/
│   └── (output CSV files)
├── requirements.txt
└── README.md
```

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.