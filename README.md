# Zomato Data Analysis

This repository contains the code and analysis performed on a Zomato dataset. The objective of this analysis was to derive insights from the data, including geospatial analysis and text analysis, to understand patterns and trends in restaurant ratings, online ordering, and customer reviews.


## Project Overview

This project involves analyzing a Zomato dataset to extract meaningful insights about restaurant ratings, online ordering, and customer reviews. The analysis includes geospatial mapping of restaurants, text analysis of customer reviews, and creating visualizations to represent the data findings.

## Dataset

The dataset contains the following columns:

- `index`
- `url`
- `address`
- `name`
- `online_order`
- `book_table`
- `rate`
- `votes`
- `phone`
- `location`
- `rest_type`
- `dish_liked`
- `cuisines`
- `approx_cost(for two people)`
- `reviews_list`
- `menu_item`
- `listed_in(type)`
- `listed_in(city)`

## Data Processing and Analysis Steps

1. **Reading the Data:**
   - The data was read from a SQLite database using `sqlite3`.

2. **Data Cleaning:**
   - Handled missing values, particularly in the `dish_liked` column.
   - Performed data cleaning to prepare the data for text analysis.

3. **Relation Between Online Order and Rating:**
   - Created a pivot table to analyze the relationship between the availability of online ordering and restaurant ratings.
   - Visualized the findings using a stacked bar chart.

4. **Data Cleaning for Text Analysis:**
   - Used `RegexpTokenizer` for text tokenization.
   - Created a sample dataset of 10,000 records for faster processing.

5. **Unigram Analysis:**
   - Performed unigram analysis and removed stopwords, including additional custom stopwords.

6. **Bi-gram and Trigram Analysis:**
   - Conducted bi-gram and trigram analysis on the cleaned text data.

7. **Geospatial Analysis:**
   - Extracted geographical coordinates from the `address` and `location` columns.
   - Manually filled missing longitude and latitude values.

8. **Heat Maps:**
   - Built geographical heat maps to visualize restaurant locations and density.

## Geospatial Analysis

- Extracted and cleaned geographical coordinates.
- Created heat maps to represent the distribution of restaurants across different locations.

## Text Analysis

- Conducted unigram, bi-gram, and trigram analysis on customer reviews.
- Removed stopwords to focus on meaningful terms.
- Generated visual representations of common terms and phrases.

## Visualizations

- Created visualizations to showcase the relationship between online ordering and restaurant ratings.
- Built heat maps to display restaurant density and geographical distribution.

## Conclusion

This analysis provides insights into the patterns and trends in restaurant ratings, online ordering, and customer reviews. The visualizations help in understanding the geographical distribution of restaurants and the common terms used in reviews.

## Requirements

- Python 3.x
- sqlite3
- pandas
- numpy
- matplotlib
- seaborn
- nltk
- folium

