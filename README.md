

# *Nintendo/GameFreak Pokemon Pokedex EDA*

## Business Case 

The Pokemon Pokedex is a fictional digital database that holds data on species called "Pokemon". This database is consistently evolving as new species are created by the talented people over at Game Freak and Nintendo.

With each game release there has been notable adjustments to the core gameplay. Primarily the inclusion of new features and new Pokémon. In the most recent years there has been a notable decline in new species, and a trend of revisiting old Pokémon and creating variations from them that vary by region.

By performing exploratory data analysis, I discover which bias the developers have had in the development of these Pokémon. Utilizing features that correspond to the core statistics that showcases a Pokémon’s combat potential, I began to see which types were favorited and which ones that were not. In these discoveries I saw the affinities that lie within particular Pokémon types. This could lead to potential type combinations that do not exist currently and can allow for further innovation in the species development process.



## Table of Contents

<details>
    <summary>Open</summary>

        1. File Descriptions
        2. Technologies Used
        3. Executive Summary

</details>

## File Descriptions

<details>
    <summary>Open</summary>

- bulbapedia_webscraper.py: Python Script that scrapes bulbapedia on pokemon to add to the pokedex.
- bulbapedia_data.csv: pokedex pre-clean.
- cleaned_pokedex.csv: pokedex post-clean.
- Pokemon_Pokedex_EDA.ipynb: jupyter notebook on data anaylsis.

</details>

## Technologies Utilized

<details>
    <summary>Open</summary>

        1. Python3
        2. Pandas
        3. Matplotlib
        4. Seaborn
        5. ski-kit learn
        6. Numpy
        7. Beautiful Soup
</details>

 ## Executive Summary

### Webscraping Beautiful Soup
<details>
    <summary>Open</summary>
    <h3>Webscraping</h3>
    <h4>Goal</h4>
    <p>The goal set for this project is to produce value for game freak and nintendo pokemon development team. This can be acomplished by identifying their bias within the species development process and locating the untapped potential of species type combinations. The primary hypothesis was "Do pokemon types influence stat distributions ?" The secondary question was "Are those pokemon types more favorable when it comes to stat distributions " The final question being "What suggestions could be proposed from the findings on this dataset"</p>
    <h4>Features Scraped</h4>
        <ul>
        <li>Dex No</li> 
        <li>Name</li>
        <li>Generation</li>
        <li>Primary Type</li>
        <li>Secondary Type</li>
        <li>Health</li>
        <li>Attack</li>
        <li>Defense</li>
        <li>Sp. Attack</li>
        <li>Sp. Defense</li>
        <li>Speed</li>
        <li>BST</li>
        </ul>
</details> 

### Data Cleaning and Early EDA
<details>
    <summary>Part 1</summary>
    <h3>Data Cleaning and Feature Engineering</h3>
    <p>The Data scraped presented a shape of 958 rows and 12 columns, due to messy nature of scraped data I had to performing some cleaning. This included filling the NaN values, removing duplicates, replacing column values, and appending missing rows.</p>
    <p>The cleaned pokedex (dataset) now has a shape of 892 rows and 19 columns. The added columns are a combination of features that categorize and classify species roles in combat.</p>

  <h4>Added Features Described</h4>
        <ul>
        <li><b>Physical Sweeper</b> : Attack + Speed</li> 
        <li><b>Special Sweeper</b>: Special Attack + Speed</li>
        <li><b>Wall</b>: Health + Defense + Special Defense</li>
        <li><b>Special Tank</b>: Special Attack + Special Defense</li>
        <li><b>Physical Tank</b>: Attack + Defense</li>
        </ul>
</details>

<details>
    <summary>Part 2</summary>
    <h3>Early Eda</h3>
    <p>The newly cleaned pokedex in addition with the added features can present some interesting insights. With my intial hypothesis to see if species type influence stat distributions, I plot each type compared to one of the primary features.
    <h5>Attack Violin Plot Distributions of all 18 types</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/attack_violin.png?raw=true" alt="Attack Violin Plot">
    The median values for Fighting and Dragon types are the highest amongst all others types with no major outliers. To inspect those further I compared the types with the speed distribution. I selected the speed feature as this is the second feature that comprises the combination for the created feature "Physical Sweeper". This feature categorizes a species that has a high affinity for attacking fast.
    <h5>Speed Violin Plot Distributions of all 18 types</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/speed_violin.png?raw=true" alt="Speed Violin Plot">
    The median values for Dragon type speed appears to be really high again in comparasion to the other types. Fighting appears to be lower, while electric and fire show high medians and distributions for speed. This leads me to inspect the physical sweeping capabilties of each type by plotting the medians values.
