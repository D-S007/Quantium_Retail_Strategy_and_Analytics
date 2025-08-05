# Replication Instructions

This guide explains how to replicate the analysis in the "Quantium Retail Strategy and Analytics" project.

## Software Requirements

- **R**: Version 4.5.1 or later.
- **RStudio**: Latest version.
- **LaTeX**: TinyTeX or MikTex for PDF output.
- **R Packages**: `data.table`, `ggplot2`, `ggmosaic`, `readr`, `readxl`, `janitor`, `dplyr`, `lubridate`, `knitr`.

## Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Quantium_Retail_Strategy_and_Analytics.git
   cd Quantium_Retail_Strategy_and_Analytics
   ```

2. **Install R Packages**:
   ```R
   install.packages(c("data.table", "ggplot2", "ggmosaic", "readr", "readxl", "janitor", "dplyr", "lubridate", "knitr"))
   ```

3. **Install TinyTeX**:
   ```R
   install.packages("tinytex")
   tinytex::install_tinytex()
   ```

4. **Verify LaTeX**:
   ```R
   tinytex::is_tinytex_installed()  # Should return TRUE
   ```
   If `FALSE`, run `tinytex::reinstall_tinytex()`.

5. **Check Datasets**:
   Ensure `QVI_transaction_data.xlsx` and `QVI_purchase_behaviour.csv` are in the `data/` folder.

## Running the Analysis

1. **Open RStudio** and set the working directory to the repository root:
   ```R
   setwd("path/to/Quantium_Retail_Strategy_and_Analytics")
   ```

2. **Open the Rmd File**:
   Open `scripts/Quantium_Task1_Solution.Rmd` in RStudio.

3. **Update File Path**:
   Modify the `filePath` variable in the script to match your `data/` folder location, e.g.:
   ```R
   filePath <- "path/to/Quantium_Retail_Strategy_and_Analytics/data/"
   ```

4. **Knit the Rmd File**:
   Click **Knit** in RStudio (select "Knit to PDF"), or run:
   ```R
   rmarkdown::render("scripts/Quantium_Task1_Solution.Rmd", output_format = "pdf_document")
   ```

5. **Check Outputs**:
   - PDF report: `reports/FinalReport.pdf`.
   - Visualizations: PNG files in `visualizations/`.

## Troubleshooting

- **LaTeX Errors**: Reinstall TinyTeX or install missing packages with `tinytex::tlmgr_install("package_name")`.
- **Package Issues**: Ensure all R packages are installed and loaded.
- **Path Errors**: Double-check the `filePath` variable matches your system.

For more details, see [README.md](README.md) or contact me via GitHub.