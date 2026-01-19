# **Data Scientist Screening Exercise -ICE Detention Facilities**

# Overview
This project analyzes and cleans a publicly released dataset of ICE detention facilities.
The objective is to:

        -  Clean a messy real-world dataset

        -  Standardize facility names and inspection dates

        -  Calculate total detained population by facility

        -  Identify the top 10 detention facilities by total population

        -  Visualize the results in a clear and publication ready chart

        -  The work is implemented in a Jupyter Notebook using Python.


# **Repository Contents**
```text
├── ice_data_cleaning.ipynb  # Main notebook (data cleaning, analysis, visualization)
├── data/
│   ├── messy_ice_detention.csv
│   ├── partially_cleaned_ice_detention.csv
│   ├── cleaned_ice_detention.csv
│   ├── top_10_detention_facilities.csv
│   └── top_10_detention_facilities.png
└── README.md
```

# **How to Run the Analysis Using the JupyterLab**

1. **Clone the repository:**
 ```bash
git clone https://github.com/subekshya-s/data-screening-exercise.git
   cd data-screening-exercise
```


2. **Install Required Dependencies**

    **Make sure Python 3 is installed, then install the required libraries:**
    
    `pip install pandas numpy matplotlib jupyterlab`
       
                
    **If using Anaconda:**

    `conda install pandas numpy matplotlib jupyterlab`

3. **Launch JupyterLab:**
            From the project root directory, run:
                                                    `jupyter lab`

            
     This will open JupyterLab in your default web browser.

4. **Open and Run the Notebook**

   In the JupyterLab file browser, open `ice_data_cleaning.ipynb`.

   - Click **Run → Run All Cells**
   - Or run cells individually using **Shift + Enter**

5. **Verify Outputs**

   After running the notebook, the following files will be generated in the `data/` folder:

   - `cleaned_ice_detention.csv`
   - `top_10_detention_facilities.csv`
   - `top_10_detention_facilities.png`

   To ensure reproducibility, restart the kernel and run all cells again:

   - **Kernel → Restart Kernel**
   - **Run → Run All Cells**


# **Methodology**

1. **Data Cleaning**

    - Removed non-data header and metadata rows

    - Reloaded the dataset with proper column headers

    - Standardized facility names by removing special characters and parenthetical text

    - Replaced empty and whitespace-only values with NaN

    - Converted mixed-format inspection dates (Excel serial numbers and string dates)

    - Ensured all dates were standardized to datetime64[ns]

2. **Data Analysis**
   

    - Created a Total Population column by summing:
        Level A
        Level B
        Level C
        Level D

    - Identified the top 10 detention facilities by total population

    - Exported the results as a CSV file


3. **Data Visualization**

    - Created a horizontal bar chart using matplotlib

    - Ordered facilities by descending total population

    - Added value labels, gridlines, and source annotations

    - Saved the visualization as a high-resolution PNG file


# **Manual Data Corrections**

The following values were manually corrected after verification using
official ICE detention facility records mentioned in the pdf:

-Missing city value for a facility located in Ohio
-Missing facility names for facilities located in Minnesota (MN) and New Hampshire (NH)
-All other cleaning steps were performed programmatically.

# **Data Source**

ICE Integrated Decision Support (IIDS), publicly released under the
DHS Appropriations Act, 2020 (H.R. 1158, Sec. 218).


# **Use of External Resources and AI Tools**

- This project was completed using a combination of personal understanding and external resources.

- ChatGPT was used to clarify pandas and matplotlib syntax and assist with data-cleaning strategies.
        Prompt used - (https://chatgpt.com/c/696cb2d9-9bcc-8322-86b6-417043f9131f)

- YouTube tutorials were consulted for general data cleaning workflows and visualization techniques.

- Google search was used to reference documentation and verify facility information where required.

- All external guidance was reviewed, adapted, and implemented with my own understanding.

- All analysis and final decisions reflect my independent work.