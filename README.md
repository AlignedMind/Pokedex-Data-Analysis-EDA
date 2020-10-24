

# *Nintendo/GameFreak Pokemon Pokedex EDA*

## Business Case 

The Pokemon Pokedex is a fictional digital database that holds data on species called "Pokemon".
This database is consistantly evolving as new species are created by the talented people over at GameFreak and Nintendo.

With each game release there has been notable adjustments to the core gameplay. Primarily the inclusion of new features and new pokemon. In the most recent years there has been a notable decline in new species, and a trend of revisting old pokemon and just creating variations from them that vary by region.

By performing exploratory data analysis, I discover which bias the developers have had in the development of these pokemon. Utilizing features that correspond to the core statistics that showcases a pokemons combat potential, I began to see which types were favorited and which ones that were not. In these discoveries I saw the affinities that lie within particular pokemon types. This could lead to potential type combinations that do not exist currently and can allow for further innovation in the species development process.

## Directory

1. File Descriptions
2. Technologies Used
3. Jupyter Notebook Structure
4. Executive Summary
    1.1 Webscraping Data Collection (Beautiful Soup)
        1.2 Import Libraries
        1.3 DataFrame Cleaning and Aggregation
            1.3.1 Replacing NaN Values
            1.2.2 Removing Duplicate Rows
            1.3.3 Replacing Column Values
            1.3.4 Appending Missing Rows
        1.4 Feature Engineering
            1.4.1 Label Encoding Pokemon Types
            1.4.2 Creating Labels to Categorize Pokemon on Base Stat Tier
            1.4.3 Creating Features by Joining stat from archtypes.
        1.5 Looking for Correlations
            1.5.1 Describing Data
        1.6 Early Data Visualization
            1.6.1 Health Stat Distributions
            1.6.2 Attack Stat Distributions
            1.6.3 Defense Stat Disributions
            1.6.4 Sp. Attack Stat Disributions
            1.6.5 Sp. Defense Stat Disributions
            1.6.6 Speed Stat Disributions
        1.7 Further Data Visualizations
            1.7.1 Histogram Distribution of Stat Features
            1.7.2 Scatter Matrix of the three Primary Stat Correlations to Base Stat.
            1.7.3 PairGrid of Archtype 
            1.7.4 Heatmap of features
        1.8 Data Visualization of Strongest Correlations to Base Stat.
            1.8.1 Physical Sweeper
            1.8.2 Special Sweeper
            1.8.3 Wall
            1.8.4 Physical Tank
            1.8.5 Special Tank
        1.9 Visualization of the total number of pokemon introduced in each Generation.





