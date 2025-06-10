# ETL_Extract_-Mohamed-Mohamed-
# ETL Extract Lab

**Name:** [Mohamed Mohamed]

## Description

This project demonstrates a basic Extract, Transform, Load (ETL) process using Python and Pandas. The notebook simulates extracting event data from a CSV file, filtering for new records based on a timestamp, and updating a timestamp file to track the last extraction. This allows for incremental data loading, processing only the data that has changed since the last run.

The notebook performs the following steps:

1.  **Data Generation:** Creates a synthetic dataset of user events (login, purchase, logout) and saves it to a CSV file (`custom_data.csv`).
2.  **Full Extraction:** Reads the entire CSV file into a Pandas DataFrame and displays the first few rows.
3.  **Incremental Extraction:** Reads the CSV file, filters for records newer than the timestamp stored in `last_extraction.txt`, and displays the new data. If `last_extraction.txt` doesn't exist, it extracts all records.
4.  **Timestamp Update:** Updates the `last_extraction.txt` file with the latest timestamp from the newly extracted data.

## Tools Used

*   **Python:** The primary programming language.
*   **pandas:** Used for data manipulation and analysis, particularly for working with DataFrames.
*   **faker:** Used for generating synthetic data.
*   **datetime:** Used for handling timestamps.
*   **Jupyter Notebook:** The interactive environment for running the code.

## How to Reproduce

### Running the Notebook

1.  **Clone the repository:**

    ```bash
    git clone [repository URL]
    cd [repository directory]
    ```

2.  **Install the required libraries:**

    ```bash
    pip install pandas faker
    ```

3.  **Run the Jupyter Notebook:**

    ```bash
    jupyter notebook etl_extract.ipynb  
    ```

    This will open the notebook in your web browser. You can then execute each cell sequentially to run the ETL process.

### Data Source

The data is synthetically generated within the notebook itself using the `faker` library. The generated data is saved to a CSV file named `custom_data.csv`. The `last_extraction.txt` file is created and updated by the notebook to track the last extraction timestamp.  If you delete `custom_data.csv` or `last_extraction.txt`, the notebook will regenerate the data or perform a full extraction, respectively.