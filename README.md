   **SharkTank_India-DataAnalysis**

   
The dataset titled Shark Tank India.csv contains detailed information about the pitches presented in the Indian version of the television show "Shark Tank." The dataset captures various attributes related to each pitch, including financial metrics, presenter demographics, industry type, and the outcomes of the pitches. This README document outlines the steps taken to analyze the data, including data cleaning, exploratory data analysis (EDA), and visualizations. Additionally, it provides suggestions for further analysis to extract more insights from the data.

**1. Data Loading and Initial Exploration**

Data Summary:

Command: shark_tank.info()
Purpose: Provides an overview of the dataset, showing the number of entries, columns, data types, and non-null values. This helps in understanding the structure of the dataset and identifying potential data quality issues.

Descriptive Statistics:
Command: shark_tank.describe().T.round(2).style.background_gradient(cmap='Oranges')
Purpose: Generates summary statistics (mean, standard deviation, min, max, etc.) for each numeric feature. The use of a gradient background makes it easier to visually identify patterns or outliers in the data.

Missing Values Check:
Command: shark_tank.isnull().sum()
Purpose: Identifies missing values in the dataset, allowing for informed decisions on data cleaning and imputation strategies.

Unique Values Count:
Command: shark_tank.nunique()
Purpose: Provides the count of unique values in each column, which helps in understanding the variability and potential redundancy in the data.

 **2. Data Cleaning and Transformation**
      
Data Type Conversion: Several columns were converted to appropriate data types using pd.Int32Dtype() and str for better consistency and to avoid potential errors during analysis:

Columns: 'Season Number', 'Episode Number', 'Pitch Number', 'Number of Presenters', 'Male Presenters', 'Female Presenters', 'Transgender Presenters', 'Couple Presenters', 'Startup Name', 'Industry', 'Business Description', 'Gross Margin', 'Net Margin', 'Started in', 'Yearly Revenue', 'Received Offer', 'Accepted Offer'.

 **3. Season-Wise Analysis**
      
Season-Wise Number of Episodes: A bar plot visualizing the number of episodes per season.

Visualization: Bar plot.
Insights: The number of episodes varied across seasons.
Season-Wise Pitches: Detailed summary of the number of episodes, real pitches, and unseen pitches for each season.

  **4. Financial Analysis**
      
Average Financial Metrics Across Seasons: Comparison of average financial metrics like 'Original Ask Amount', 'Total Deal Amount', 'Valuation Requested', 'Deal Valuation', 'Original Offered Equity', and 'Total Deal Equity' across different seasons.
Visualization: Pivot table and bar plot.
Insights: Differences in financial metrics across seasons, including the gap between requested valuations and deal valuations.
Demographic Analysis
Presenter Gender Distribution: Analysis of gender distribution among the presenters.

Visualization: Pie chart.
Insights: Percentage breakdown of male, female, and transgender presenters.
Age Distribution: Analysis of the age distribution of presenters.

Visualization: Pie chart.
Insights: Distribution of presenter ages in percentages.

  **5. Shark Investment Analysis**

Investment by Sharks: Total investment amounts by each shark across all seasons.
Visualization: Bar plot.
Insights: Comparison of the total investments made by different sharks.
