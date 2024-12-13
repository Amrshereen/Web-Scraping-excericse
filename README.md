# Web-Scraping-excericse

This code performs web scraping on a webpage (https://www.baraasallout.com/test.html) using the BeautifulSoup library to extract various elements and save them into CSV and JSON files.

Key Sections:
  - HTTP Request
  - Data Extraction
  - Saving data to csv and json files 


## HTTP Request:

The script sends an HTTP request to the provided URL using the requests.get() method.
It checks if the request is successful (status_code == 200). If successful, it proceeds to scrape the page. If not, it prints an error message.
Parse HTML Content:

The HTML content of the page is parsed with BeautifulSoup using the html.parser.
It extracts multiple elements, including headings, paragraphs, list items, tables, forms, links, videos, and product information.


## Data Extraction:

Headings: Extracts the text of all heading tags and stores it in the headings list.
Paragraphs: Extracts text content from all <p> tags and stores it in the paragraphs list.
Lists : Extracts the content of all list items and stores it in the lists list.
Table: Extracts the table headers and row data (product name, price, stock status) and saves it in the table_data list. It writes this data to a CSV file (Extract_Text_Data.csv).
Book Cards: Extracts book titles, prices, stock availability, and button text from the book cards. It appends this data to the book_data list and saves it to a JSON file (Product_Information.json).
Form Input Fields: Extracts details about form input fields like name, type, and placeholder text and stores it in the input_feild_data list, saving it to a JSON file (Input_feild_data.json).
Links and Videos: Extracts hyperlinks (<a>) and video links (<iframe>) from the page and stores them in hyperlinks and video_links lists, respectively. This data is saved to a JSON file (Links.json).
Featured Products: Extracts data from the featured products section, including product ID, name, hidden price, and available colors, printing this data to the console.
Data Saving:

## Saving Data
The data extracted from the page is saved in various formats:
CSV: The headings, paragraphs, lists, and table data are written to Extract_Text_Data.csv.
JSON: The book data, form input fields, hyperlinks, video links, and featured products are saved as JSON files (Product_Information.json, Input_feild_data.json, Links.json, and featured_products.json).
Error Handling:

If the HTTP request fails (e.g., due to a network issue), it prints an error message indicating that the page could not be fetched.
Summary:
The script scrapes various elements from an HTML page, processes them, and saves the extracted data into structured CSV and JSON files for further use.
