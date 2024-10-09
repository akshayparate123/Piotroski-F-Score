# Piotroski-F-Score
Piotroski F-Score Strategy

This project automates the calculation of the Piotroski F-Score, a financial analysis tool that helps assess a company's financial strength based on its profitability, liquidity, and operating efficiency. The project involves data mining, cleaning, score calculation, and dashboard generation using various tools and data sources.

## Features
1. **Data Mining from Livemint**: 
   - Scrapes financial data like cash flow statements, balance sheets, and income sheets from [Livemint.com](https://www.livemint.com).
   
2. **Data Cleaning and Storing**: 
   - Cleans the mined data to ensure consistency and accuracy before storing it in a MySQL database.

3. **Data Mining from NSE Website**: 
   - Scrapes board meeting dates and other relevant event information from the [NSE website](https://www.nseindia.com).

4. **Data Cleaning and Storing**: 
   - Similar to financial data, the board meeting data is cleaned and stored in the same MySQL database.

5. **Score Calculation**: 
   - Fetches data from the database and calculates the Piotroski F-Score, which consists of nine signals:
     1. **Profitability Signals**:
        - **ROA (Return on Assets)**: \( \text{Net Income} / \text{Total Assets} \)
        - **Operating Cash Flow**: Checks if operating cash flow is positive.
        - **Change in ROA**: Compares ROA of the current year with the previous year.
     2. **Leverage, Liquidity, and Source of Funds**:
        - **Change in Leverage**: \( \text{Long-term Debt} / \text{Total Assets} \), compares the current year to the previous year.
        - **Change in Current Ratio**: \( \text{Current Assets} / \text{Current Liabilities} \), compares the current year to the previous year.
        - **No New Shares Issued**: Checks if no new shares were issued.
     3. **Operating Efficiency**:
        - **Change in Gross Margin**: \( \text{Gross Profit} / \text{Total Revenue} \), compares the current year to the previous year.
        - **Change in Asset Turnover**: \( \text{Revenue} / \text{Total Assets} \), compares the current year to the previous year.
        - **Accruals**: Compares Net Income with Operating Cash Flow.

6. **Storing Results**: 
   - Stores the Piotroski F-Score results in the database for future analysis.

7. **Dashboard Generation Using Power BI**:
   - Integrates Power BI with the MySQL database to create interactive dashboards for visualizing the Piotroski scores and other financial metrics.

## How to Run the Project
1. Clone the repository.
2. Set up a MySQL database and ensure the scraping tools have access to the websites.
3. Run the data mining and cleaning scripts.
4. Use Power BI to create the dashboard by connecting it to the MySQL database.

## Tech Stack
- **Web Scraping**: Python (BeautifulSoup, Requests)
- **Database**: MySQL
- **Data Cleaning**: Pandas
- **Data Visualization**: Power BI

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
