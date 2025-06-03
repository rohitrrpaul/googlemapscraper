# Google Maps Business Scraper

A Python script that scrapes business details from Google Maps search results and saves them to both JSON and Excel files.

## Features

- Scrapes business details including:
  - Business Name
  - Rating
  - Reviews
  - Category
  - Website
  - Address
  - Phone Number
- Human-like behavior to avoid detection
- Saves data in both JSON and Excel formats
- Configurable scrape limit
- Sophisticated mouse movement patterns
- User agent rotation

## Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd <repository-directory>
```

2. Create and activate a virtual environment:

For Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

For macOS/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

3. Install the required packages:
```bash
pip install -r requirements.txt
```

## Usage

Run the script with a search query:
```bash
python google_maps_scraper.py "restaurants in pune" --limit 5
```

### Arguments

- `search_query`: The search query for Google Maps (required)
- `--limit`: Maximum number of businesses to scrape (optional)

### Output

The script generates two files:

1. JSON file: `business_details_<search_query>.json`
   - Contains raw data in JSON format
   - Useful for data processing or importing into other systems

2. Excel file: `business_details_<search_query>_<timestamp>.xlsx`
   - Formatted data in Excel format
   - Features:
     - Tahoma font, size 11
     - Row height: 21
     - Vertical alignment: Middle
     - Auto-sized columns
     - Headers in row 1
     - Timestamp in filename

## Anti-Detection Features

The script includes several features to avoid detection:

1. **User Agent Rotation**
   - Randomly selects from multiple modern user agents
   - Includes Chrome, Firefox, Safari, and Edge

2. **Human-like Behavior**
   - Sophisticated mouse movements using Bezier curves
   - Random delays between actions
   - Natural scrolling patterns
   - Variable timing for interactions

3. **Browser Fingerprinting Protection**
   - Uses undetected-chromedriver
   - Disables automation flags
   - Simulates real browser behavior

## Error Handling

The script includes comprehensive error handling for:
- Network issues
- Missing data
- Browser automation errors
- File I/O operations

## Requirements

- Python 3.7 or higher
- Chrome browser installed
- Internet connection
- Required Python packages (see requirements.txt)

## Notes

- The script includes random delays to avoid rate limiting
- Some data might be missing if not available on Google Maps
- Phone numbers are formatted according to specific rules
- Review counts are converted from K notation to numeric format

## Troubleshooting

If you encounter issues:

1. Make sure Chrome is installed and up to date
2. Check your internet connection
3. Verify all required packages are installed
4. Ensure you have write permissions in the directory

## License

This project is licensed under the MIT License - see the LICENSE file for details. 