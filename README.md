

# New York City Airbnb Data Analysis
![](https://github.com/PrajwalGpy/Airbnb_Data_Analysis_Python/blob/main/New-York-City-Brooklyn-Bridge-Panorama-Juergen-Roth-2.jpg)

## Project Overview

This project performs an in-depth exploratory data analysis (EDA) on the New York City Airbnb listings dataset (`datasets.csv`). The primary goal is to uncover trends, patterns, and insights related to pricing, availability, location, and host activity. This analysis serves as a practical demonstration of data cleaning, manipulation, visualization, and interpretation skills using Python's data science stack.

## Dataset

The dataset used is `datasets.csv`, which contains detailed listing information for Airbnb properties in New York City.

Key columns in the dataset include:

  * `id`: Listing ID
  * `name`: Name of the listing
  * `host_id`: Host ID
  * `host_name`: Name of the host
  * `neighbourhood_group`: The main borough (e.g., Manhattan, Brooklyn)
  * `neighbourhood`: Specific neighborhood (e.g., Harlem, Bushwick)
  * `latitude`, `longitude`: Geographic coordinates
  * `room_type`: Type of listing (e.g., Entire home/apt, Private room)
  * `price`: Price per night (in USD)
  * `minimum_nights`: Minimum number of nights required for a stay
  * `number_of_reviews`: Total number of reviews
  * `last_review`: Date of the most recent review
  * `reviews_per_month`: Average number of reviews per month
  * `availability_365`: Number of days the listing is available out of 365
  * `rating`: Overall guest rating
  * `bedrooms`, `beds`, `baths`: Property amenities

## Key Questions & Objectives

The analysis aims to answer the following key questions:

1.  What is the distribution of listings across different boroughs (`neighbourhood_group`)?
2.  How do `price` and `rating` vary by `room_type` and `neighbourhood_group`?
3.  What are the most expensive neighborhoods for an Airbnb rental?
4.  What is the relationship between `price`, `number_of_reviews`, and `availability_365`?
5.  Who are the top hosts based on the number of listings (`calculated_host_listings_count`)?
6.  What is the typical availability (`availability_365`) of listings, and does it vary by area?

## Analysis Workflow

The project follows a standard data analysis workflow as detailed in the `Project4Paython.ipynb` notebook:

1.  **Data Loading:** Imported the `datasets.csv` file into a `pandas` DataFrame.
2.  **Data Cleaning & Preprocessing:**
      * Handled missing values in columns like `rating`, `last_review`, and `reviews_per_month`.
      * Checked for and removed any duplicate listings.
      * Corrected data types for analysis (e.g., ensuring `price` is numeric).
3.  **Exploratory Data Analysis (EDA):**
      * Calculated descriptive statistics for numerical features.
      * Analyzed the frequency distribution of categorical features like `room_type` and `neighbourhood_group`.
      * Created visualizations to answer the key questions defined above.

## Key Findings & Visualizations

### Finding 1: Manhattan is the Most Expensive Borough, While Private Rooms Offer a Budget-Friendly Alternative

  * **Insight:** The analysis shows a clear price hierarchy. Manhattan has the highest median price for "Entire home/apt" listings, significantly more expensive than other boroughs. "Private rooms" are consistently the cheapest option across all five boroughs.
  * **Visualization:**
      * **Interpretation:** Travelers seeking budget-friendly options should focus on private rooms, particularly outside of Manhattan. Hosts with entire homes in Manhattan can command premium pricing.

### Finding 2: Most Listings are Rarely Available

  * **Insight:** A large portion of listings (over XX%) have very low availability (e.g., less than 60 days a year). This suggests many hosts are casual renters rather than full-time property managers.
  * **Visualization:**
      * **Interpretation:** This could imply regulatory effects (like NYC's 30-day minimum) or that many listings are primary residences.


### Finding 3: A Small Number of "Super-Hosts" Dominate the Market

  * **Insight:** The New York City Airbnb market is heavily influenced by a few professional hosts and property management companies. The analysis of `calculated_host_listings_count` reveals that the top 10 hosts manage a combined total of over 3,000 listings, with the top host, **Blueground**, managing over 700 properties alone.

  * **Visualization:** This bar chart of the "Top 10 Hosts by Number of Listings" clearly illustrates this market concentration. The drop-off from the top hosts to even the 10th-ranked host is significant, highlighting the scale of these top operations.

  * **Interpretation:** This finding indicates that the NYC Airbnb landscape is not solely comprised of casual, individual homeowners renting out a spare room. Instead, it has a substantial commercial component. These large-scale operations, which function like hotel businesses, likely have a significant impact on rental availability and pricing in their respective neighborhoods. This commercialization is a key factor for any analysis of the platform's community or economic impact.

### Tools & Libraries Used

  * **Python 3**
  * **Pandas:** For data loading, cleaning, and manipulation.
  * **NumPy:** For numerical operations.
  * **Matplotlib:** For creating static, base visualizations.
  * **Seaborn:** For advanced and aesthetically pleasing statistical visualizations.
  * **Jupyter Notebook:** For interactive analysis and code development.

## How to Reproduce

To run this analysis yourself:

1.  Clone this repository:
    ```bash
    git clone https://github.com/PrajwalGpy/Airbnb_Data_Analysis_Python.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd Airbnb_Data_Analysis_Python
    ```
3.  Install the required dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```
4.  Ensure the `datasets.csv` file is in the root of the project directory.
5.  Launch the Jupyter Notebook:
    ```bash
    jupyter notebook Project4Paython.ipynb
    ```
