

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
    <p>The goal set for this project is to produce value for game freak and nintendo pokemon development team. This can be acomplished by identifying their bias within the species development process and locating the untapped potential of species type combinations. The primary hypothesis was "Do pokemon types influence stat distributions ?" The secondary question was "Are those pokemon types more favorable when it comes to stat distributions " The final question being "How can I express stat combinations as roles that pokemon play to categorize these types functionality in a real world scenerio" e.g combat is one of the game core mechanics so a role one pokemon serves in combat can be described as a "physical sweeper" a stat combination of Physical attack and speed.</p>
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
    <summary>Open</summary>
    <h3>Data Cleaning</h3>
    <h4>Part 1</h4>
    <p>The Data scraped presented a shape of 958 rows and 12 columns, due to messy nature of scraped data I had to performing some cleaning. This included filling the NaN values, removing duplicates, replacing column values, and appending missing rows.</p>
    <p>The cleaned pokedex (dataset) now has a shape of 892 rows and 19 columns. The added columns are a combination of features that categorize and classify species roles in combat.</p>
</details>

<details>
    <summary>Open</summary>
    <h3>Early Eda</h3>
    <h4>Part 2</h4>
    <p>The newly cleaned pokedex in addition with the added features can present some interesting insights. With my intial hypothesis to see if species type influence stat distributions, I plot each type compared to one of the primary features.
![](https://github.com/AlignedMind/Pokedex_EDA_Project/blob/master/Analysis_Images/attack_violin.png)   
</p>
    

</details>




