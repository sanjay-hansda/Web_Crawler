# Web_Crawler

## Configuration

The script can be configured by modifying the following variables:

*   **`base_url`**: The base URL of the website to scrape.  Change this to target a different section or website. Example: `https://thebetterindia.com/topics/sustainability/page/`
*   **`total_pages`**: The number of pages to scrape. Adjust this value according to the website's pagination structure. Example: `45`
*   **`html_dir`**:  Directory to save the downloaded HTML pages.  The script creates this directory if it doesn't already exist. Example: `"html_files_1"`
*   **`proxies`**: A list of proxy servers. This script uses multiple proxies to overcome IP address blocking issues that may occur during web crawling.  **Important**: Replace the provided proxy list with your own working proxies.

## Usage

1.  **Install Libraries:** Run the pip install commands listed in the prerequisites section.

2.  **Configure Variables**: Adjust the `base_url`, `total_pages`, and `html_dir` variables as needed. Most importantly, **replace the placeholder proxy list** with a list of working proxies. If you don't have any working proxies, remove the proxy configuration from the `fetch_html` function and test your connection.

3.  **Run the script**. Execute the script.  It will download HTML content from each page, extract the desired data, and save the results in a file named "all\_articles.xlsx".

## Data Extraction

The script extracts the following data for each article:

*   **Title**: The article title.
*   **Link**: The article URL.
*   **Publish Date**: The article's publication date.

## Error Handling

The script attempts to handle common errors such as HTTP request failures and proxy connection issues.  When it encounters a problem with a particular proxy, it tries the next proxy in the list. If all proxies fail for a given page, it will print an error message but continue processing the next pages.


## Output

The script outputs an Excel file named "all\_articles.xlsx" containing the extracted data.  It also saves the raw HTML of each page in the directory specified by `html_dir`.


## Notes

*   The script includes random delays between requests to avoid overloading the server and to reduce the chance of getting your IP address blocked.

