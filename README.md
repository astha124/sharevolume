# SEC Company Shares Outstanding Data Viewer

This is a single-file responsive HTML application built with Tailwind CSS that displays the maximum and minimum number of common stock shares outstanding for a given company, based on data fetched from the SEC EDGAR API.

## Features

-   Displays the company name, maximum shares outstanding, and the fiscal year in which it occurred.
-   Displays the minimum shares outstanding and its corresponding fiscal year.
-   Data filtered for fiscal years greater than 2020.
-   Defaults to Automatic Data Processing (ADP) data (CIK: 0000008670).
-   Allows dynamic loading of data for any 10-digit CIK by appending a query parameter to the URL.

## How to Use

1.  **Open `index.html` in your browser.**
    By default, it will load data for Automatic Data Processing (ADP).

2.  **View data for a different company:**
    Append `?CIK=YOUR_CIK_NUMBER` to the URL.
    For example: `index.html?CIK=0001018724` (for Apple Inc.)

    **Note on Data Fetching:**
    The application uses a public proxy (`https://api.allorigins.win/`) to fetch data from the SEC EDGAR API (`https://data.sec.gov/`). This is necessary to bypass potential Cross-Origin Resource Sharing (CORS) restrictions when running the HTML file directly from your local filesystem (`file://` protocol) or some web servers. For production environments, it is recommended to implement your own secure backend proxy.

## Development

This application is built using:
-   HTML5
-   Tailwind CSS (via CDN)
-   Vanilla JavaScript

## Attachments

This project includes the `uid.txt` file, committed as-is, alongside the source code.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
