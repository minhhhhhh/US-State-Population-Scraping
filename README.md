# Project 4: US States and Population Data Scraper

## Author
**Minh Nguyen**  


## Overview
This project demonstrates web scraping using Python to extract information about the states and territories of the United States, including their populations, from a Wikipedia page. The data is processed and saved into a CSV file for further analysis.

## Features
- **Web Scraping**: Uses `BeautifulSoup` to parse HTML content from a Wikipedia page.
- **Data Extraction**: Extracts state names and population figures from the web page.
- **Data Cleaning**: Filters and formats the extracted data into a clean, structured format.
- **Data Export**: Saves the cleaned data into a CSV file (`us_info.csv`).

## Tools and Libraries
The project uses the following Python libraries:
- **BeautifulSoup**: For HTML parsing and web scraping.
- **Requests**: To fetch HTML content from the webpage.
- **Pandas**: For data manipulation and exporting to CSV.

## Workflow
1. **Fetching Webpage Content**:  
   The code fetches HTML content from the Wikipedia page [List of states and territories of the United States](https://en.wikipedia.org/wiki/List_of_states_and_territories_of_the_United_States) using the `requests` library.

2. **Parsing HTML**:  
   The content is parsed using `BeautifulSoup` to locate the table containing the states and territories' information.

3. **Extracting Data**:  
   - **State Names**: Scraped from the `<th>` tags within the table.
   - **Population Figures**: Extracted from `<div>` tags within the table.

4. **Data Cleaning**:  
   - Filters out unnecessary strings from the scraped data.
   - Matches each state with its corresponding population.

5. **Exporting Data**:  
   The final data is saved as a CSV file named `us_info.csv`, with columns:
   - `state`: The name of each U.S. state or territory.
   - `population`: The population of each state or territory.

## Usage
1. Install the required libraries:
   ```bash
   pip install requests beautifulsoup4 pandas
   ```

2. Run the script:
   ```bash
   python project4.py
   ```

3. The script will output:
   - A printed list of state names.
   - A printed list of populations.
   - A CSV file `us_info.csv` in the current working directory.

## File Structure
- `project4.ipynb`: The main notebook file containing the code.
- `us_info.csv`: The output file containing state and population data (generated after running the script).

## Example Output
Sample data saved in `us_info.csv`:
| State       | Population    |
|-------------|---------------|
| California  | 39,512,223    |
| Texas       | 28,995,881    |
| Florida     | 21,477,737    |

