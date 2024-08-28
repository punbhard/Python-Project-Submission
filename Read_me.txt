Movie Recommendation Script
----------------------------
This Python script uses the Selenium library to scrape movie information from the Rotten Tomatoes website based on a user-selected genre. It then displays a random movie recommendation from the selected genre.
Requirements

-Python 3.x
-Selenium library (pip install selenium)
-Pandas library (pip install pandas)
-Chrome web driver (or the web driver for your preferred browser)

Installation
-------------
-Clone the repository or download the script file.
-Install the required Python libraries using pip:
   pip install selenium pandas
-Download the appropriate web driver for your browser and add it to your system's PATH. For example, if you're using Chrome, you can download the Chrome driver from the official [ChromeDriver website](https://sites.google.com/a/chromium.org/chromedriver/downloads).

Usage
------
-Run the script:

    python movie_recommendation.py

-When prompted, enter a genre from the list (e.g., "action", "comedy", "drama").
-The script will display a random movie recommendation from the selected genre.

Script Overview
----------------
-The script imports the necessary libraries: webdriver and By from the selenium library, WebDriverWait for handling dynamic content, and pandas for data manipulation.
-It defines a list of genres Genre_List that the user can choose from.
-The script prompts the user to choose a genre from the list. If the user enters a valid genre, the script proceeds to the next step. If the genre is not in the list, the script prompts the user to choose again.
-The script creates a webdriver instance (in this case, a Chrome driver) and navigates to the Rotten Tomatoes website's "Movies in Theaters" page, filtering the results by the user-selected genre.
-It then extracts the movie titles and release dates using Selenium's find_elements method and XPath expressions.
-The script creates a pandas DataFrame Movie_data with the extracted movie titles and release dates.
-Finally, the script randomly selects a movie from the Movie_data DataFrame and prints the movie information.

Limitations
---------------
-The script's functionality is limited to the data available on the Rotten Tomatoes website at the time of its last update (August 2023).
-The script only displays a single random movie recommendation and does not provide any additional information or functionality