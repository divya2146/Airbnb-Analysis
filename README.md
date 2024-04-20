# Airbnb-Analysis
This project is an exploration and analysis of Airbnb data with a focus on geospatial and exploratory data analysis. It includes interactive visualizations, statistical insights, and recommendations for users interested in Airbnb accommodations in specific countries and cities.

Introduction ==>
The Airbnb Geospatial Analysis project provides users with tools to analyze Airbnb data from various countries and cities. It offers features such as:

- Geospatial analysis to visualize Airbnb listings on a map.
- Exploratory Data Analysis (EDA) for understanding price distributions, top hotels, and more.
- Recommendations based on user-defined criteria, including price range.

Usage==>
- Launch the Streamlit app by running main.py.
- Use the app to explore geospatial data, select countries and cities, set price filters, and view recommendations.
- Analyze the exploratory data analysis (EDA) visualizations for insights into Airbnb data.

Exploratory Data Analysis===>
    
The project includes an EDA section with several interactive visualizations, including:

- Price Analysis by Country and City.
- Distribution of Price by Country.
- Distribution of Price using Box Plot.
- Scatter Plot by Price and Availability.

  Here's the workflow of the project:

1.Import libraries: Streamlit, streamlit_folium, folium, pandas, seaborn, matplotlib, plotly.express, plotly.graph_objects, plotly.subplots
2.Set webpage configurations: Page title, icon, layout
3. Set suppress deprecation warning: for pyplot
4. Display title: AirBnb Geospatial Analysis
5. Read CSV data: airbnb_dataset.csv
6. Group data by country and city: count occurrences
7. Create tabs: Geospatial Analysis and Exploratory Data Analysis
8. In Geospatial Analysis tab:
- Select a country
- Depending on the country, select a city from a predefined list
- Input minimum and maximum price range
9. If all inputs are provided:
- Query data based on selected country, city, price range
- Reset index
- Create base map centered on first entry's coordinates
- Loop through data:
 Add marker to map with popup displaying details (ID, name, price, review score)
- Render map using streamlit_folium
- Display top hotels based on price and review score (sorted descending)
- Display top hotels by price and review score from original data (not filtered by price range)
- Input field to enter ID for detailed hotel information (checks within filtered data)
10 In Exploratory Data Analysis tab:
- Select type of analysis from dropdown
11.Price Analysis by Country:
- Create animated histogram showing city distribution by country with color representing country
- Display table showing number of hotels by country and city (commented out)
- Display table showing average price and review score grouped by country and city (sorted descending by price and review score)
12.Distribution of Price by Country:
- Select country
- Depending on the country, select a city from a predefined list
- Create and display price distribution plot for the selected city and country
- Analyze and display skewness of the price distribution
13.Distribution of Price using Box Plot:
- Create box plot showing price distribution by country
14:Scatter Plot by Price and Availability:
- Create subplots for each availability type (30, 60, 90, 365 days)
- Add scatter plots to each subplot showing price vs availability

This code builds a web app to explore Airbnb data. Users can filter by country, city, and price to see listings on a map and analyze price distribution.

It can be a foundation for a real-time application by integrating features like:-

1.Live availability updates: Instead of static availability information, the application could connect to Airbnb's API to show real-time availability for listings.
2.Dynamic pricing updates: Prices on Airbnb can fluctuate based on demand. A real-time connection could update listing prices as they change.
3.Interactive filtering: Currently, filter selections require reloading the entire page. A real-time implementation could update results instantly based on user selections.
