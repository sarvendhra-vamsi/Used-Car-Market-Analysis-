# Used Car Market Analysis

An exploratory data analysis project that collects used-car listing information from Cars24 and compares listing prices across selected brands and cities.

**Project type:** Exploratory Data Analysis · Web Scraping  
**Language:** Python  
**Notebook:** [Finalized_UsedCar_project.ipynb](./Finalized_UsedCar_project.ipynb)  
**Website studied:** [Cars24](https://www.cars24.com/)

## Project objective

Used-car listings can vary by vehicle brand, model year, mileage, fuel type, transmission, and location. This project explores how listing data can be collected and analysed to help identify patterns in advertised prices.

The notebook builds URLs for selected brand and city combinations, extracts listing details, cleans selected fields, and explores the resulting data with Python visualisations.

**This is an exploratory snapshot of advertised listings—not a valuation model or a guarantee of the final selling price.**

## Scope

The notebook initially targets these brands:

- Toyota
- Hyundai
- Tata
- Honda

It explores city-level listing pages and uses the brand and city associated with each URL as part of the collected dataset. The website's available listings and page structure can change over time.

## Data collected

| Field | Description |
|---|---|
| Car name | Vehicle name displayed on the listing |
| Brand | Brand selected for the listing search |
| City | City associated with the listing search |
| Model year | Vehicle model year, where parsed |
| Kilometres driven | Displayed distance driven |
| Fuel type | Fuel type identified from the listing |
| Transmission | Manual or automatic, where identified |
| Listed price | Advertised price converted to a numeric value for analysis |

The notebook notes that owner type is not available on the listing card and is therefore not collected in the current workflow.

## Workflow

1. **Collect** — request listing pages using Python's requests library.
2. **Parse** — use Beautiful Soup to locate car cards and extract displayed fields.
3. **Clean** — use Pandas and regular expressions to convert text fields such as price and kilometres into analysis-ready values.
4. **Explore** — compare listing counts and price patterns across available categories.
5. **Visualise** — use Matplotlib and Seaborn to inspect distributions and compare average prices by brand and city.
6. **Interpret** — treat the charts as exploratory evidence and validate any business recommendation against the actual collected data.

## Tools and skills

- Python
- Requests and Beautiful Soup
- Pandas and NumPy
- Regular expressions for text cleaning
- Matplotlib and Seaborn
- Exploratory data analysis
- Data collection and feature preparation

## Run the notebook

### 1. Install dependencies

Use a Python environment with Jupyter Notebook or JupyterLab installed, then install:

    pip install requests beautifulsoup4 pandas numpy matplotlib seaborn jupyter

### 2. Open the notebook

Open **Finalized_UsedCar_project.ipynb** in Jupyter and run the cells in order.

### 3. Refresh the collection

The notebook requests live website pages when run. The returned listings, prices, and number of records can differ from the saved notebook outputs.

**Website structure warning:** The extraction logic relies on page elements and CSS classes that may change. If extraction returns empty or incomplete results, inspect the current page structure and update the selectors before interpreting the analysis.

## Findings: how to read the results

Use the notebook's charts to examine questions such as:

- How does the number of observed listings vary by brand and city?
- How do advertised prices differ across the collected categories?
- How are price and kilometres driven distributed?
- Do model year, fuel type, or transmission appear associated with price in this sample?

Report findings with the actual sample size, collection date, and relevant chart or summary statistic. Because listings can change and only a limited set of listing pages is collected, the analysis should not be generalised to the entire used-car market without additional data.

## Limitations

- The notebook collects a limited set of listing pages and does not currently implement full pagination.
- The website may change its HTML structure, causing selectors to stop working.
- Some fields may be missing or inconsistently formatted.
- The data reflects advertised listings at collection time, not completed sales.
- The current repository does not include a separately exported, cleaned dataset.

## Responsible data collection

Before collecting data, review the website's current terms and applicable access rules. Keep requests modest, do not bypass access controls, and stop if the site disallows automated access. This notebook is intended for learning and exploratory analysis.

## Suggested next improvements

- Export a documented, reproducible cleaned dataset when permitted.
- Record the collection date and number of valid listings.
- Add automated checks for missing values, duplicate listings, and failed extraction.
- Replace unverified general statements with quantified findings from the current dataset.
- Add chart screenshots and a short executive summary based on validated results.

## Author

**Vamsi** — BCA graduate building practical skills in Python, web scraping, and data analytics.

[View my GitHub profile](https://github.com/u200cbvt)