</details>
<details>
    <summary>Part 3</summary>
    <h3>Further Eda</h3>
    <h5>Physical Sweeper Plot of all 18 types</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/ps_barplot.png?raw=true" alt="Physical Sweeper Bar Plot">
    The Dragon, Fighting, Fire and Electric are all types that were previously identified for having high attack, high speed, or a combination of both. I want to further explore this data to see if there is a trend. Particularly types having high affinities in the features I created that comprise of stat combinations.
    <h5>Special Sweeper Plot of all 18 types</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/ss_barplot.png?raw=true" alt="Special Sweeper Bar Plot">
    The combined median values for Sp. Attack and Speed are represented here. Dragon appears once again near the top of the stack and Bug towards the bottom.
    <h5>Wall Bar Plot of all 18 types</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/wall_barplot.png?raw=true" alt="Wall Bar Plot">
    A "Wall" represents a species Health, Defense and Sp. Defense values. Dragon makes another appearance. So far we have represented all of the possible stat values and Dragon has appeared. However lets explore the two remaining arch-types for a through anaylsis.
    <h5>Physical Tank Bar Plot of all 18 types</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/pt_barplot.png?raw=true" alt="Physical Tank Bar Plot">
    Dragon again rounds out the top 5.
    <h5>Special Tank Bar Plot of all 18 types</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/st_barplot.png?raw=true" alt="Special Tank Bar Plot">
</p>
    In this last plot Dragon again rounds out the upper third of the bar plot. I collected the data based on the type placement and trends. To create a new dataframe with those findings.
    <h5>Type Plotting against Favorable and Unfavorable feature.</h5>
<img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/point_plot.png?raw=true" alt="PairGrid">
</details>

<details>
    <summary>Part 4</summary>
    <h3>Summarizing Findings</h3>
    <h4>Do pokemon types influence stat distributions ?</h4>
    <p>
    After evaluating the data and you can see that pokemon types do heavily influence stat distributions. The Development team at Game Freak heavily favorites <b>Dragon</b> type pokemon where as they do not favor <b>Bug</b> type pokemon. <b>Water</b> type they appear to be indifferent on as they have no favorable or unfavorable arch-types based on median values.
    <h4>Are those pokemon types more favorable when it comes to stat distributions</h4>
    <p>This question was an interesting one to answer as select types appear in the upper third of the stat distributions. Notably Dragon, Ice, Electric, Steel, Rock, and Fire. These types represent high stat distributions and more appearances in the favorable third, less while showing up less in the unfavorable third of the barplots. Dragon type being the only exception, being that they do not make any appearance other than in favorable. This leads me to the "balanced" types those are types that make equal appearances in both favorable and unfavorable those are, Ground, Flying, Fairy, Fighting, and Psychic. Then they're the unfavorable, those of which I believe can be explored further by the GameFreak. These types include, Poison, Normal, Grass, Bug, Ghost, and Dark. Then there is Water the only type that is neither favorable or unfavorable.</p>
    <h4>"What suggestions could be proposed from the findings on this dataset"</h4>
    <p>When exploring this data and understanding the bias, trends and distribution of data I began to look more towards the amount of pokemon released each generation.</p>
    <img src="https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/pokedex_count.png?raw=true" alt="Pokedex Count">
    I saw that they was a trend of rise and fall with the introduction of new species. After generation five there was a major decline and a stagnation in the number of new pokemon released. Which leads me to showcase those pokemon that have unfavorable stat distributions, this analysis showcased that types influence stats and those stats impact how well a pokemon can perform in battle. Poison, Normal, Grass, Bug, Ghost, and Dark pokemon should be more heavily focused on perhaps combining types that are unfavorable and those that are favorable.
    <details>
    <summary>Part 5</summary>
    <h3>Closing Thoughts</h3>
    <p> This project I hope can produce value for GameFreak and Nintendo when developing their next game. I seek to revisit this project and performing machine learning on the features. To perhaps predict base stat distributions on unreleased pokemon by exploring type combinations using MLR or Neural Networks to predict what stats can be increased for each type to shift them into a more favorable position, while not over powering them like dragon types have been and currently are. </p>
</details>



    


